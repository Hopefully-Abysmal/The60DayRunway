---
Date Created: 2025-06-04 21:44
Last Updated: 2025-06-04 21:44
tags: 
Index: 
Topic:
  - "[[Chronological UX (WNC-supply-sites)]]"
Status: Unweathered
Published: true
Author: 
---
---

Here’s a breakdown of **what the backend is likely doing at each step** of the workflow you described, inferred from behavior and system design:

---

## 🏢 **Supply Site Registration & Setup**

### Backend Responsibilities:

- **Create new `Site` record** in DB (e.g., `SiteEntity`)
    
- Store structured metadata:
    
    - Address, contact, hours, manager list
        
    - Boolean flags: `acceptingPublic`, `distributingToPublic`, `publicVisible`, `isActive`
        
    - Enum field: `siteType = {DISTRIBUTION_CENTER, WAREHOUSE}`
        
- Initialize empty inventory tied to site (`ItemStatus` per itemID)
    
- Save `MaxLoadCapacity` and any `ReceivingInstructions`
    
- Add `siteManagers` via `UserPhoneNumber → Whitelist` table
    
- Generate unique `WSS ID` for cross-system matching
    

---

## 📦 **Inventory Management (Supply Site Portal)**

### Backend Responsibilities:

- Lookup or match items using existing `ItemTaxonomy`
    
- If “Add New Item”:
    
    - Create new taxonomy entry or placeholder
        
- For each item:
    
    - Set `SupplyStatus = {UrgentlyNeeded, Needed, Available, Oversupply}`
        
    - Link to the current `SiteInventory` table
        
- Apply filters with tag-based (NOT fuzzy) search
    
- Update DB with inventory changes on item toggle
    

---

## 🚐 **Driver Registration & Route Matching**

### Backend Responsibilities:

- Jotform POSTs data to backend → create `DriverProfile`
    
    - Store: address, phone, license plate, availability, notes
        
    - Mark `status = active` or allow deactivation
        
- Enable driver login (likely by phone #)
    
- On login:
    
    - Serve eligible routes by:
        
        - Matching nearby pickup → dropoff pairs with item compatibility
            
        - Filter by `distanceThreshold` (maybe customizable later)
            
- **Route Matching Logic:**
    
    - For each pair of `Site A → Site B`:
        
        - IF A has `oversupply` AND B has `need` of same item → generate route
            
        - Use Haversine or Maps API for distance + drive time
            
- Likely batch generated and cached or live-generated upon driver login
    

---

## ✍️ **Alternative Volunteer Form (Ambiguous Use)**

### Backend Responsibilities:

- Likely creates a **DonationIntent** or **VolunteerIntent**
    
    - POST contact info, chosen site, selected items
        
- Possibly creates an unconfirmed `DeliveryDraft` or flags for manual review
    
- UX confusion likely due to single route used for multiple intents
    

---

## 📬 **Dispatch Process & Delivery Confirmation**

### Backend Responsibilities:

#### When Dispatcher Approves Driver:

- Update `Delivery.status = CONFIRMING`
    
- Set `pickupDate`
    
- Save dispatcher notes, attach driver to delivery
    
- Possibly generates backend event to trigger SMS/text queue
    

#### When Creating Delivery Manually:

- Backend creates `Delivery` object:
    
    - Links: driver, pickupSite, dropoffSite
        
    - Populates from `NeedsMatchingService`
        
    - If both sites have WSS IDs → perform item eligibility check
        
        - If not, skip silently (⚠️ bad UX, no server error raised)
            
- Autopopulate metadata like dispatcher name and volunteer window (optional)
    
- Stores form data in Airtable-linked DB or local copy
    

#### On “Add Eligible Items”:

- Pings backend:
    
    - Queries item overlap between pickup & dropoff
        
    - For each eligible item → add to `DeliveryItemList`
        
- No frontend error = backend likely returns empty silently if nothing matches
    

#### On “Send Confirmation”:

- Backend:
    
    - Saves state: `Delivery.status = CONFIRMING`
        
    - Generates secure `ManifestLink` tokens for:
        
        - Pickup site contact
            
        - Dropoff site contact
            
        - Driver
            
    - Triggers SMS queue with short-lived links
        
- `ManifestLink` may reference a `/confirm?token=` style endpoint
    

---

## 🗺️ **Needs Matching (Grid + Site View)**

### Backend Responsibilities:

- Query all `Sites` with `NeededItems > 0`
    
- Join table with inventory data to get:
    
    - Site → item match
        
    - Count of items needed
        
    - Geo distance from current user or ref site
        
- Return:
    
    - Closest matches sorted by distance
        
    - Possibly with transport estimates
        

---

## 🚚 **Delivery Lifecycle (Driver Confirm → Completion)**

### Backend Workflow:

1. **Manifest Confirmations** (driver, pickup, dropoff):
    
    - Each link triggers backend endpoint:
        
        - Verifies token
            
        - Sets confirmation bit (e.g. `isPickupConfirmed`)
            
    - Once all 3 confirmed:
        
        - Sets `Delivery.status = CONFIRMED`
            
2. **Day of Delivery:**
    
    - Driver sees “Start Delivery” button
        
        - Triggers:
            
            - `status = IN_PROGRESS`
                
            - SMS to pickup: “Driver en route”
                
    - "Arrived at pickup":
        
        - Log timestamp
            
    - "Leaving pickup":
        
        - SMS to dropoff: ETA + driver info
            
    - "Arrived at dropoff":
        
        - Finalize status:
            
            - `Delivery.status = COMPLETE`
                
            - Update all timestamps
                

⚠️ **Backend lacks enforcement logic for step progression**

- Driver can skip ahead (e.g., hit “Arrived at dropoff” before “Start Delivery”)
    
- No confirmation required between actions
    

---

## ⚠️ Risks & Observations

|Area|Backend Concern|Suggestion|
|---|---|---|
|Manifest Confirmation|No explicit auth check?|Enforce 1-click lock or time window expiry|
|Delivery flow|Skippable steps|Add FSM enforcement or mutex-style gatekeeping|
|Add Eligible Items|Silent failure|Add API response alert or frontend fallback|
|Form submission|Closes immediately|UX should confirm save or return to draft|

---

Let me know if you'd like this turned into a backend route map (`/api/site/create`, `/api/delivery/confirm`, etc.) or if you want a GitHub issue set for modularizing improvements!