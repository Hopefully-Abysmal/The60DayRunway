---
Date Created: 2025-06-17 16:04
Last Updated: 2025-06-17 16:04
tags: 
Index: 
Topic: 
Status: Unweathered
Published: true
Author:
  - "[[Landon Dahle]]"
aliases:
---

---
To be compared to [[WNC-supply-sites featureset]] to make [[wnc-s-s to R4Dash diff]]
## Live Links:
https://preview--r4dash-frontend-mvp.lovable.app/
https://github.com/The-ARX-Foundation/r4dash-frontend-mvp
https://deepwiki.com/The-ARX-Foundation/r4dash-frontend-mvp

## R4Dash - Comprehensive Feature List 

### 🧭 Dashboard & Navigation

- **Description:** Central hub showing role-based quick actions, coordinator tools, and user welcome with role badges
    
- **Tech Used:** `<Index />` page, React Router, `useMockAuth` & `useMockRole` hooks, Lucide icons (Plus, Search, User, MapPin)
    

### 🗺️ Interactive Task Map

- **Description:** Real-time map displaying tasks as color-coded pins with hover tooltips and click navigation to details
    
- **Tech Used:** `<TaskMap />`, Mapbox GL JS, `useMapTasks` hook, `<TaskHoverTooltip />`, Mapbox token via Supabase Edge Function
    

### 🔍 Task Browser & Search

- **Description:** Filterable grid view of available tasks with search, location filtering, and sorting capabilities
    
- **Tech Used:** `<TaskBrowser />`, `<TaskFilters />`, `useMockTasks` hook, React Query, date-fns formatting
    

### 🛠️ Task Management System

- **Description:** Complete CRUD operations for tasks including creation, claiming, completion, and verification workflows
    
- **Tech Used:** `tasks` table, `useTasks` hooks, Supabase client
    

### 🎯 Advanced Map Filtering

- **Description:** Radius search, urgency filtering, skill-based matching, location autocomplete
    
- **Tech Used:** `<MapFilters />`, `useMapboxGeocoding`, Mapbox Geocoding API, Slider and Checkbox components
    

### 🧾 Admin Task Queue

- **Description:** Coordinator interface for reviewing completed tasks with image proofs
    
- **Tech Used:** `<AdminTaskQueue />`, `usePendingTasks`, image utilities, role-based permissions
    

### 🏅 Badge & Achievement System

- **Description:** Earned/available badge display with progress tracking and gamification
    
- **Tech Used:** `badges`, `user_badges`, `user_badge_progress` tables, `<BadgeGrid />`, `<BadgeCard />`, `useBadges` hooks
    

### 👤 User Profile Management

- **Description:** Profile display with role-based data, permissions, and achievements
    
- **Tech Used:** `<Profile />` page, `profiles` table, conditional components
    

### 🧩 Role-Based Access Control

- **Description:** Permission system for volunteers, coordinators, medics, etc.
    
- **Tech Used:** `user_role` enum, `get_user_role()`, `has_role()`, `useRole`, conditional rendering
    

### 📄 Task Detail Views

- **Description:** Modal overlays with task info, images, locations, and actions
    
- **Tech Used:** `<TaskDetailsModal />`, `<TaskDetail />`, React Router, image uploads
    

### 📍 Location Services

- **Description:** GPS detection, manual search, fallback geolocation
    
- **Tech Used:** Geolocation API, Mapbox Geocoding, coordinate fallback
    

### 🖼️ Image Upload & Proof

- **Description:** Upload image evidence for completed tasks
    
- **Tech Used:** `imageUpload.ts`, `getImageUrl()`, Supabase storage, preview components
    

### 🔄 Real-time Data Management

- **Description:** Background syncing and cache invalidation
    
- **Tech Used:** React Query, Supabase, optimistic updates, error handling
    

### 📱 Mobile-First Responsive Design

- **Description:** Touch-friendly layouts, bottom nav, gesture-optimized
    
- **Tech Used:** Tailwind CSS, `<Navigation />`, responsive grids
    

### 🔐 Authentication System

- **Description:** Email/password auth, session tracking, new user triggers
    
- **Tech Used:** Supabase Auth, `<AuthPage />`, `handle_new_user()` trigger, `<ProtectedRoute />`
    

### 🧠 About & Branding

- **Description:** Mission/vision pages and platform context
    
- **Tech Used:** `<About />`, R4Dash branding, responsive design
    

### 🧮 Task Status Workflow

- **Description:** Lifecycle: open → claimed → completed → pending → verified
    
- **Tech Used:** `task_status` enum, transitions, validation functions
    

### 🌡️ Heatmap Visualization

- **Description:** Map overlay of badge activity/engagement
    
- **Tech Used:** `useBadgeHeatmap`, Mapbox heatmap, toggle UI
    

### 🔎 Search & Discovery

- **Description:** Search/filter/sort tasks by keywords, distance, tags
    
- **Tech Used:** Search algorithms, sort utils, location math
    

### 🧪 Mock Data System

- **Description:** Preloaded demo data (e.g. Texas A&M)
    
- **Tech Used:** `useMockData`, College Station coordinates, fake profiles
    

