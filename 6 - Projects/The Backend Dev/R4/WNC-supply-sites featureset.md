---
Date Created: "2025-06-17 16:09"
Last Updated: "2025-06-17 16:09"
tags: 
Index: 
Topic: 
Status: Unweathered
Published: true
Author: 
aliases:
---
To be compared to [[R4Dash Lovable MVP Breakdown]] to make [[wnc-s-s to R4Dash diff]]

## Live Links
https://wnc-supply-sites.com/
https://github.com/wnc-supply-sites/wnc-supply-sites/tree/master
https://deepwiki.com/wnc-supply-sites/wnc-supply-sites

## WNC Supply Sites – Feature Inventory (Frontend-Oriented)

This is a structured feature breakdown of the current WNC-Supply-Sites platform, focused solely on **frontend interactions** and **user-experience flows**, omitting backend implementation details. The goal is to create a baseline inventory to:

- **Compare to R4Dash for feature parity**
    
- **Identify key user flows**
    
- **Draft intelligent prompts for codebase assistant Devin**
    

---

### 🔎 Purpose and Scope

WNC Supply Sites is a web application designed to facilitate disaster relief operations by providing a centralized platform for managing supply sites, inventory, and delivery logistics. It supports redistribution of resources between supply warehouses and distribution centers across multiple deployments (e.g., WNC, SoCal).

---

### 🧭 Public Search & Discovery

- **Description:** Public-facing view of supply sites with filters
    
- **Features:**
    
    - County/item filters (Urgent / Needed / Available / Oversupply)
        
    - Site type filters (Distribution vs Warehouse)
        
    - Grid of site cards with status indicators
        
    - Simple search bar (non-fuzzy)
        
    - **Devin Ref:** `supplies.html` rendered via `SuppliesController.supplies()` — filters handled via JavaScript in `supplies.js`
        

### 🗂️ Site Manager Registration & Portal

- **Description:** Portal for managing site information and inventory
    
- **Features:**
    
    - Form to input site metadata (name, address, hours, visibility, site type, status)
        
    - Set site managers (via phone number whitelist)
        
    - Item inventory view (tagged by status: urgent, needed, available, oversupplied)
        
    - Add new items (tagged taxonomy UI)
        
    - Toggle public visibility and active/inactive state
        
    - **Devin Ref:** Inventory editing handled by `inventory.html` and `inventory.js` — status toggles managed via `changeItemStatus()` and backend calls to `InventoryController`
        

### 🔐 Phone Whitelist & Login Flow

- **Description:** Restricted login system for site managers via phone numbers
    
- **Features:**
    
    - Whitelist via Jotform or internal admin tool
        
    - Users set password post-whitelist
        
    - Auth persists session for portal usage
        

### 🚐 Driver Registration & Profile

- **Description:** Volunteer driver onboarding system
    
- **Features:**
    
    - Jotform registration (address, vehicle, availability)
        
    - Driver portal to view/edit info, deactivate profile
        
    - Grid view of drivers (location, availability, vehicle)
        
    - **Devin Ref:** Jotform webhook sends driver data to `/webhook/driver/upsert` handled by `DriverUpdatesWebhook`
        

### 🛣️ Route Matching & Delivery Creation

- **Description:** Delivery creation interface with dispatch logic
    
- **Features:**
    
    - Dispatcher builds delivery route manually or via site-to-site need matching
        
    - Form includes pickup/dropoff site, item count, dispatcher/driver, volunteer window
        
    - Add eligible items auto-query
        
    - Send confirmation triggers SMS with manifest links to driver/pickup/dropoff
        
    - **Devin Ref:** Route matching triggered in `BrowseRoutesController.browseRoutes()` → core logic in `BrowseRoutesDao.findDeliveryOptions()`
        

### 🧾 Manifest Confirmation Interface

- **Description:** Authless manifest view for each stakeholder to confirm participation
    
- **Features:**
    
    - Confirm/cancel buttons
        
    - Manifest includes map embed, pickup/dropoff addresses, items, contacts
        
    - Confirmation log converts manifest into live delivery state
        
    - **Devin Ref:** Links built via `DeliveryConfirmationController.buildConfirmUrl()` and `DeliveryController.buildDeliveryPageLinkWithCode()`
        

