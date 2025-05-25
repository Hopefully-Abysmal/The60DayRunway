---
Date Created: 2025-05-06 10:52
Last Updated: 2025-05-06 10:52
tags:
  - Project
Index:
  - "[[The ARX Index]]"
Topic: 
Status: Unweathered
Published: true
Author:
  - "[[ChatGPT]]"
  - "[[Landon Dahle]]"
---
Discussed in [[conversation on The Decentralized Semantic Web Mirror (DSWM)]]

---
# **DSWM Tech Stack Overview**

> _The Decentralized Semantic Web Mirror (DSWM)_ is a hybrid decentralized system for logging, verifying, and mirroring user-contributed knowledge. It includes a verifiable impact ledger, a contributor dashboard, and semantic link indexing — all while avoiding token speculation.

---

## **1. Programming Language**

- **Python 3.11**
    
    - Chosen for: rapid backend prototyping, ecosystem (FastAPI, Typer, Pydantic), and rich cryptographic + data tooling.
        
    - Core for backend logic, ledger management, Merkle hashing, CLI utilities, and snapshot anchoring.
        

---

## **2. Backend**

### **Frameworks & Libraries**

- **FastAPI**
    
    - Used to expose REST API endpoints (e.g., `/user/:id`, `/snapshot/:cycle_id`)
        
    - Auto-generates Swagger/OpenAPI docs at `/docs`
        
- **Typer**
    
    - CLI tool interface to allow admin actions (`award`, `summarize`, `cycle`, `verify`)
        
    - Uses Python decorators to auto-generate help documentation
        
- **SQLite / TinyDB**
    
    - Local prototype DB for storing:
        
        - `LedgerEntry`: hash, user_id, impact, cycle
            
        - `SnapshotBlock`: Merkle root, cycle ID, IPFS CID
            
- **Pydantic**
    
    - For schema definition, data validation, and auto-exportable JSON schema documentation
        
- **Requests**
    
    - Handles IPFS pinning + snapshot verification (via NFT.Storage, IPFS.io, etc.)
        

---

## **3. Merkle Tree + Ledger**

- Custom utility functions for:
    
    - Hash pair chaining (`sha256(a + b)`)
        
    - Merkle root generation
        
    - Inclusion proof verification
        
- Snapshot + anchoring layer signs and serializes these trees into IPFS-compatible JSON blocks
    

---

## **4. Frontend**

### **Framework**

- **React (via Vite)**
    
    - Fast hot-reloadable dev experience
        
    - Small footprint, great with static deployment
        
- **TailwindCSS**
    
    - Utility-first CSS framework for rapid UI prototyping
        
    - Used to build the Contributor Dashboard
        

### **Frontend Features**

- Fetches live API data:
    
    - `/api/user/:id` — impact summary
        
    - `/api/content/:id` — list of user contributions
        
    - `/api/snapshot/:cycle` — snapshot validation
        
- Breaks UI into modular React components:
    
    - `ImpactSummary`
        
    - `ContentList`
        
    - `SnapshotStatus`
        
- Optionally supports `.env` config (via `VITE_API_BASE`)
    

---

## **5. Deployment & Automation**

### **Build Tooling**

- **Vite** for frontend bundling
    
- **npm scripts**: `dev`, `build`, `preview`, `deploy`
    

### **Hosting Options**

- **Netlify** for instant GitHub-to-deploy workflows
    
- **GitHub Pages** for zero-cost static hosting
    

### **CI/CD**

- GitHub Actions:
    
    - Auto-runs a `generate_docs.py` script
        
    - Rebuilds CLI help, environment var lists, and Pydantic schema docs on every push to `main`
        
    - Commits results back to `/docs/`
        

---

## **6. Documentation & Dev Tooling**

- `DEPLOY.md`, `USE-CASES.md`, and `README.md` for onboarding
    
- `generate_docs.py` produces:
    
    - `cli.md`: CLI commands
        
    - `env.md`: environment vars
        
    - `schema.json`: schema of the ledger/block format
        
- **Makefile** for quick local scripts (`make docs`)
    

---

## **7. Future (Planned or Optional)**

- IPFS/Arweave snapshot anchors signed with private keys
    
- DAO/chain-ready extensions for Merkle checkpointing
    
- Vault importers for PKM integration (e.g., SCOOL compatibility)
    
- Non-speculative token accounting + reward flow
    
- Public CDN / mirror node CLI for distributed sync