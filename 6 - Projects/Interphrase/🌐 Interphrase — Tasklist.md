---
Date Created: 2025-04-23 10:58
Last Updated: 2025-04-23 10:58
tags: 
Index:
  - "[[Tasks]]"
  - "[[The ARX Index]]"
Topic: 
Status: Unweathered
Published: true
Author:
---
---

**Focus:** Contextual language replacement or auto-translation using LibreTranslate

## 🔧 Core Setup
- [x] Basic Firefox extension scaffold created
- [x] `manifest.json` configured for scripting and storage
- [x] `popup.html` for adding translation pairs + toggle for API mode
- [x] `contentScript.js` handles both local replacement and LibreTranslate
- [x] LibreTranslate integration implemented (manual & auto mode)
- [x] `README.md` documents API and usage

## 🎨 Branding & Aesthetics
- [x] Minimalist interphase-inspired icon (cell + nucleus + chromatin)
- [ ] Export icon to `.ico`, `.png`, and `.svg` for packaging
- [ ] Add icon to `manifest.json`

## 🌐 Server/Translation Enhancements
- [ ] Test live translation using LibreTranslate public endpoint
- [ ] Set up and test local LibreTranslate server
- [ ] Optionally add fallback if public API fails

## 🧠 Functionality Upgrades
- [ ] Add language auto-detection UI in popup
- [ ] Phrase-level or sentence-level translation batching
- [ ] Highlight translated words (visual feedback)

## 🧪 Testing & Polish
- [ ] Validate translations on multilingual pages
- [ ] Ensure graceful fallback for untranslated content
- [ ] Optimize MutationObserver performance
- [ ] Enable private browsing permissions
