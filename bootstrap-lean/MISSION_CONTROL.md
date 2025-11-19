# 🎯 Mission Control: [PROJECT_NAME]

**Last Updated:** [YYYY-MM-DD]

---

## 🚀 Project Overview

**[PROJECT_NAME]** does [BRIEF_DESCRIPTION_OF_PROJECT].

**Current Status:** [DEVELOPMENT_PHASE]
**Next Milestone:** [NEXT_GOAL]
**Tech Stack:** [BRIEF_LIST_OF_TECH]

---

## 📍 Documentation Map

All project knowledge lives in 3 places:

| Team | File | What's Inside |
|------|------|---|
| 🔧 **ENGINEERING** | `DOCS/ENGINEERING.md` | Architecture, tech stack, APIs, testing |
| 🎨 **PRODUCT** | `DOCS/PRODUCT.md` | Features, design, requirements, roadmap |
| ⚙️ **OPERATIONS** | `DOCS/OPERATIONS.md` | Deployment, monitoring, runbooks, incidents |

**Not sure where to look?** Check `DOCS_INDEX.md` for a complete registry.

---

## 🔄 Documentation Workflow

### When You Update a Document

1. **Edit the doc** (ENGINEERING.md, PRODUCT.md, etc.)
2. **Update DOCS_INDEX.md** timestamp for that file
3. **Commit together:**
   ```bash
   git add DOCS/FILENAME.md DOCS_INDEX.md
   git commit -m "[TEAM] Brief description of change"
   ```

**That's it.** No mandatory 7-step process. Keep it simple.

---

## 👥 For AI Agents

When working with Claude Code or other AI agents:

### What They Should Do

1. **Read this file first** to understand the project
2. **Check DOCS_INDEX.md** to see what docs exist
3. **Read relevant docs** from DOCS/ENGINEERING.md, PRODUCT.md, or OPERATIONS.md
4. **Make changes** to the relevant doc
5. **Update the registry** (DOCS_INDEX.md timestamp)
6. **Commit atomically** (all related changes together)

### Guidelines for AI Agents

- **Be honest** if you don't understand something. Ask the human.
- **Check for contradictions** between docs before making changes.
- **Always update the registry** when docs change.
- **Commit with clear messages** explaining what changed and why.
- **Reference related documents** when making cross-team changes.

---

## 🎯 Project-Specific Context

### Key Decisions

- [Decision 1: Why we chose X over Y]
- [Decision 2: Why we structured it this way]
- [Decision 3: Other important context]

### Important Constraints

- [Constraint 1: Regulatory, technical, or business]
- [Constraint 2: Things we must always do]
- [Constraint 3: Things we must never do]

### Critical Pathways

- **To add a feature:** Update PRODUCT.md → ENGINEERING.md → Test → Commit
- **To fix a bug:** Update ENGINEERING.md → Test → Update OPERATIONS.md if needed → Commit
- **To deploy:** Follow OPERATIONS.md → Verify monitoring → Document any issues

---

## 📊 Quick Reference

### Directory Structure

```
[PROJECT_NAME]/
├── README.md                  (Project intro)
├── MISSION_CONTROL.md         (This file - AI agent instructions)
├── DOCS_INDEX.md              (Registry of all docs)
│
├── DOCS/
│   ├── ENGINEERING.md         (Tech, architecture, APIs)
│   ├── PRODUCT.md             (Features, design, requirements)
│   └── OPERATIONS.md          (Deployment, monitoring, incidents)
│
└── [Your code/assets here]
```

### Git Conventions

**Commit message format:**
```
[TEAM] Brief description of change

Longer explanation if needed:
- What changed and why
- What docs were updated
- Any follow-up needed
```

**Examples:**
```
[ENGINEERING] Add PostgreSQL connection pooling documentation
[PRODUCT] Update feature roadmap with Q4 priorities
[OPERATIONS] Add incident response procedure for database failures
```

---

## 📋 Checklists

### When Reviewing a PR or Change

```
☐ Is the code change documented in ENGINEERING.md?
☐ If a feature changed, is PRODUCT.md updated?
☐ If deployment changed, is OPERATIONS.md updated?
☐ Is DOCS_INDEX.md timestamp updated?
☐ Do the docs contradict each other?
☐ Are there relevant cross-references?
```

### When Starting New Work

```
☐ Have I read MISSION_CONTROL.md (this file)?
☐ Have I checked DOCS_INDEX.md for related docs?
☐ Do I understand the project's current status?
☐ Do I know which doc(s) I need to update?
☐ Do I understand the git workflow?
```