### 🚚 Live Delivery Flow (Driver Journey UI)

- **Description:** Driver-side flow once delivery is confirmed
    
- **Features:**
    
    - Step-by-step buttons:
        
        - Start Delivery → Arrived Pickup → Left Pickup → Arrived Dropoff
            
    - Each step triggers status update and SMS to parties
        
    - No gating logic—can skip steps
        
    - **Devin Ref:** UI in `delivery.html` with logic in `delivery.js` — step URLs generated server-side with role-aware tokens
        

### 🔍 Needs Matching (Grid + Site View)

- **Description:** Matchmaking interface for dispatchers
    
- **Features:**
    
    - Needs matrix between sites
        
    - Filter by item type and quantity
        
    - Site-level button to go to route builder or match maker
        
    - Displays closest match by item + distance
        

### 🔔 Delivery Confirmation Page (Admin View)

- **Description:** Admin summary of pending deliveries
    
- **Features:**
    
    - Status bar (uncategorized → delivery complete)
        
    - Each row editable pre-confirmation
        
    - Attachments, comments, item additions, manual editing
        
    - **Devin Ref:** Confirmation responses captured in `DeliveryConfirmationController.confirmRequest()`
        

---

### 🧠 Devin Codebase Overview (Contextual Reference)

The system is built using **Spring Boot**, **Mustache**, and **vanilla JS**, avoiding Spring Security and JPA. Core architectural layers include:

- Controllers (Site, Delivery, Inventory, Auth)
    
- Services (Notification, Inventory, Delivery, etc.)
    
- DAOs (PostgreSQL access via JDBI)
    
- Integration with R4, Airtable, and Twilio (via environment config)
    
- Multiple deployment targets (WNC, SoCal)
    

It includes core subsystems for:

- Supply Site Management (filterable site data, needs matching)
    
- Inventory Management (status-tagged items, taxonomy syncing)
    
- Delivery System (dispatch workflow, SMS confirmations, live status tracking)
    
- Authentication (auth cookie logic via RequestInterceptor)
    

Use this as a source of grounding when asking Devin about:

- Inventory, delivery, or status control logic
    
- Notification or webhook flow
    
- Integration contracts with Airtable, R4, or Twilio
    

#### ✅ Supplementary Devin Queries Now Answered

- Where is route matching triggered? → `BrowseRoutesController.browseRoutes()` and `BrowseRoutesDao.findDeliveryOptions()`
    
- Who handles manifest link generation? → `DeliveryConfirmationController.buildConfirmUrl()` and `DeliveryController.buildDeliveryPageLinkWithCode()`
    
- How is driver progress UI rendered? → `delivery.html` + `delivery.js`, status set via tokenized URL interactions
    
- How is inventory editing managed? → `inventory.js`, `toggleInventory()`, `changeItemStatus()`
    
- How is Jotform driver data integrated? → `DriverUpdatesWebhook` via POST `/webhook/driver/upsert`
    
- Where are SMS confirmations handled? → `DeliveryConfirmationController.confirmRequest()` and `cancelRequest()`
    
- What template shows public search/filter? → `supplies.html`, powered by `SuppliesController.supplies()`
    
- Where are Airtable views shown? → Not frontend; only backend integration via webhook endpoints

---

### 🔍 Suggested Devin Prompts (To Extract Code Functionality)

