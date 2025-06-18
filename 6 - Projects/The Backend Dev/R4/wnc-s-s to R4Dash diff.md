---
Date Created: "2025-06-17 16:21"
Last Updated: "2025-06-17 16:21"
tags: 
Index: 
Topic: 
Status: Unweathered
Published: true
Author: 
aliases:
---
---

combo of [[WNC-supply-sites featureset]] and [[R4Dash Lovable MVP Breakdown]]

## 🔍 Comparative Queries: R4Dash vs. WNC Supply Sites

This list helps determine what R4Dash MVP includes that WNC Supply Sites does not, and vice versa. These queries can be asked directly in DeepWiki to support the hybridization effort.

---

### 🧪 Phase 1 – "Does it exist?" Feature Parity Queries (Ask Both)

#### General UI/UX

- Does the system have a centralized dashboard with role-based quick actions?
    
- Are task maps with geographic markers supported?
    
- Can users search/filter tasks by keyword, skill, location, and urgency?
    
- Is there a responsive mobile-first interface?
    

#### Task Lifecycle & Assignment

- Can users create tasks? Who can?
    
- What are the task states (e.g., open → claimed → completed → verified)?
    
- Are there verification or proof submission workflows for completed tasks?
    
- Can tasks be claimed or assigned based on user roles or availability?
    

#### Role & Access Management

- How are user roles defined?
    
- Is there a distinction between coordinators, volunteers, medics, drivers, scouts, etc.?
    
- How is access controlled at the UI and API levels?
    

#### Location Services

- Is geolocation used to suggest tasks near the user?
    
- Can users search by location or radius?
    

#### Image & Proof Submission

- Can users upload images as proof of task completion?
    
- Are these images reviewed by admins or coordinators?
    

#### Gamification & Feedback

- Is there a badge/achievement system or user motivation layer?
    
- Does the system track user progress toward badges or reputation?
    

#### Admin Views

- Is there a separate view or dashboard for coordinators/admins to verify submissions?
    
- Are task queues prioritized by urgency or region?
    

#### Data Infrastructure

- Which database tables or services support task status, user roles, and geodata?
    
- Is the system integrated with any real-time data sync (e.g. React Query or similar)?
    

#### Deployment & Configuration

- Is the system multi-deployable across geographical zones?
    
- Are configuration values stored in environment variables?
    

---

### 🔍 Phase 2 – Feature Value Add Queries (Per System)

#### 💡 Ask Devin (WNC Supply Sites)

- What external systems (Airtable, Twilio, R4 Dispatch) does the current deployment rely on?
    
- What workflows are fully automated via SMS or webhook integrations?
    
- How are delivery logistics tracked and updated?
    
- Are volunteer driver flows tracked separately from site managers?
    
- Does the system support surplus redistribution between supply sites?
    
- What scalability features support multi-region deployment?
    

#### 🧠 Ask DeepWiki (R4Dash)

- How is badge activity tracked and visualized on the map?
    
- What hooks or UI components support real-time feedback for task progress?
    
- How is the profile page structured to reflect user achievement and role?
    
- Which components render differently depending on user role?
    
- How are optimistic updates managed during CRUD actions?
    
- How does the heatmap layer toggle or respond to user input?
    
- Are there any onboarding or demo flows that make development easier?
    

---

### 🧬 Phase 3 – Hybridization Guidance: What to Keep?

Ask:

- What features does R4Dash introduce that could enhance WNC workflows?
    
- What field-tested components in WNC (e.g. delivery tracking, SMS notifications) are missing in R4Dash?
    
- Which codebases have cleaner, more modular implementations for task creation, assignment, and verification?
    
- Which stack better supports low-bandwidth or offline-first UX?
    
- Are there UX patterns (e.g., role dashboards or map-first views) that are preferred by coordinators or volunteers?
    

This list enables clear mapping of MVP functionality gaps and synthesis of the most useful elements from both systems.

---

## Database Utilization Comparison: WNC Supply Sites vs. R4Dash MVP

### 🔧 Underlying Technology

|Feature|WNC Supply Sites|R4Dash MVP|
|---|---|---|
|Base DB|PostgreSQL|Supabase (PostgreSQL under the hood)|
|DB Access Layer|JDBI (Java)|React Query (JS) via Supabase JS client|
|Auth Integration|Cookie-based, manual role validation|Supabase Auth (email/password, auto role attach)|
|ORM/Query Style|SQL via DAO classes|Supabase client w/ typed hooks and filters|

---

### 📚 Schema & Domain Modeling

|Domain Area|WNC Supply Sites|R4Dash MVP|
|---|---|---|
|Sites/Tasks|Supply site focus (distribution, inventory)|Task focus (volunteer-driven, completion flows)|
|User Roles|wss_user_roles table (custom enum + DAO filter)|Profiles table (auto role on sign-up)|
|Inventory Tracking|Detailed: site_item, item_status, item_tag|Not tracked (task metadata only)|
|Delivery Tracking|Yes: delivery, delivery_item, confirmations|No delivery system|
|Task Lifecycle|Delivery-centric|open → claimed → completed → verified + flagged|
|Gamification|N/A|Badges, progress views|

---

### 🧩 Relationships & Structure

|Feature|WNC Supply Sites|R4Dash MVP|
|---|---|---|
|Foreign Keys|Traditional FKs + JDBI enforcement|Enforced via Supabase + TypeScript types|
|Schema Migrations|Flyway SQL-based|Supabase auto-generation + manual SQL|
|Data Seeding|Manual SQL + dev scripts|AutoSeed hooks, sample data loader|
|Deployment Split|prod/staging with region-based DB instances|Multi-project Supabase config (not yet multi-region)|

---

### 🔐 Authentication & Permissions

|Feature|WNC Supply Sites|R4Dash MVP|
|---|---|---|
|Login Flow|Cookie check + secret validation|Supabase Auth (built-in session + OAuth ready)|
|Role Enforcement|Java Interceptors, role table|React role context, table-backed|
|RLS (Row Level Security)|Manual via Java DAOs|Supabase RLS policies + helper functions|

---

### 🎯 Access Pattern Differences

|Pattern Type|WNC Supply Sites|R4Dash MVP|
|---|---|---|
|Querying|DAO methods per use case|Hooks: `useTasks`, `useOpenTasks`, etc.|
|Mutations|DAO updates via JDBI|Typed hook mutations w/ React Query|
|Sync Strategy|Manual DB sync + webhook integrations|Realtime/Live sync via Supabase + optimistic UI|

---

### 🚀 Summary

**WNC Supply Sites** prioritizes a robust, modular PostgreSQL schema with clear DAOs, external system integration (e.g., R4, Airtable), and traditional backend control via Java. Its delivery and inventory handling is deeply integrated.

**R4Dash MVP** leverages Supabase for a low-friction modern stack, excelling in rapid development, role-based frontend logic, built-in auth, and gamification via a tight task lifecycle. It trades deep inventory/delivery modeling for speed, extensibility, and usability.

### ✅ Takeaway for Hybrid Design

**Keep from WNC:**

- Detailed delivery + inventory schema
    
- Webhook-compatible architecture
    
- DAO-style separation for business logic
    

**Keep from R4Dash:**

- Supabase auth and session management
    
- Task lifecycle model and role-based access
    
- Realtime syncing and React Query integration
    
- Badge and gamification system
    

Combined, this enables a platform with operational depth _and_ modern agility.