# [PROJECT_NAME] Documentation Index

**Last Updated:** [YYYY-MM-DD]
**Total Documents:** [NUMBER]

This is the **central registry** of all documentation for the [PROJECT_NAME] project. All documents are listed here with descriptions, categories, and last updated timestamps.

---

## How to Use This Index

1. **Starting a new session?** → Read this file first to see what documents exist
2. **Looking for information?** → Use the categories below to find the right document
3. **Created a new document?** → Add it to this index immediately
4. **Modified a document?** → Update its timestamp below

---

## Documentation Categories

### 📋 Core Documents ([NUMBER])

#### README.md
- **Purpose:** Project overview, quick start guide, high-level features
- **Audience:** New contributors, potential users, general public
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - What is [PROJECT_NAME]?
  - Quick start instructions
  - Links to detailed documentation
- **Related Documents:** All documents (serves as entry point)

---

#### claude.md
- **Purpose:** Instructions for AI agents working on the project, documentation maintenance workflow
- **Audience:** Claude Code and other AI assistants, human contributors maintaining docs
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Project overview & current status
  - **CRITICAL: Documentation maintenance instructions**
    - When you create a new document
    - When you modify an existing document
    - When you update claude.md itself
  - Documentation structure & cross-reference rules
  - Git workflow & commit message guidelines
  - Development workflow
  - Quality standards
  - Project-specific conventions
- **Related Documents:**
  - document-index.md (this file - must stay in sync)
  - All documents (provides maintenance guidelines)

---

#### document-index.md
- **Purpose:** Central registry of all documentation (THIS FILE)
- **Audience:** Everyone - first stop for finding documentation
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Complete list of all documents with descriptions
  - Categories and organization
  - Timestamps for tracking freshness
  - Cross-reference map
  - Document status tracking
- **Related Documents:**
  - claude.md (explains how to maintain this file)
  - All documents (listed within this file)

---

### 📐 Planning & Requirements ([NUMBER])

[Add your planning documents here following the same format]

#### REQUIREMENTS.md
- **Purpose:** [DESCRIPTION]
- **Audience:** [WHO_SHOULD_READ_THIS]
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - [SECTION_1]
  - [SECTION_2]
- **Related Documents:**
  - [DOCUMENT_NAME] ([relationship])

---

### 🏗️ Architecture & Technical ([NUMBER])

[Add your technical documents here]

#### ARCHITECTURE.md
- **Purpose:** [DESCRIPTION]
- **Audience:** [WHO_SHOULD_READ_THIS]
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - [SECTION_1]
  - [SECTION_2]
- **Related Documents:**
  - [DOCUMENT_NAME] ([relationship])

---

### 🔧 Development & Operations ([NUMBER])

[Add development/operations docs here]

---

## Future Documents (Planned)

These documents will be created as needed during development:

### 🚀 Planned Documents

#### [FUTURE_DOCUMENT_NAME.md]
- **Purpose:** [DESCRIPTION]
- **Status:** Not yet created
- **Create When:** [TRIGGER_CONDITION]
- **Should Include:**
  - [EXPECTED_CONTENT_1]
  - [EXPECTED_CONTENT_2]
  - [EXPECTED_CONTENT_3]

---

## Cross-Reference Map

This shows how documents relate to each other:

```
README.md (Entry Point)
    ├── claude.md (How to maintain docs)
    │   └── document-index.md (This file)
    │
    ├── [MAIN_CATEGORY_DOCS]
    │   ├── [SUBCATEGORY_DOC_1]
    │   └── [SUBCATEGORY_DOC_2]
    │
    └── Future Documents:
        ├── [PLANNED_DOC_1]
        └── [PLANNED_DOC_2]
```

---

## Document Status Tracking

### ✅ Complete & Up-to-Date
- README.md
- claude.md
- document-index.md
- [OTHER_COMPLETE_DOCS]

### 🚧 In Progress
- [DOCS_BEING_WORKED_ON]

### 📝 Planned
- [PLANNED_DOCS]

---

## Maintenance Checklist

When you create or modify documents, ensure:

- [ ] Document is listed in this index
- [ ] Timestamp is current (YYYY-MM-DD format)
- [ ] Description accurately reflects content
- [ ] Related documents are cross-linked
- [ ] Document category is appropriate
- [ ] Cross-reference map is updated if needed
- [ ] All changes committed atomically

---

## Document Freshness

**Recently Updated (Last 7 Days):**
- [RECENTLY_UPDATED_DOCS]

**Needs Review (>30 Days Old):**
- [DOCS_OLDER_THAN_30_DAYS]

**Stale (>90 Days Old):**
- [DOCS_OLDER_THAN_90_DAYS]

---

## Quick Navigation

**New to the project?**
→ Start with [README.md](./README.md)

**Working as an AI agent?**
→ Read [claude.md](./claude.md) for workflow instructions

**Looking for [SPECIFIC_TOPIC]?**
→ [RELEVANT_DOCUMENT.md]([./RELEVANT_DOCUMENT.md])

[Add more navigation shortcuts based on your project]

---

## Document Statistics

- **Total Documents:** [NUMBER] (current) + [NUMBER] (planned) = [TOTAL]
- **Total Words:** ~[ESTIMATE] words across all current documents
- **Documentation Coverage:** [PHASE_DESCRIPTION]

---

## Version History

**[YYYY-MM-DD]** - Initial creation
- Added core documents
- Established index structure and categories
- Created cross-reference map
- Defined maintenance checklist

**[Future updates will be listed here]**

---

## Notes

- This index should be updated **every time** a document is created, modified, or deleted
- Timestamps use YYYY-MM-DD format for consistency
- Keep descriptions concise but informative (2-3 sentences max)
- When a planned document is created, move it from "Planned" to "Complete"
- Review this index monthly to ensure all links work and descriptions are accurate

---

**This document is the source of truth for what documentation exists in this project.**