- "Where is the route matching logic triggered for drivers after they log in?"
https://deepwiki.com/search/where-is-the-route-matching-lo_cb33dbb0-64aa-4a16-ac7d-2d27cbc86c8e
```
Based on the codebase context, you're asking about the route matching logic for drivers in the WNC Supply Sites system. Let me trace through where this is triggered after driver login.

## Answer

The route matching logic for drivers is triggered through the **Browse Routes** system, which becomes accessible after drivers log in. Here's how it works:

### Authentication and Access Control

First, drivers must be authenticated to access the route browsing functionality. The `AuthInterceptor` enforces this by requiring authentication for the browse routes path AuthInterceptor.java:53-56 .

### Route Matching Entry Point

Once authenticated, drivers can access the route browser at `/browse/routes`, which is handled by the `BrowseRoutesController.browseRoutes()` method BrowseRoutesController.java:65-71 . This controller method checks if the user has the `DRIVER` role and sets the `isDriver` template parameter accordingly BrowseRoutesController.java:119 .

### Route Discovery and Filtering

The core route matching logic occurs in `BrowseRoutesDao.findDeliveryOptions()`, which finds potential delivery routes between sites with matching supply/need items BrowseRoutesController.java:100-105 . The results are then filtered using `RouteWeighting.filter()` to remove impractical routes.

### Driver Interface

In the frontend, drivers see a "Volunteer" button for each route only when they have the driver role routes.html:150-154 . When clicked, this triggers the volunteer workflow through JavaScript routes.js:25-31 .

### Volunteer Request Processing

When a driver confirms volunteering for a route, the request is sent to `/browse/routes/volunteer` and handled by `RouteVolunteeringController` RouteVolunteeringController.java:27-43 . This controller enriches the volunteer request with driver information from the database and forwards it to external systems.

## Notes

The route matching system is specifically designed for professional drivers (those with the `DRIVER` role), not general volunteers. There's a separate volunteer delivery system for non-professional volunteers that works differently. The route matching logic is automatically triggered when drivers access the browse routes page - there's no separate "matching" step, as routes are dynamically generated based on current supply/need data across sites.

Wiki pages you might want to explore:

- [Site Detail Pages (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/2.1-site-detail-pages)
- [Driver Portal (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/3.2-driver-portal)
- [Volunteer Delivery System (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/3.3-volunteer-delivery-system)
```

- "What function generates the manifest confirmation links and routes?"
https://deepwiki.com/search/where-is-the-route-matching-lo_cb33dbb0-64aa-4a16-ac7d-2d27cbc86c8e
```
Based on the codebase context, you're asking about the functions that generate manifest confirmation links and routes in the delivery management system. Let me trace through the key functions responsible for this.

## Answer

The manifest confirmation links and routes are generated by several functions in the `DeliveryConfirmationController` and `DeliveryController` classes:

### Confirmation Link Generation Functions

The primary functions that generate confirmation links are:

**`buildConfirmUrl()`** - Generates confirmation links for accepting deliveries: DeliveryConfirmationController.java:31-34

**`buildCancelUrl()`** - Generates cancellation links: DeliveryConfirmationController.java:36-39

**`buildDriverStatusLink()`** - Generates driver status update links: DeliveryConfirmationController.java:41-48

### Delivery Page Link Generation

The `DeliveryController` provides functions for generating delivery manifest page links:

**`buildDeliveryPageLink()`** - Creates basic delivery page URLs: DeliveryController.java:32-34

**`buildDeliveryPageLinkWithCode()`** - Creates delivery page URLs with authentication codes: DeliveryController.java:36-38

### Link Usage in Notifications

These link generation functions are used by the `NotificationStateMachine` when sending SMS notifications. For example, when requesting confirmations: NotificationStateMachine.java:52-53

The notification system calls `DeliveryController.buildDeliveryPageLink()` to create role-specific links that are included in SMS messages sent to drivers, pickup sites, and dropoff sites.

### External System Integration

The `SendDeliveryUpdate` class also generates confirmation links when sending updates to external systems like Airtable: SendDeliveryUpdate.java:62-85

This function creates confirmation links for all three roles (driver, pickup site, dropoff site) and includes them in the payload sent to external webhook endpoints.

## Notes

The confirmation link generation is centralized in the `DeliveryConfirmationController` class, while the basic delivery page links are handled by `DeliveryController`. These functions work together to create a complete set of URLs that allow different parties to access and interact with delivery manifests based on their role and the current delivery status. The links include secret codes for authentication and are distributed via SMS notifications through the `NotificationStateMachine`.

Wiki pages you might want to explore:

- [Delivery Management & Confirmation (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/3.1-delivery-management-and-confirmation)
- [Volunteer Delivery System (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/3.3-volunteer-delivery-system)
```