### Before Committing

```
☐ All changes are documented in the relevant DOCS/ file
☐ DOCS_INDEX.md is updated with new timestamp
☐ Commit message follows [TEAM] format
☐ Related docs are checked for contradictions
☐ Links and cross-references still work
```

---

## 🚨 Common Mistakes to Avoid

| Mistake | Why It's Bad | What to Do Instead |
|---------|------------|-------------------|
| Updating a doc but not DOCS_INDEX.md | Other people don't know it was updated | Always update timestamp when you edit a doc |
| Committing doc changes without code changes | Creates doc-only commits with no substance | Keep related doc changes and code in the same commit |
| Making changes to the wrong doc | Creates duplicated/contradictory info | Check DOCS_INDEX.md first, see which doc owns this |
| Not updating related docs | Docs get out of sync | Check "Related Docs" in DOCS_INDEX.md entry |
| Long commit messages that don't explain WHY | Future you won't remember the context | Write "why" in commit message, not just "what" |

---

## 🔗 Cross-Team References

When your change affects multiple teams:

**Example:** Adding a new API endpoint

```
1. Update ENGINEERING.md with API details
2. Update PRODUCT.md if it affects user features
3. Update OPERATIONS.md if it affects monitoring/deployment
4. In DOCS_INDEX.md, add cross-references:
   - In ENGINEERING entry: "Related: PRODUCT.md, OPERATIONS.md"
   - In PRODUCT entry: "Related: ENGINEERING.md, OPERATIONS.md"
   - In OPERATIONS entry: "Related: ENGINEERING.md"
5. Commit ALL THREE files together
```

---

## 📈 How This System Works

```
    Human/AI Agent Makes Change
            ↓
    Updates Relevant DOCS/ File
            ↓
    Updates DOCS_INDEX.md Timestamp
            ↓
    Commits Both Files Together
            ↓
    Next Session Reads DOCS_INDEX.md
            ↓
    Finds Recent Changes
            ↓
    Understands Project State
```

This creates a **feedback loop** where the documentation system improves itself with every interaction.

---

## 🎓 Examples

### Example 1: Adding a New Feature

```
Task: Add user profile avatars

Step 1: Update PRODUCT.md
- Add "user avatars" to feature list
- Explain design (profile page section)

Step 2: Update ENGINEERING.md
- Add image storage service (S3/CDN)
- Add database schema changes
- Add API endpoint details

Step 3: Update OPERATIONS.md
- Add S3 bucket monitoring
- Document image caching strategy

Step 4: Update DOCS_INDEX.md timestamps

Step 5: Commit
git add DOCS/PRODUCT.md DOCS/ENGINEERING.md DOCS/OPERATIONS.md DOCS_INDEX.md
git commit -m "[PRODUCT] Add user profile avatars feature"
```

### Example 2: Fixing a Critical Bug

```
Task: Database connection timeouts

Step 1: Investigate in ENGINEERING.md
- Identify connection pool limit
- Review configuration

Step 2: Update ENGINEERING.md
- Document the fix (increase pool size)
- Explain rationale

Step 3: Update OPERATIONS.md
- Add monitoring alert for pool exhaustion
- Add troubleshooting step

Step 4: Commit
git add DOCS/ENGINEERING.md DOCS/OPERATIONS.md DOCS_INDEX.md
git commit -m "[ENGINEERING] Fix database connection timeout issue"
```

---

## ❓ Quick Questions

**Q: What if I don't know which doc to update?**
A: Check DOCS_INDEX.md, ask the team, or start a discussion. It's better to ask than guess.

**Q: What if my change affects all 3 teams?**
A: Update all 3 docs and commit them together. That's when cross-team collaboration happens.

**Q: How detailed should each doc be?**
A: Detailed enough for someone to understand *without asking*. Not so detailed it becomes outdated. Aim for clarity.

**Q: Who decides what goes in which doc?**
A: See the team definitions above. If it's still unclear, add it to the right team and ask for feedback in the next review.

---

## 🔄 Feedback Loop

This system improves itself:

```
Session 1: AI agent reads docs, finds them helpful
        ↓
Session 2: AI agent improves docs based on new context
        ↓
Session 3: New team member finds docs even more helpful
        ↓
Session 4: Another AI agent makes further improvements
        ↓
Result: Documentation gets progressively better
```

Each interaction teaches the system. That's the goal.

---

**Last reminder:** Keep docs in sync, update the registry, commit together. Everything else follows naturally.

Good luck! 🚀
