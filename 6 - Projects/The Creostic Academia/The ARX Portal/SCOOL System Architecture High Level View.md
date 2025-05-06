---
Date Created: "2025-05-05 17:58"
Last Updated: "2025-05-05 17:58"
tags:
  - Project
Index:
  - "[[The ARX Index]]"
Topic: 
Status: Unweathered
Published: true
Author:
---
---
(Using GPT for this so take with grain of salt; input [[Fast - Augment Realities eXpedition]], [[Fathom - Augment Realities eXegesis]], [[Flow - Augment Realities eXpergefaction]], [[Forge - Augment Realities eXternalization]], [[Forum - Augment Realities eXpostulations]], [[Found - Augment Realities eXcursion]], [[Frame - Augment Realities eXpurgation]], [[Free - Augment Realities eXploration]], [[Fun - Augment Realities eXtravaganza]], and the raw source code of [[The SCOOL Student Experience.canvas|The SCOOL Student Experience]])


Consolidating these into a single unified system architecture will help clarify how each portal functions, shares infrastructure, and interacts across the ecosystem.

Here’s the **SCOOL Unified Portal System Architecture**, showing:

- **Core Shared Infrastructure**
    
- **Portal-Specific Frontends**
    
- **ALT Layer (Agents)**
    
- **Cross-Portal Interoperability**
    
- **User Data Layer / Frame Integration**
    

---

## 🧠 **SCOOL System Architecture – High-Level View**

```mermaid
graph TD

%% Core Layers
A[Core Data Layer: User Data, Metadata, Impact Tracking]
B[ALT Layer: Autonomous Learning Tools]
C[Content Index & Embeds]

%% Portal Frontends
subgraph Portals
  FST[Fast: Shortform]
  FTH[Fathom: Longform]
  FRM[Frame: Reflection]
  FND[Found: Discovery]
  FLW[Flow: Focused Mode]
  FRG[Forge: Creation]
  FRM2[Forum: Discussion]
  FNE[Free: Open Browsing]
  FUN[Fun: Gamified Learning]
end

%% Relationships
A --> FRM
A --> FND
A --> FRG
A --> FST
A --> FTH
A --> FUN
A --> FLW

B --> FST
B --> FND
B --> FLW
B --> FRM

C --> FST
C --> FTH
C --> FND
C --> FNE
C --> FRG
C --> FRM2

FRM --> FRG
FRM --> FLW

FRG --> FRM2
FRG --> FTH
FRG --> FND
FRG --> FRM

FTH --> FRM
FTH --> FLW
FTH --> FST
FTH --> FRG

FND --> FST
FND --> FTH
FND --> FNE
FND --> FRM2
FND --> FRM

FST --> FLW
FST --> FRM
FST --> FRG

FLW --> FRM
FLW --> FRG

FUN --> FRM
FUN --> FRM2
FUN --> FRG

FRM2 --> FRM
FRM2 --> FRG
FRM2 --> FND
FRM2 --> FTH

FNE --> FRM
FNE --> FRG

```

---

## 🔧 Shared Subsystems & Specialization Highlights

|Layer|Description|Used Extensively In|
|---|---|---|
|**Core Data Layer**|Stores all user actions, PKM trails, skip logs, reflections, impact data|Frame, Fast, Flow|
|**ALT Layer**|Intelligent agents (e.g., Bliss) that shape experience, regulate dopamine loops, enhance reflection|Flow, Fast, Frame|
|**Content Index & Embeds**|Wraps internet content in SCOOL UX — includes licensing, metadata injection, embed hooks|Fathom, Found, Free, Forge|
|**Game Engine / Daemon**|Runtime environment, device scanner, performance mapping|Fun|
|**Thread Graph Layer**|Meta-discussion engine — links belief friction and cross-platform quotes|Forum, Found|
|**Branch View Engine**|Sacred Timeline UI — mental thread tracing|Free, Flow, Frame|

---

## 🧭 Portal Roles (in one sentence each)

- **Fast**: Bite-sized conceptual delivery with reinforcement tracking
    
