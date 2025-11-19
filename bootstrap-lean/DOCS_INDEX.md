# 📑 Documentation Index for [PROJECT_NAME]

**Last Updated:** [YYYY-MM-DD]

---

## 📖 What This Is

Central registry of **all project documentation**. When you want to know:
- ❓ What docs exist?
- 📅 Which ones are fresh vs. stale?
- 🔗 How do they relate to each other?
- 👤 Who should read what?

You come here.

---

## 🗂️ Documentation Overview

**Total Documents:** 3 core docs + [YOUR_NUMBER] custom docs
**Last Full Review:** [YYYY-MM-DD]
**Health Status:** ✅ All current (within 30 days)

---

## 🔧 ENGINEERING Documentation

### DOCS/ENGINEERING.md
**Purpose:** Technical architecture, how the system works, APIs, tech choices
**Last Updated:** [YYYY-MM-DD]
**Freshness:** ✅ Recent (0-7 days) / ⚠️ Aging (8-30 days) / 🔴 Stale (30+ days)
**Owner:** [YOUR_ENGINEER]
**Related Docs:**
- PRODUCT.md (features we're building)
- OPERATIONS.md (how we deploy/monitor)

**Contains:**
- [ ] System architecture diagram or description
- [ ] Technology stack with versions
- [ ] API endpoints or interface contracts
- [ ] Database schema overview
- [ ] Testing strategy
- [ ] Code organization and key files
- [ ] Common troubleshooting steps

**Read This If:** You need to understand how the system works, want to contribute code, or need API details.

---

### Add More Engineering Docs Here (Optional)

If you split ENGINEERING.md into smaller files, register them:

```
DOCS/ENGINEERING/ARCHITECTURE.md
DOCS/ENGINEERING/API_REFERENCE.md
DOCS/ENGINEERING/TESTING.md
```

Just follow the same template for each.

---

## 🎨 PRODUCT Documentation

### DOCS/PRODUCT.md
**Purpose:** What we're building, why, feature list, user workflows, roadmap
**Last Updated:** [YYYY-MM-DD]
**Freshness:** ✅ Recent / ⚠️ Aging / 🔴 Stale
**Owner:** [YOUR_PRODUCT_PERSON]
**Related Docs:**
- ENGINEERING.md (how we build it)
- OPERATIONS.md (what do we run)

**Contains:**
- [ ] Feature list (current + planned)
- [ ] Product roadmap or priorities
- [ ] User workflows or personas
- [ ] Key product decisions
- [ ] Design system or UI guidelines
- [ ] Requirements or acceptance criteria

**Read This If:** You need to understand what we're building, why features exist, or what the product does.

---

### Add More Product Docs Here (Optional)

```
DOCS/PRODUCT/REQUIREMENTS.md
DOCS/PRODUCT/DESIGN_SYSTEM.md
DOCS/PRODUCT/ROADMAP.md
```

---

## ⚙️ OPERATIONS Documentation

### DOCS/OPERATIONS.md
**Purpose:** How we deploy, run, monitor, and respond to incidents
**Last Updated:** [YYYY-MM-DD]
**Freshness:** ✅ Recent / ⚠️ Aging / 🔴 Stale
**Owner:** [YOUR_OPS_PERSON]
**Related Docs:**
- ENGINEERING.md (what are we deploying)
- PRODUCT.md (what features do users see)

**Contains:**
- [ ] Deployment procedures
- [ ] Infrastructure overview
- [ ] Monitoring and alerting setup
- [ ] Incident response procedures
- [ ] Operational runbooks
- [ ] Troubleshooting guide
- [ ] Backup and recovery procedures

**Read This If:** You need to deploy, monitor, fix production issues, or understand how the system runs.

---

### Add More Operations Docs Here (Optional)

```
DOCS/OPERATIONS/DEPLOYMENT.md
DOCS/OPERATIONS/MONITORING.md
DOCS/OPERATIONS/INCIDENTS.md
DOCS/OPERATIONS/RUNBOOK.md
```

---

## 📋 Project Meta Documentation

### MISSION_CONTROL.md
**Purpose:** AI agent instructions, project overview, workflow guidelines
**Last Updated:** [YYYY-MM-DD]
**Freshness:** ✅ Recent / ⚠️ Aging / 🔴 Stale
**Owner:** [PROJECT_LEAD]
**Related Docs:** Links to all other docs
**Contains:**
- Project overview and current status
- Documentation map
- Workflow instructions for AI agents
- Key decisions and constraints
- Git conventions
- Checklists for reviews and commits

**Read This If:** You're new to the project, working with AI agents, or need to understand how we do things.

---

### README.md
**Purpose:** Project introduction, quick start, getting started guide
**Last Updated:** [YYYY-MM-DD]
**Freshness:** ✅ Recent / ⚠️ Aging / 🔴 Stale
**Owner:** [YOUR_NAME]
**Related Docs:** Links to MISSION_CONTROL.md and all team docs

**Read This If:** You're completely new and want the 2-minute overview.

---

### DOCS_INDEX.md (This File)
**Purpose:** Registry of all documentation, what each contains, freshness status
**Last Updated:** [YYYY-MM-DD]
**Freshness:** ✅ Recent / ⚠️ Aging / 🔴 Stale
**Owner:** [PROJECT_LEAD]

**Read This If:** You want to know what docs exist or what to read next.

---

## 🆕 Custom Documentation

Add any additional docs your project needs:

### Template

```
### [YOUR_DOC_NAME]
**Purpose:** [One sentence on what this doc covers]
**Last Updated:** [YYYY-MM-DD]
**Freshness:** ✅ Recent / ⚠️ Aging / 🔴 Stale
**Owner:** [WHO_MAINTAINS_THIS]
**Related Docs:** [Links to 2-3 related docs]
**Contains:**
- [ ] Item 1
- [ ] Item 2
- [ ] Item 3

**Read This If:** [When would someone need to read this?]
```

---

## 🚨 Freshness Tracker

**How old are our docs?**

| Document | Last Updated | Age | Status |
|----------|--------------|-----|--------|
| ENGINEERING.md | [DATE] | [DAYS] days | ✅ Fresh |
| PRODUCT.md | [DATE] | [DAYS] days | ✅ Fresh |
| OPERATIONS.md | [DATE] | [DAYS] days | ✅ Fresh |
| MISSION_CONTROL.md | [DATE] | [DAYS] days | ✅ Fresh |
| README.md | [DATE] | [DAYS] days | ✅ Fresh |

**Legend:**
- ✅ Fresh: 0-7 days (actively maintained)
- ⚠️ Aging: 8-30 days (review soon)
- 🔴 Stale: 30+ days (needs update)

---

## 📊 Quick Facts

```
Total Documents:        5 (3 core + 2 meta)
Total Lines:            ~1000
Average Doc Age:        [X] days
Last Full Review:       [YYYY-MM-DD]
Broken Links Found:     0
Missing Cross-Refs:     0
```

---

## 🔄 How This Registry Works

### When You Update a Doc

1. **Make your change** to the doc
2. **Update this registry** with new date:
   ```
   DOCS/ENGINEERING.md
   **Last Updated:** [TODAY'S DATE]
   **Freshness:** ✅ Recent (0-7 days)
   ```
3. **Commit both together:**
   ```bash
   git commit -m "[TEAM] Updated docs"
   ```

### When You Review Docs

Look at the "Freshness" column:
- ✅ Fresh = Good, keep using
- ⚠️ Aging = Review soon to confirm still accurate
- 🔴 Stale = Read through and update

---

## 💡 Navigation Guide

**Scenario: You're new and want to understand the project**
1. Read: README.md (2 min)
2. Read: MISSION_CONTROL.md (5 min)
3. Skim: DOCS_INDEX.md (2 min, this file)
4. Read: PRODUCT.md (5 min) - understand what we build
5. Read: ENGINEERING.md (10 min) - understand how we build it
6. Skim: OPERATIONS.md (5 min) - understand how we run it

**Total: 30 minutes to full context**

---

**Scenario: You're changing a specific feature**
1. Check: Which doc owns this? (Usually PRODUCT.md or ENGINEERING.md)
2. Read: That doc
3. Check: What else is affected? (DOCS_INDEX.md "Related Docs")
4. Read: Related docs
5. Update: All affected docs
6. Commit: Together

---

**Scenario: You're deploying or fixing production**
1. Read: OPERATIONS.md immediately
2. Check: ENGINEERING.md for details if needed
3. Update: OPERATIONS.md with what you learned
4. Commit: Updated OPERATIONS.md

---

## 🔍 Finding What You Need

**By Question:**

| Question | Answer | Document |
|----------|--------|----------|
| What does this project do? | Feature list, description | PRODUCT.md |
| How does it work? | Architecture, code | ENGINEERING.md |
| How do we deploy it? | Deployment steps, infrastructure | OPERATIONS.md |
| What's broken? | Troubleshooting, incidents | OPERATIONS.md |
| What are we building next? | Roadmap, future features | PRODUCT.md |
| How do I run tests? | Testing strategy | ENGINEERING.md |
| Who decided this? | Key decisions | MISSION_CONTROL.md |
| How do I commit? | Git conventions | MISSION_CONTROL.md |

---

## 📝 Maintenance Checklist

**Weekly (2 minutes):**
- [ ] Check this file for any obviously stale dates
- [ ] Skim MISSION_CONTROL.md for accuracy

**Monthly (10 minutes):**
- [ ] Review all "⚠️ Aging" docs, confirm still accurate
- [ ] Update their dates if reviewed
- [ ] Check 2-3 cross-references to ensure links work

**Quarterly (30 minutes):**
- [ ] Read through entire registry
- [ ] Update any stale docs (🔴)
- [ ] Check all links are valid
- [ ] Verify ownership assignments still current

---

## ✅ Success Criteria

You know this system is working when:

- ✅ New people find docs they need within 5 minutes
- ✅ Dates are accurate (within 7 days of last change)
- ✅ Cross-references work and are bidirectional
- ✅ All "⚠️ Aging" docs get reviewed monthly
- ✅ AI agents understand project state from reading this
- ✅ You rarely get asked "where's the docs for X?"

---

## 📞 Questions?

If you don't know which doc to read, ask:
- Your team lead
- In a comment/PR discussion
- Add a new entry here if it's a common question

That's valuable feedback for improving the registry.

---

**Keep this file updated. It's the map to everything else.**
