---
Date Created: 2025-06-04 21:45
Last Updated: 2025-06-04 21:45
tags: 
Index: 
Topic:
  - "[[Chronological UX (WNC-supply-sites)]]"
Status: Unweathered
Published: true
Author:
---
---

## ✅ **Airtable Features to Replace (Grouped by Function)**

### 🗂️ **Kanban Workflow (Delivery Lifecycle Tracking)**

**Used For:**

- Visual tracking of deliveries through stages:
    
    - `Uncategorized`
        
    - `Driver Volunteered`
        
    - `Creating Dispatch`
        
    - `Assigning Driver`
        
    - `Confirming`
        
    - `Confirmed`
        
    - `Delivery In Progress`
        
    - `Delivery Complete`
        

**Replacement Needs:**

- Web-based drag-and-drop interface or status-based update logic
    
- Delivery object with `status` enum and `updatedAt` timestamps
    
- Role-based permissions (e.g., dispatcher-only updates)
    
- Activity log / audit trail
    

---

### 👤 **Driver Grid View**

**Used For:**

- Listing:
    
    - Name
        
    - Vehicle Type
        
    - Current Location (if manually input)
        
    - Phone Number
        
    - Availability
        

**Replacement Needs:**

- Driver profile dashboard
    
- Location opt-in (manual or GPS optional)
    
- Driver availability settings (schedule picker or status toggle)
    
- Admin-accessible table of all registered drivers
    

---

### 📋 **Delivery Creation Form**

**Used For:**

- Manually creating dispatch entries:
    
    - Pickup site
        
    - Dropoff site
        
    - Driver
        
    - Date/time
        
    - Items (auto-filled via "add eligible items" button)
        
    - Dispatcher notes
        
    - Attachments
        

**Replacement Needs:**

- Delivery creation modal/form
    
- Site + driver dropdowns w/ autocompletion
    
- Server-side logic to pull eligible items (see below)
    
- Optional file uploads (PDF manifests, ID photos, etc.)
    
- Admin UX for preview/edit
    

---

### 🔄 **“Add Eligible Items” Button**

**Used For:**

- Pulls items from **pickup** and **dropoff** inventories that match
    
    - E.g., Pickup has “trash bags” oversupplied, Dropoff needs “trash bags”
        

**Replacement Needs:**

- Server endpoint that:
    
    - Accepts pickup + dropoff site IDs
        
    - Compares inventory states
        
    - Returns list of intersecting item types
        
- Fallback UX if WSS IDs are missing or no items match
    

---

### 📤 **Send Confirmation**

**Used For:**

- Sends SMS (via backend) to:
    
    - Pickup site contact
        
    - Dropoff site contact
        
    - Driver
        
- Includes manifest link for confirmation
    

**Replacement Needs:**

- SMS API integration (e.g., Twilio)
    
- Backend logic to:
    
    - Generate secure manifest links (UUID tokens or short codes)
        
    - Track confirmation status for each party
        
- UI to preview manifest before sending
    
- Trigger logic to move delivery to “Confirming” state
    

---

### 📝 **Comments, Attachments & Dispatcher Notes**

**Used For:**

- Manual notes per delivery
    
- Optional attachment uploads (not detailed in walkthrough but mentioned)
    

**Replacement Needs:**

- Notes field per delivery
    
- Attachment upload system (e.g., PDFs, images)
    
- Permission gating (e.g., only dispatcher can add internal notes)
    

---

## 📦 **Optional Bonus Features To Rebuild or Improve**

|Airtable Feature|Upgrade Opportunity|
|---|---|
|No error message when “eligible items” fails|Add clear frontend feedback|
|Auto-redirect buttons to web interface|Deep-link into specific filtered views|
|Driver current location field (manual)|GPS optional update or auto ping|
|Confirmation without all parties checking|Enforce 3/3 confirmation or timed fallback|

---

Would you like this reformatted as a:

- ✅ GitHub Epic breakdown
    
- ✅ Airtable → Postgres schema migration spec
    
- ✅ Developer handoff doc?
    

Let me know and I’ll prep the output accordingly.

---

# Potential FOSS Alternatives?

Certainly! Here's a structured list of Airtable functionalities currently in use within the WNC Supply Sites platform, along with suggested open-source alternatives to replace each component. This approach aims to maintain or enhance existing capabilities while ensuring compatibility with your tech stack and operational requirements.

---

## 🗂️ Airtable Functionalities & Open-Source Replacements

### 1. **Kanban-Style Delivery Tracking**

