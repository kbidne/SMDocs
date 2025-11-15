# SMDocs Documentation Index

**Last Updated:** 2025-11-15
**Total Documents:** 3

This is the **central registry** of all documentation for the SMDocs (Self-Maintaining Documents) project. All documents are listed here with descriptions, categories, and last updated timestamps.

---

## How to Use This Index

1. **Starting a new session?** → Read this file first to see what documents exist
2. **Looking for information?** → Use the categories below to find the right document
3. **Created a new document?** → Add it to this index immediately
4. **Modified a document?** → Update its timestamp below

---

## Documentation Categories

### 📋 Bootstrap Templates (3)

These are the core templates that users copy to their own projects.

#### README.md
- **Purpose:** Comprehensive guide for using the SMDocs bootstrap system in any project
- **Audience:** Developers setting up self-documenting projects, AI agents implementing the system
- **Last Updated:** 2025-11-15
- **Key Sections:**
  - What's included in the bootstrap system
  - Why use this self-documenting approach
  - Step-by-step bootstrap instructions
  - Core principles (sync, cross-references, central registry)
  - Daily usage patterns
  - Best practices and success metrics
  - Advanced customization options
  - Real-world example from domideas project
  - Troubleshooting common issues
- **Related Documents:**
  - claude.md (template for AI instructions)
  - document-index.md (template for doc registry)

---

#### claude.md
- **Purpose:** Template for AI agent instructions and documentation maintenance workflow
- **Audience:** AI agents (Claude Code, etc.), developers customizing for their projects
- **Last Updated:** 2025-11-15
- **Key Sections:**
  - Project overview section (customizable placeholder)
  - **CRITICAL: Documentation maintenance instructions**
    - Mandatory steps when creating documents
    - Mandatory steps when modifying documents
    - Mandatory steps when updating claude.md itself
  - Documentation structure and cross-reference rules
  - Git workflow and commit message guidelines
  - Development workflow templates
  - Code organization instructions
  - AI-specific instructions for context management
  - Quality standards and success criteria
  - Common tasks quick reference
  - Troubleshooting guide
  - Project-specific conventions (customizable)
- **Related Documents:**
  - document-index.md (must stay in sync)
  - README.md (explains how to use this template)

---

#### document-index.md
- **Purpose:** Template for central documentation registry (THIS FILE when customized)
- **Audience:** Everyone - serves as single source of truth for documentation
- **Last Updated:** 2025-11-15
- **Key Sections:**
  - Complete document listing with descriptions
  - Customizable categories for different doc types
  - Timestamp tracking for freshness monitoring
  - Cross-reference map visualization
  - Document status tracking (complete/in-progress/planned)
  - Maintenance checklist
  - Document freshness indicators
  - Quick navigation shortcuts
  - Document statistics
  - Version history
- **Related Documents:**
  - claude.md (explains how to maintain this registry)
  - README.md (explains how to customize this template)

---

## Future Documents (Planned)

Potential additions to the SMDocs bootstrap system:

### 🚀 Planned Documents

#### EXAMPLES.md
- **Purpose:** Real-world examples of projects using the SMDocs system
- **Status:** Not yet created
- **Create When:** Multiple projects have adopted the system
- **Should Include:**
  - Case studies from different project types
  - Before/after documentation comparisons
  - Lessons learned from implementations
  - Common customization patterns

#### CONTRIBUTING.md
- **Purpose:** Guidelines for contributing to the SMDocs project itself
- **Status:** Not yet created
- **Create When:** Opening to external contributors
- **Should Include:**
  - How to improve templates
  - How to submit template variations
  - Code of conduct
  - PR guidelines for documentation improvements

#### CHANGELOG.md
- **Purpose:** Track versions and improvements to the bootstrap system
- **Status:** Not yet created
- **Create When:** First major revision to templates
- **Should Include:**
  - Version numbers for template releases
  - Template improvements and bug fixes
  - Breaking changes to template structure
  - Migration guides for existing users

---

## Cross-Reference Map

This shows how documents relate to each other:

```
README.md (Bootstrap Usage Guide - Entry Point)
    ├── Explains how to use templates ──┐
    │                                   │
    ├── claude.md (AI Instructions Template)
    │   └── References document-index.md for doc tracking
    │
    └── document-index.md (Doc Registry Template - This File)
        └── References claude.md for maintenance workflow

Future Documents:
    ├── EXAMPLES.md (Real-world case studies)
    ├── CONTRIBUTING.md (How to improve templates)
    └── CHANGELOG.md (Version history)
```

---

## Document Status Tracking

### ✅ Complete & Up-to-Date
- README.md (Bootstrap usage guide)
- claude.md (AI instructions template)
- document-index.md (Doc registry template)

### 🚧 In Progress
- (None currently)

### 📝 Planned
- EXAMPLES.md (Real-world case studies)
- CONTRIBUTING.md (Contribution guidelines)
- CHANGELOG.md (Version history)

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
- README.md (2025-11-15)
- claude.md (2025-11-15)
- document-index.md (2025-11-15)

**Needs Review (>30 Days Old):**
- (None - all documents created today)

**Stale (>90 Days Old):**
- (None - all documents created today)

---

## Quick Navigation

**Want to bootstrap a new project?**
→ Start with [README.md](./README.md) for complete instructions

**Need the AI instructions template?**
→ Copy [claude.md](./claude.md) to your project and customize

**Need the doc registry template?**
→ Copy [document-index.md](./document-index.md) to your project and customize

**Working on SMDocs itself?**
→ This file (document-index.md) tracks the bootstrap templates

**Want to see a real example?**
→ Check the domideas project referenced in README.md

---

## Document Statistics

- **Total Documents:** 3 (current) + 3 (planned) = 6 total
- **Total Words:** ~4,500 words across all current documents
- **Documentation Coverage:** Bootstrap templates complete and ready for use
- **Template Files:** 2 customizable templates (claude.md, document-index.md)
- **Guide Files:** 1 comprehensive usage guide (README.md)

---

## Version History

**2025-11-15** - Initial creation
- Created bootstrap template system
- Added README.md (usage guide)
- Added claude.md (AI instructions template)
- Added document-index.md (doc registry template)
- Established SMDocs project structure
- Customized document-index.md for the SMDocs project itself
- Defined planned future documents (EXAMPLES, CONTRIBUTING, CHANGELOG)

**[Future updates will be listed here]**

---

## Notes

**About SMDocs (this project):**
- SMDocs is the bootstrap template repository
- Users copy templates FROM this repo TO their own projects
- This document-index.md file itself is both a template AND the registry for SMDocs

**Maintenance:**
- This index should be updated **every time** a document is created, modified, or deleted
- Timestamps use YYYY-MM-DD format for consistency
- Keep descriptions concise but informative (2-3 sentences max)
- When a planned document is created, move it from "Planned" to "Complete"
- Review this index monthly to ensure all links work and descriptions are accurate

**For Template Users:**
- Copy claude.md and document-index.md to your project
- Customize all [BRACKETED] placeholders
- Follow the process described in README.md

---

**This document is the source of truth for what documentation exists in the SMDocs project.**