- "How is the delivery progress state managed client-side (step button flow)?"
https://deepwiki.com/search/where-is-the-route-matching-lo_cb33dbb0-64aa-4a16-ac7d-2d27cbc86c8e
```
You're asking about how the delivery progress state is managed client-side, specifically the step button flow in the delivery system. Based on the code context, this refers to the delivery status progression interface that drivers use to update their progress through delivery steps.

## Answer

The delivery progress state is managed client-side through the delivery page interface in `webapp/src/main/resources/public/delivery/delivery.html` and its associated JavaScript in `webapp/src/main/resources/public/delivery/delivery.js`.

### Step Button Flow Structure

The delivery page displays the current delivery status and provides action buttons based on the delivery state delivery.html:18-30 . The interface shows both the overall delivery status and driver-specific status.

The step progression is controlled through confirmation buttons that are conditionally displayed based on the current state delivery.html:31-40 . When a confirmation action is available, the system shows a confirm button with a dynamically generated URL.

### Client-Side State Management

The client-side state management works through URL-based actions rather than complex JavaScript state management. Each step in the delivery process generates a specific URL that, when clicked, advances the delivery to the next state. This is handled by the `buildDriverStatusLink()` function , which creates links that include the next status in the progression.

### Cancel/Decline Flow

The system also provides a cancel/decline workflow with a two-step confirmation process delivery.html:42-58 . The initial "CLICK TO CANCEL" button reveals a confirmation interface with an "ARE YOU SURE?" button and a text area for the cancel reason.

The JavaScript handles the toggle between the cancel button and confirmation interface through the `toggleConfirmCancel()` function, and processes the actual cancellation through `sendCancel()` with the provided URL and reason.

### Integration with Backend State

The client-side interface is tightly integrated with the backend delivery state management. The delivery page URLs are generated by `buildDeliveryPageLink()` and `buildDeliveryPageLinkWithCode()` functions , ensuring that each user sees the appropriate interface based on their role and the current delivery status.

## Notes

The delivery progress system uses a URL-driven approach rather than complex client-side state management. Each step in the delivery process is represented by a specific URL that, when accessed, updates the backend state and refreshes the page with the new status. This approach ensures consistency between client and server state while keeping the client-side logic simple and reliable.

Wiki pages you might want to explore:

- [Overview (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/1-overview)
- [Supply Site Management (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/2-supply-site-management)
- [Volunteer Delivery System (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/3.3-volunteer-delivery-system)
```

- "Where is the UI logic for site inventory editing defined (add/edit status of items)?"
https://deepwiki.com/search/where-is-the-route-matching-lo_cb33dbb0-64aa-4a16-ac7d-2d27cbc86c8e
```
You're asking about the UI logic for site inventory editing, specifically the functionality to add items and edit their status. Based on the codebase context, this refers to the inventory management system in the WNC Supply Sites platform.

## Answer

The UI logic for site inventory editing is primarily defined in the inventory management system, with the main components being:

### Frontend JavaScript Logic

The core client-side logic is in inventory.js:1-24 , which handles user interactions for toggling inventory items and changing their status.

The main functions include:

- **`toggleInventory()`** - Handles when users check/uncheck items to add/remove them from inventory inventory.js:7-18
    
- **`addItem()`** - Processes adding new items to the inventory inventory.js:213-352
    
- **`changeItemStatus()`** - Handles status changes for existing items (referenced in the HTML but implementation would be in the same file)
    

### HTML Template Structure

The user interface is defined in inventory.html:55-135 , which creates:

- A table displaying all inventory items with checkboxes for activation/deactivation
- Radio buttons for each item to set status (Urgently Needed, Needed, Available, Oversupply) inventory.html:90-131
- A form at the bottom for adding new items inventory.html:143-178

### Backend Controller Integration

The frontend calls are handled by the `InventoryController` InventoryController.java:175-198 , which provides endpoints for:

- `/manage/add-site-item` - Adding new items
- `/manage/activate-site-item` - Activating existing items InventoryController.java:200-231
- `/manage/deactivate-site-item` - Removing items from inventory
- `/manage/update-site-item-status` - Changing item status InventoryController.java:265-293

### Status Change Implementation

When users change item status via radio buttons, the JavaScript sends requests to update the backend, which then calls InventoryDao.java:122-167 to persist the changes and maintain audit trails.

## Notes

The inventory editing system uses a combination of server-side rendering (Mustache templates) for the initial page load and client-side JavaScript for dynamic interactions. The system maintains comprehensive audit trails and sends updates to external systems via webhooks when inventory changes occur. The UI is designed to be intuitive with large clickable areas and clear visual feedback for user actions.

Wiki pages you might want to explore:

- [Site Detail Pages (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/2.1-site-detail-pages)
- [Inventory Management (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/2.2-inventory-management)
- [Delivery System (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/3-delivery-system)
```