---

### 🗄️ Database Architecture

- **Core Tables:** `tasks`, `profiles`, `badges`, `user_badges`, `user_badge_progress`
    
- **Security:** RLS policies, user role functions, permission validation
    
- **Functions:** `handle_new_user()`, `get_user_role()`, `has_role()`, `is_admin()`
    

### 🌐 External Integrations

- **Mapbox:** Maps, geocoding, location services
    
- **Supabase:** Auth, DB, storage, edge functions, real-time sync
    

---

### 📘 DeepWiki-Indexed Overview (Devin Reference)

- **Feature Capabilities:**
    
    - Task Creation (`/create-task` → `TaskCreatePage`)
        
    - Task Discovery (`/browse-tasks` → `TaskBrowserPage`)
        
    - Task Completion (`/complete-tasks` → `TaskCompletionPage`)
        
    - Admin Queue Review (`/admin/tasks` → `AdminTaskQueuePage`)
        
    - Profile Management (`/profile` → `ProfilePage`)
        
    - Interactive Map View (`/map` → `MapViewPage`)
        
- **Auth & Role Logic:**
    
    - `useMockAuth()`, `useMockRole()` for dev
        
    - Role-controlled UI exposure
        
- **Component Routing:** BrowserRouter and React Router with role-gated `<Index />` hub
    
- **Project Structure:**
    
    - `/components/ui/`: shared shadcn UI components
        
    - `/hooks/`: data and role accessors
        
    - `/pages/`: route components
        
    - `/lib/`: utility logic
        
    - `/types/`: TS schemas
        

---

This feature set positions **R4Dash** as a production-ready volunteer coordination and community engagement platform—ideal for deployment by WNC and transition into `r4dash.disastersupplysites.org`.

---

# DeepWiki Questions

- What is the database setup?
https://deepwiki.com/search/what-is-the-database-setup-for_a666b757-5134-4932-992e-0c43546ab1f7
```
The database setup for this R4Dash application uses **Supabase** as the backend database with a PostgreSQL foundation. Based on the codebase, here's the comprehensive database architecture:

## Database Connection & Client

The application connects to Supabase through a centralized client configuration and uses React Query for data management useTasks.tsx:2-3 .

## Core Database Tables

### Tasks Table

The primary `tasks` table stores all task-related data with these key fields types.ts:80-103 :

- **Identity**: `id`, `user_id`, `volunteer_id`, `claimed_by`, `verified_by`
- **Content**: `title`, `description`, `location`, `image_url`
- **Geography**: `latitude`, `longitude`
- **Status Management**: `status` (enum: open, claimed, completed, pending, verified, flagged)
- **Timestamps**: `created_at`, `claimed_at`, `submitted_at`, `verified_at`
- **Metadata**: `urgency`, `skill_tags`, `medical_priority`, `wellness_check`, `verified`

### Profiles Table

User profile management types.ts:45-53 :

- Links to Supabase auth via `user_id`
- Stores `name`, `role` (enum: coordinator, scout, medic, communicator, volunteer)
- Auto-created with default 'volunteer' role AuthContext.tsx:58-66

### Badge System Tables

- **badges**: Badge definitions with criteria types.ts:12-22
- **user_badges**: Junction table for earned badges types.ts:174-179
- **user_badge_progress**: View combining badge progress data types.ts:218-233

## Data Access Patterns

The application uses React Query hooks for all database operations:

**Query Operations** useTasks.tsx:6-30 :

- `useUserTasks`: Fetches tasks where user is creator, volunteer, or claimer
- `useOpenTasks`: Gets available tasks (status: 'open' or 'verified')
- `usePendingTasks`: Admin view of completed tasks awaiting review

**Mutation Operations** useTasks.tsx:89-122 :

- `useTaskCreation`: Inserts new tasks with status 'open'
- `useTaskClaim`: Updates task status to 'claimed'
- `useTaskCompletion`: Updates with completion proof and status 'completed'
- `useTaskVerification`: Admin approval/rejection

## Database Relationships

The schema includes foreign key relationships types.ts:150-172 :

- Tasks link to users via `user_id`, `volunteer_id`, `verified_by`
- All user references connect to the `user_badge_progress` view
- Profiles have one-to-one relationship with auth users

## Sample Data & Seeding

The system includes automated sample data creation useAutoSeed.tsx:202-205 and manual seeding capabilities SampleDataCreator.tsx:101 for development and testing.

**Notes**

The database uses Supabase's built-in authentication system integrated with custom profile management. The task lifecycle is managed through status enums with proper state transitions enforced at the application level. Badge progress is calculated through database views rather than stored procedures, providing real-time gamification metrics.

Wiki pages you might want to explore:

- [Task Management System (The-ARX-Foundation/r4dash-frontend-mvp)](https://deepwiki.com/The-ARX-Foundation/r4dash-frontend-mvp/3-task-management-system)
- [Task Data Management (The-ARX-Foundation/r4dash-frontend-mvp)](https://deepwiki.com/The-ARX-Foundation/r4dash-frontend-mvp/3.2-task-data-management)
```