- **Fathom**: Deep immersive consumption with sacred focus
    
- **Forum**: Public reasoning and belief dialogue across media
    
- **Fun**: Educational arcade with tracked learning
    
- **Free**: Open, nonlinear exploration and branch mapping
    
- **Flow**: Deep work and focus sessions with intent scaffolding
    
- **Forge**: Creation, remixing, and publishing zone
    
- **Found**: Discovery engine seeded by curiosity, guided by conversation
    
- **Frame**: Central PKM and reflection hub tying everything together
    

---

### 🧭 **User Journey Diagram (e.g. Learn → Reflect → Create)**

Best for understanding **flow and transitions** — how a learner navigates SCOOL over time.

|Stage|Portals Emphasized|Purpose|
|---|---|---|
|**Discover**|Found, Free|Curiosity & entry|
|**Learn**|Fast, Fathom, Fun|Content consumption|
|**Focus**|Flow|Deep dives & cognitive alignment|
|**Reflect**|Frame|Personal growth, journaling|
|**Create**|Forge|Remixing, publishing|
|**Discuss**|Forum|Debate, critique, ideation circulation|

✅ Ideal for visualizing **learning cycles**, **session types**, or the **semantic loop** between input → processing → output.

**User Journey Diagram in Mermaid** format that maps a typical flow through the SCOOL system — from discovery, through learning, into reflection and creation:

```mermaid
flowchart TD
    A[Start Journey] --> B[Found - Serendipity Discovery]
    B --> C[Free - Nonlinear Browsing]
    C --> D[Fast - Shortform Learning]
    C --> E[Fathom - Longform Immersion]
    C --> F[Fun - Gamified Learning]

    D --> G[Flow - Focused Session]
    E --> G
    F --> G

    G --> H[Frame - Reflection and PKM]
    H --> I[Forge - Create and Remix]
    I --> J[Forum - Public Debate and Sharing]

    J --> K[Frame - Reflect Again or Archive]
    K --> L[Loop or Exit]

    style A fill:#b8c6db,stroke:#333,stroke-width:2px
    style B fill:#dce2f0
    style C fill:#dce2f0
    style D fill:#ffd580
    style E fill:#cfe2f3
    style F fill:#e0ffe0
    style G fill:#b3e6ff
    style H fill:#f3e5f5
    style I fill:#ffe0e0
    style J fill:#fdfd96
    style K fill:#dcdcdc
    style L fill:#ffffff,stroke:#999,stroke-dasharray: 5 5
```

### 🔁 Notes:

- **Multiple entry points** are possible (e.g., straight into Found or Free).
    
- All learning modes (Fast, Fathom, Fun) **can lead into Flow** for focused deepening.
    
- **Frame is the memory mirror**, guiding future journeys or creation.
    
- **Forge and Forum** close the loop by letting the user **externalize** or **debate** what they’ve learned.
    


---

### 🧑‍🚀 **Role-Based Architecture (e.g. Student, Creator, ALT, Admin)**

Best for understanding **access layers, permissions**, and **tool affordances** per role.

|Role|Portals Primarily Used|Special Abilities|
|---|---|---|
|**Student**|Found, Fast, Fathom, Flow, Frame|Learning paths, skip history, progress metrics|
|**Creator**|Forge, Frame, Forum, Fathom|Publish, remix, build learning trails, earn impact|
|**ALT**|ALL (invisible layer)|Curate, nudge, reflect, filter, guide|
|**Admin / Curator**|Curation layer, Moderation tools, Impact Dashboard|Manage platform structure, approve content packages|


✅ Ideal for mapping **system architecture**, **data access**, and **interface specialization**.

**Mermaid diagram** showing the **role-based architecture** of SCOOL — mapping how each role interacts with the system’s portals and layers:

```mermaid
flowchart TD
    %% Roles
    A[Student] --> B1[Found]
    A --> B2[Fast]
    A --> B3[Fathom]
    A --> B4[Flow]
    A --> B5[Frame]

    C[Creator] --> B3
    C --> B5
    C --> B6[Forge]
    C --> B7[Forum]

    D[ALT Agent] --> B1
    D --> B2
    D --> B3
    D --> B4
    D --> B5
    D --> B6
    D --> B7

    E[Admin / Curator] --> B8[Curation Layer]
    E --> B9[Moderation Tools]
    E --> B10[Impact Dashboard]
    E --> B6
    E --> B7

    %% Styles
    classDef role fill:#b8c6db,stroke:#333,stroke-width:2px;
    classDef portal fill:#dce2f0,stroke:#666;
    classDef system fill:#fdfd96,stroke:#666;

    class A,C,D,E role;
    class B1,B2,B3,B4,B5,B6,B7 portal;
    class B8,B9,B10 system;
```


Note from Landon on above: Student would have access to all tools, but potentially can pull off pushing answers to forums unless known to be knowledgeable in the subject; alternatively just flag them as students but not discredit their input (there could be some cool insights!). 

**Layered system diagram** (showing databases, interface, AI layer, etc.):

```mermaid
flowchart TD
    %% Layers
    A[Data Layer: User Data, Content Index, Metadata, Logs]
    B[AI Layer: ALT Agents for personalization, feedback, intervention, analysis]
    C[Application Layer: Portals like Fast, Fathom, Flow, Found, Frame, Forge, Forum, Free, Fun]
    D[Interaction Layer: UI/UX, Gestures, Devices, Localization]
    E[Reflection & Impact Layer: Metrics, Journals, Impact Scores, Optional Tokenization]
    
    %% Flow
    A --> B
    B --> C
    C --> D
    D --> E
    E --> B
    E --> A

    %% Style
    classDef layer fill:#fdfd96,stroke:#333,stroke-width:2px;
    class A,B,C,D,E layer;
```



**data flow breakdown** for the roles (e.g. “How does a Creator’s content propagate”)?

```mermaid
flowchart TD
    %% Roles
    C[Creator]
    S[Student]
    ALT[ALT Agent]

    %% Portals
    Forge[Forge: Create Modules, Games, Lessons]
    Fun[Fun: Games Played]
    Fathom[Fathom: Longform Content Watched]
    Fast[Fast: Shortform Content Browsed]
    Flow[Flow: Focused Session]
    Forum[Forum: Discussion, Debate]
    Frame[Frame: Reflections, PKM Vault]
    Found[Found: Serendipitous Discovery]
    Free[Free: Semantic Browsing]

    %% Metadata & Impact
    Track[Tracking Layer: Interaction Logs, Completion, Retention]
    Impact[Impact Layer: Scoring, Contribution Ratings]
    Recommend[Recommendation Engine]
    
    %% Creator flow
    C --> Forge
    Forge --> Fast
    Forge --> Fathom
    Forge --> Fun
    Forge --> Forum
    Forge --> Recommend

    %% Student flow
    S --> Found
    S --> Fast
    S --> Fathom
    S --> Flow
    S --> Forum
    S --> Free
    S --> Fun
    S --> Frame

    %% Logging
    Found --> Track
    Fast --> Track
    Fathom --> Track
    Flow --> Track
    Fun --> Track
    Forum --> Track
    Free --> Track
    Frame --> Track

    %% ALT feedback
    ALT --> Recommend
    Track --> ALT
    ALT --> Flow
    ALT --> Frame
    ALT --> Forum

    %% Impact system
    Track --> Impact
    Impact --> C
    Impact --> S

    %% Optional edge: Community feedback
    Forum --> Impact

    %% Styling
    classDef role fill:#e0f7fa,stroke:#0a0a0a,stroke-width:1.5px;
    classDef portal fill:#fff9c4,stroke:#0a0a0a,stroke-width:1.5px;
    classDef system fill:#ffe0b2,stroke:#0a0a0a,stroke-width:1.5px;

    class C,S,ALT role;
    class Forge,Fast,Fathom,Flow,Forum,Frame,Found,Free,Fun portal;
    class Track,Impact,Recommend system;

```

---