- "How is the driver Jotform data integrated into the main delivery system?"
https://deepwiki.com/search/where-is-the-route-matching-lo_cb33dbb0-64aa-4a16-ac7d-2d27cbc86c8e
```
Based on the codebase context, you're asking about how driver data from Jotform (an external form service) is integrated into the main delivery system in the WNC Supply Sites platform.

## Answer

The driver Jotform data integration occurs through a webhook-based system that receives driver information and stores it in the main database for use in the delivery system.

### Webhook Integration Entry Point

Driver data from Jotform is received via the `DriverUpdatesWebhook` controller, which provides two endpoints:

- `/webhook/driver/upsert` - Receives complete driver records DriverUpdatesWebhook.java:18-35
    
- `/webhook/driver/update-field` - Receives individual field updates DriverUpdatesWebhook.java:37-45
    

### Data Processing and Storage

When Jotform sends driver data, it's parsed into a `Driver` object using JSON deserialization Driver.java:35-37 . The driver data includes essential fields like name, phone number, location, availability, and vehicle information.

The parsed data is then stored in the database using `DriverDao.upsert()`, which handles both new driver creation and updates to existing records DriverUpdatesWebhook.java:21-33 .

### Integration with Delivery System

Once stored, the driver data becomes available throughout the delivery system:

1. **Driver Portal Access**: Drivers can access their portal using their phone number for authentication DriverController.java:42-50
    
2. **Route Volunteering**: When drivers volunteer for routes, the system looks up their information by phone number to enrich delivery requests RouteVolunteeringController.java:45-51
    
3. **Delivery Assignment**: The delivery system can fetch deliveries assigned to specific drivers using their phone numbers DriverController.java:52
    

### Registration Flow Reference

The system provides a registration page that directs potential drivers to the Jotform registration.html:27-30 , creating a complete onboarding flow from external form submission to internal system integration.

## Notes

The integration uses phone numbers as the primary identifier for matching drivers across systems. The webhook handles duplicate submissions gracefully and maintains data consistency. This architecture allows the WNC Supply Sites system to leverage Jotform's user-friendly form interface while maintaining full control over driver data within their delivery management system.

Wiki pages you might want to explore:

- [Delivery Management & Confirmation (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/3.1-delivery-management-and-confirmation)
- [Driver Portal (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/3.2-driver-portal)
- [Volunteer Delivery System (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/3.3-volunteer-delivery-system)
```

- "Where is the confirmation response captured for pickup/dropoff/driver from SMS links?"
https://deepwiki.com/search/where-is-the-route-matching-lo_cb33dbb0-64aa-4a16-ac7d-2d27cbc86c8e
```
You're asking about where the confirmation responses are captured when pickup sites, dropoff sites, and drivers click on the SMS links they receive to confirm or cancel deliveries.
Answer

The confirmation responses from SMS links are captured in the DeliveryConfirmationController class, which handles all delivery confirmation and cancellation requests through dedicated endpoints.
Main Confirmation Endpoint

The primary endpoint that captures confirmation responses is /confirm/delivery in the confirmRequest() method DeliveryConfirmationController.java:133-175 . This single endpoint handles confirmations from all three parties (driver, pickup site, dropoff site) by:

    Validating the delivery key and confirmation code - Each SMS link contains a unique delivery key and role-specific confirmation code
    Identifying the confirming party - The system matches the confirmation code against all three roles to determine who is confirming
    Recording the confirmation - Calls ConfirmationDao.confirmDelivery() to update the database with the confirmation status
    Triggering notifications - Sends SMS updates to relevant parties about the confirmation status

Cancellation Endpoint

Cancellation responses are captured at /confirm/cancel in the cancelRequest() method DeliveryConfirmationController.java:177-213 . This endpoint:

    Processes cancellation requests from any of the three parties
    Records the cancellation reason if provided
    Updates delivery status to cancelled
    Sends cancellation notifications to all parties

Driver Status Updates

For drivers specifically, there's an additional endpoint /confirm/driver that captures driver status updates during delivery execution DeliveryConfirmationController.java:56-126 . This handles the step-by-step delivery progress (en route, arrived at pickup, departed pickup, arrived at dropoff).
Link Generation and SMS Distribution

The SMS links that lead to these endpoints are generated by the NotificationStateMachine when the dispatcher initiates confirmations NotificationStateMachine.java:34-114 . Each party receives a unique link with their role-specific confirmation code embedded in the URL.
Database Storage

The confirmation responses are ultimately stored in the delivery_confirmation table through the ConfirmationDao, which tracks the confirmation status for each role (driver, pickup site, dropoff site) DeliveryDao.java:372-380 .
Notes

The system uses a unified approach where all confirmation responses flow through the same controller endpoints, with role identification happening based on the confirmation codes embedded in the SMS links. This ensures consistent handling and proper audit trails for all delivery confirmations regardless of which party is responding.

Wiki pages you might want to explore:

    Delivery Management & Confirmation (wnc-supply-sites/wnc-supply-sites)
```


