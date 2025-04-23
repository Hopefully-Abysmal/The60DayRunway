---
Date Created: 2025-04-23 12:10
Last Updated: 2025-04-23 12:10
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

Want to use cursor but don't want to pay for the pro pro mode with unlimited shit; thought I'll just optimize the fuck out of project planning to get to the point that I just upload a github issues list esque plan and let it go ham.

Converstion prompting this: [[Architecture Planning]]

[[ChatGPT]] Reformatting of all of that: 

**Canvas Title: Obsidian-to-GitHub Issue Automation Pipeline**

---

### ✨ Vision:

Automate the entire junior-to-senior dev planning process by parsing Obsidian vault content into GitHub-style project boards, issues, sub-issues, blockers, and task contexts. All locally powered by LLMs (e.g. Phi via Ollama) and structured to be human-readable, resumable, and check-pointable at every stage.

---

### 🏠 Architecture Overview:

**Pipeline Steps:**

1. **Write Vault Content**
    
    - Use bullet points and headers in Obsidian to distinguish:
        
        - Projects vs Features
            
        - Tasks vs Motivations
            
        - Qualities (desired outcomes)
            
2. **Consolidate Vault**
    
    - Combine all notes into a single master `.md` document.
        
    - Output: `Consolidated_Notes.md`
        
3. **Parse Structure**
    
    - Create hierarchy-aware tree from `# Headers`, `## Subsections`, and bullet points.
        
    - Output:
        
        - `structure.json` → machine-usable hierarchy
            
        - `structure_visual.md` → human-readable outline
            
        - Folder tree with:
            
            - One folder per issue
                
            - Parent/sub-issue hierarchy reflected in folders
                
            - Each folder includes: `issue.md` and `issue.json`
                
            - Path length under 260 characters (Windows limit)
                
            - Root path: `D:\Artificing\Coding\60DRW\Plan`
                
4. **Semantic Classification**
    
    - Determine type: `Task`, `Quality`, or `Motivation` using local LLM.
        
    - Route snippets accordingly for task planning or documentation enrichment.
        
5. **Fuzzy Search + Routing**
    
    - Fuzzy match each snippet to existing issues/projects.
        
    - Attach to appropriate note or create a new one.
        
    - Track matched/used snippets to avoid reprocessing.
        
6. **Issue Expansion**
    
    - Parse bullet nesting for sub-issues.
        
    - Determine temporality/ordering via LLM (e.g. "what must come before what?").
        
    - Restructure if necessary (flip parent and sub-task).
        
7. **Blocker Detection**
    
    - NLP scan of each issue to find blockers.
        
    - Fuzzy match against known issues to auto-link.
        
8. **Export for GitHub**
    
    - JSON export of structured issues:
        
        ```json
        {
          "repository": "ProjectName",
          "issue_title": "Implement Context Parser",
          "assignees": ["ai:phi"],
          "status": "Todo",
          "milestone": "MVP",
          "labels": ["automation", "llm"],
          "parent_issue": null,
          "sub_issues": ["Tokenize Markdown", "Detect nesting"],
          "linked_prs": []
        }
        ```
        
9. **Optional GitHub Upload**
    
    - Use REST or GraphQL API to post issues to GitHub.
        
    - For local-first dev, maintain Obsidian-linked local JSON instead.
        
10. **Snapshot + Resume**
    

- At every stage:
    
    - Save state (JSON + human-readable `.md`)
        
    - Track snippets in-use
        
    - All issue content lives in its own folder:
        
        - `D:\Artificing\Coding\60DRW\Plan\<issue-subpath>\issue.md`
            
        - Includes full context + classification + LLM output cache
            
        - Makes resuming or re-parsing trivial
            

---

### 🚀 Core Tools Used:

- `Python`
    
- `fuzzywuzzy`, `nltk`
    
- `Ollama` + `phi` model
    
- `mistune` or `markdown-it-py` for parsing
    
- `json`, `yaml`, `markdown` for data interchange
    

---

### 🧰 Output Folders:

- `/consolidated/` → `Consolidated_Notes.md`
    
- `/structure/` → `structure.json`, `structure_visual.md`, `D:\Artificing\Coding\60DRW\Plan\...`
    
- `/tasks/` → individual issue `.md` files (during dev)
    
- `/snapshots/` → live snapshot folders (one per issue, nested hierarchy)
    
- `/export/` → `issues_export.json` for GitHub API
    

---

### 🤖 Goal:

Build a fully transparent, self-refining AI pipeline that documents and scaffolds projects the way a senior dev would—directly from raw thinking and notes.

Everything from MVP planning to detailed issue creation to task dependency mapping—all from bullet points and headers.

---

Next: Implementing `parse_structure.py` to generate the folder hierarchy + outputs.