- **Current Use**: Visual workflow for deliveries (e.g., "Driver Volunteered" → "In Progress" → "Complete").
    
- **Replacement Options**:
    
    - **Kanboard**: A minimalist, self-hosted Kanban board with features like task filtering and WIP limits.
        
    - **Planka**: Trello-like interface with real-time updates and markdown support.
        
    - **WeKan**: Customizable and privacy-focused Kanban board. ([opensource.com](https://opensource.com/alternatives/trello?utm_source=chatgpt.com "5 open source alternatives to Trello | Opensource.com"), [wekan.github.io](https://wekan.github.io/?utm_source=chatgpt.com "WeKan ® — Open-Source kanban"))
        

### 2. **Grid View for Driver Profiles**

- **Current Use**: Tabular display of driver details (name, location, vehicle type, availability).
    
- **Replacement Options**:
    
    - **InvenTree**: Open-source inventory management with customizable fields, suitable for tracking driver assets.
        
    - **Snipe-IT**: IT asset management system that can be adapted for personnel tracking. ([snipeitapp.com](https://snipeitapp.com/?utm_source=chatgpt.com "Home - Snipe-IT Free open source IT asset management"))
        

### 3. **Needs Matching Interface**

- **Current Use**: Matching supply sites' needs with available resources.
    
- **Replacement Options**:
    
    - **OpenBoxes**: Supply chain management system tailored for healthcare and disaster relief logistics.
        
    - **ERPNext**: Comprehensive ERP with modules for inventory and supply chain management. ([track-pod.com](https://www.track-pod.com/?utm_source=chatgpt.com "Track-POD: Delivery Management Software, Proof of Delivery App"), [openboxes.com](https://openboxes.com/?utm_source=chatgpt.com "OpenBoxes"))
        

### 4. **Driver Registration & Availability Management**

- **Current Use**: Collecting driver information and managing their availability.
    
- **Replacement Options**:
    
    - **Fleetbase**: Modular logistics platform supporting driver management and route planning.
        
    - **Odoo Fleet Management**: Part of the Odoo suite, offering vehicle and driver management features. ([dispatchtrack.com](https://www.dispatchtrack.com/?utm_source=chatgpt.com "The Global Leader in Last Mile Delivery Software"), [onfleet.com](https://onfleet.com/?utm_source=chatgpt.com "Last Mile Delivery Software for Dispatch and Route Management"), [fynd.com](https://www.fynd.com/blog/fleet-management-software-open-source?utm_source=chatgpt.com "Top 20 Fleet Management Software Open-Source in 2025 - Fynd"))
        

### 5. **Delivery Creation & Confirmation Workflow**

- **Current Use**: Setting up deliveries, assigning drivers, and confirming deliveries via SMS.
    
- **Replacement Options**:
    
    - **Enatega**: Open-source delivery app solution with real-time tracking and proof of delivery features.
        
    - **Track-POD**: Delivery management software with electronic proof of delivery and real-time driver performance monitoring. ([sdi-tool.org](https://sdi-tool.org/?utm_source=chatgpt.com "Snappy Driver Installer - Install and Update Drivers for Free"), [track-pod.com](https://www.track-pod.com/?utm_source=chatgpt.com "Track-POD: Delivery Management Software, Proof of Delivery App"))
        

### 6. **Inventory Management & Site Status**

- **Current Use**: Managing site inventories, statuses, and visibility settings.
    
- **Replacement Options**:
    
    - **InvenTree**: Offers intuitive parts management and stock control, suitable for tracking site inventories.
        
    - **OpenBoxes**: Designed for managing supplies and medications, with features for tracking site statuses. ([inventree.org](https://inventree.org/?utm_source=chatgpt.com "InvenTree"), [openboxes.com](https://openboxes.com/?utm_source=chatgpt.com "OpenBoxes"))
        

### 7. **Public Search & Filter Interface**

- **Current Use**: Allowing the public to search and filter supply sites based on various criteria.
    
- **Replacement Options**:
    
    - **ERPNext**: Provides customizable portals and search functionalities.
        
    - **Odoo**: Offers website builder with dynamic filtering capabilities.
        

---

## 🔧 Implementation Considerations

- **Integration**: Ensure that chosen tools can integrate seamlessly with your existing tech stack (Spring Boot, PostgreSQL, etc.).
    
- **Customization**: Evaluate the ease of customizing each tool to fit specific workflow requirements.
    
- **Community Support**: Prefer tools with active communities for better support and continuous improvement.
    

---

Would you like assistance in drafting GitHub issues or setting up a phased implementation plan for these replacements?