- "What template is used to render the public site search/filter view?"
https://deepwiki.com/search/where-is-the-route-matching-lo_cb33dbb0-64aa-4a16-ac7d-2d27cbc86c8e
```
You're asking about the template used to render the public site search/filter view in the WNC Supply Sites system. Based on the codebase context, this refers to the supplies search page where users can filter and view supply sites.
Answer

The template used to render the public site search/filter view is supplies/supplies, which corresponds to the HTML template file supplies.html:1-316 .
Template Rendering Flow

The template is rendered through the SuppliesController class, specifically in the supplies() method SuppliesController.java:38-53 . This controller method:

    Handles GET requests to /supplies/site-list and /supplies/needs
    Sets template parameters based on the mode (donate vs view)
    Returns a ModelAndView with the template name "supplies/supplies"

Template Structure

The supplies.html template includes several key components for the search/filter interface:

    Filter controls with dropdowns for site, state, county, and item selection supplies.html:89-196
    Status checkboxes for filtering by item status (Urgently Needed, Needed, Available, Oversupply) supplies.html:197-272
    Results table that gets populated dynamically via JavaScript supplies.html:294-307

Dynamic Data Population

The template works in conjunction with JavaScript to provide dynamic filtering. The client-side logic in supplies.js:2-43 fetches filter data from /supplies/filter-data endpoint and populates the dropdown options, while the updateData() function supplies.js:220-268 handles the dynamic updating of search results.
Notes

This template serves as the main public interface for browsing supply sites and is distinct from other templates in the system like the browse routes template (browse/routes) used for driver route matching or the inventory management templates used by site managers.

Wiki pages you might want to explore:

    Supply Site Management (wnc-supply-sites/wnc-supply-sites)
    Inventory Management (wnc-supply-sites/wnc-supply-sites)
    Volunteer Delivery System (wnc-supply-sites/wnc-supply-sites)
```


- "Where are the Airtable-like views implemented or mirrored in JS/CSS/HTML?"
https://deepwiki.com/search/where-is-the-route-matching-lo_cb33dbb0-64aa-4a16-ac7d-2d27cbc86c8e
```
You're asking about where Airtable-like views are implemented in the frontend (JS/CSS/HTML) or where Airtable is referenced throughout the WNC Supply Sites codebase.
Answer

Based on the codebase context, there are no Airtable-like views implemented or mirrored in the frontend. The WNC Supply Sites system uses its own custom HTML tables and interfaces for data display, not Airtable-style grid views.

However, Airtable is extensively referenced throughout the backend for external integrations and webhooks:
Airtable Integration Configuration

The system integrates with Airtable through webhook endpoints configured in application.properties:22-25
Driver Data Integration

Airtable is heavily used for driver management. Driver data flows from Jotform → Airtable → WNC Supply Sites through webhooks:

    Driver updates are sent to Airtable via SendDriverUpdate.java:25-31
    Driver records contain airtableId fields for cross-system tracking: Driver.java:15
    Route volunteering requests include driver Airtable IDs: RouteVolunteeringController.java:48

Site Data Integration

Site information is synchronized with external systems (likely including Airtable) through the Make platform: SendSiteUpdate.java:18-20
Frontend Data Display

The actual data views in the frontend use custom HTML tables, not Airtable-style interfaces:

    The public supplies search uses a custom filter/results table: supplies.html:296-306
    Site inventory management uses custom HTML forms and tables with JavaScript:

Notes

Airtable serves as an external data coordination platform rather than a UI framework for this system. The WNC Supply Sites platform maintains its own custom frontend interfaces while using Airtable for data synchronization, driver management, and workflow automation through webhooks and the Make platform integration.

Wiki pages you might want to explore:

    Overview (wnc-supply-sites/wnc-supply-sites)
    Supply Site Management (wnc-supply-sites/wnc-supply-sites)
    External Integrations (wnc-supply-sites/wnc-supply-sites)
```

- What is the database setup?
https://deepwiki.com/search/where-is-the-route-matching-lo_cb33dbb0-64aa-4a16-ac7d-2d27cbc86c8e
```
You're asking about the database setup for the WNC Supply Sites system. Based on the codebase context, this refers to the PostgreSQL database configuration and schema used by the disaster relief supply management platform.

## Answer

The WNC Supply Sites system uses **PostgreSQL** as its primary database with a comprehensive schema for managing supply sites, inventory, deliveries, and user data.

### Database Technology Stack

The system uses PostgreSQL with JDBI for database access build.gradle:34-40 . The database connection is managed through HikariCP connection pooling.

### Database Configuration

For local development, the system requires two PostgreSQL databases to be created README.md:68-82 :

- `wnc_helene` - Main development database
- `wnc_helene_test` - Testing database

Both databases use the same user credentials (`wnc_helene` / `wnc_helene`).

### Schema Management

The database schema is managed through **Flyway migrations** located in the `schema/` directory README.md:84-99 . Migrations are automatically applied during deployment and can be run locally using the helper script `./schema/run-flyway.sh`.

### Core Database Tables

Based on the test data and DAO classes, the database includes these key tables:

**Site Management Tables:**

- `site` - Supply sites with location, contact info, and operational status
- `county` - Geographic counties with state information
- `site_type` - Site classifications (Distribution Center, Supply Hub)
- `max_supply_load` - Vehicle capacity classifications

**Inventory Tables:**

- `item` - Master list of supply items
- `item_status` - Status classifications (Urgently Needed, Needed, Available, Oversupply)
- `site_item` - Junction table linking sites to their inventory items
- `item_tag` - Item categorization tags

**Delivery Tables:**

- `delivery` - Delivery records with pickup/dropoff sites and driver info
- `delivery_confirmation` - Confirmation status for drivers and sites
- `delivery_item` - Items included in each delivery

**User Management Tables:**

- `wss_user` - System users
- `wss_user_roles` - User role assignments
- `driver` - Driver-specific information

This is evident from the test data setup TestData.sql:1-120 which shows the table structure and relationships.

### Database Access Patterns

The system uses JDBI for database access with DAO classes that handle specific data operations:

- `SuppliesDao` - Handles supply site queries and filtering SuppliesDao.java:127-177
- `SiteDetailDao` - Manages individual site data lookups SiteDetailDao.java:56-95
- `BrowseRoutesDao` - Handles delivery route matching queries BrowseRoutesDao.java:259-274

### Production Database Setup

For production deployment, the database setup involves ops.md:172-181 :

1. Creating the PostgreSQL databases
2. Setting up proper user permissions
3. Running Flyway migrations
4. Optionally seeding with production data

Database access in production is available through standard PostgreSQL tools ops.md:47-52 .

## Notes

The database design supports multi-deployment scenarios where different geographical regions (WNC, SoCal) can have separate data while sharing the same schema. The system maintains comprehensive audit trails and supports real-time inventory updates that sync with external systems like R4 and Airtable through webhooks.

Wiki pages you might want to explore:

- [Overview (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/1-overview)
- [Supply Site Management (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/2-supply-site-management)
- [External Integrations (wnc-supply-sites/wnc-supply-sites)](https://deepwiki.com/wnc-supply-sites/wnc-supply-sites/5-external-integrations)
```