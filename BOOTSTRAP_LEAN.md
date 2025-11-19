# 📚 Project Bootstrap Template (Lean Edition)

**A lightweight, generic documentation system for any project**

> Perfect for: New projects, AI-agent-heavy work, distributed teams, projects that need fast onboarding

---

## 🎯 What This Is

This is a **5-file, 1000-line documentation bootstrap** that solves:

```
Problem                    → Solution
─────────────────────────────────────────────────────────
AI forgets context         → Mission Control (claude.md)
Docs scattered everywhere  → Central Registry (DOCS_INDEX.md)
Unclear what to read first → Quick Start Guide
Where do I work?           → 3 clear documentation teams
How do I update docs?      → Simple 2-step workflow
```

**Setup Time:** 30 minutes | **Learning Curve:** 15 minutes | **Maintenance:** 5 min/week

---

## 📂 What You Get

```
your-project/
├── README.md                    ← Project intro (your existing file)
├── QUICKSTART.md                ← How to bootstrap this system
├── MISSION_CONTROL.md           ← AI agent instructions
├── DOCS_INDEX.md                ← Registry of all documents
│
├── DOCS/                         ← Your documentation
│   ├── ENGINEERING.md           ├─ Tech, architecture, APIs
│   ├── PRODUCT.md               ├─ Features, design, requirements
│   └── OPERATIONS.md            └─ Deployment, incidents, runbooks
│
└── .claude/                      ← Optional: AI agent config
    └── mission.md               └─ How Claude should help
```

**That's it.** 5 files. Done.

---

## 🚀 Quick Start (3 Steps)

### Step 1: Copy the Templates
```bash
# Copy all bootstrap files to your project root
curl -s https://raw.githubusercontent.com/kbidne/SMDocs-Lean/main/MISSION_CONTROL.md > MISSION_CONTROL.md
curl -s https://raw.githubusercontent.com/kbidne/SMDocs-Lean/main/DOCS_INDEX.md > DOCS_INDEX.md
curl -s https://raw.githubusercontent.com/kbidne/SMDocs-Lean/main/QUICKSTART.md > QUICKSTART.md
```

### Step 2: Customize (5 minutes)

In `MISSION_CONTROL.md`, replace these:
- `[PROJECT_NAME]` → Your project name
- `[BRIEF_DESCRIPTION]` → What your project does
- `[YOUR_TECH_STACK]` → Technologies you use

### Step 3: Commit

```bash
git add MISSION_CONTROL.md DOCS_INDEX.md QUICKSTART.md
git commit -m "[Docs] Bootstrap project documentation system"
```

**Done! Your documentation is set up.**

---

## 🏗️ The 3 Documentation Teams

Instead of 7 specialized teams (overkill), this system uses **3 core teams**:

### 🔧 **ENGINEERING**
*Technical decisions, architecture, how things work*
- System architecture and design
- Technology choices and rationale
- API documentation
- Testing strategy
- Database schema
- Integration guides

📄 **File:** `DOCS/ENGINEERING.md`

---

### 🎨 **PRODUCT**
*What you're building and why*
- Feature requirements
- Design patterns and UI
- User workflows and use cases
- Product decisions
- Roadmap and priorities
- Business rules

📄 **File:** `DOCS/PRODUCT.md`

---

### ⚙️ **OPERATIONS**
*Keeping it running*
- Deployment procedures
- Infrastructure and DevOps
- Monitoring and alerts
- Incident response
- Operational runbooks
- Troubleshooting guides

📄 **File:** `DOCS/OPERATIONS.md`

---

## 📋 The 2-Step Workflow

**Update ANY document:**

```
Step 1: Make your change
        └─→ Edit the doc (ENGINEERING.md, PRODUCT.md, etc.)

Step 2: Update the registry
        └─→ Edit DOCS_INDEX.md (change timestamp and link)
        └─→ Update MISSION_CONTROL.md if workflows changed

Step 3: Commit together
        └─→ git add [doc] DOCS_INDEX.md MISSION_CONTROL.md
        └─→ git commit -m "[Team] Brief description of what changed"
```

That's it. No mandatory 7-step workflows, no governance theater. Just keep things in sync.

---

## 🎯 When to Use Each Doc

**Decision Tree:**

```
    Is it about...?

    ENGINEERING?           → DOCS/ENGINEERING.md
    (code, tech, architecture, how it works)
         ↓
    PRODUCT?               → DOCS/PRODUCT.md
    (features, design, what we're building, why)
         ↓
    OPERATIONS?            → DOCS/OPERATIONS.md
    (deployment, running, monitoring, ops)
         ↓
    None of above?         → Add a new file OR ask in DOCS_INDEX.md
    (create it, add to registry)
```

---

## 👤 For AI Agents

When you start working with Claude Code or other AI agents:

**Provide them this:**
```
Here's our project structure:
- MISSION_CONTROL.md: AI agent instructions
- DOCS_INDEX.md: What docs we have
- DOCS/ENGINEERING.md: Tech info
- DOCS/PRODUCT.md: Feature info
- DOCS/OPERATIONS.md: Ops info

When you make changes, update the registry and commit atomically.
```

**They will:**
1. Read `MISSION_CONTROL.md` to understand guidelines
2. Check `DOCS_INDEX.md` to see what exists
3. Update relevant files + registry
4. Commit with proper messages

---

## ✅ Success Looks Like

```
✓ New team members onboard in 15 minutes
✓ AI agents understand project context in one session
✓ Docs always match each other (no contradictions)
✓ You know what docs exist (DOCS_INDEX.md)
✓ Timestamps show what's fresh vs. stale
✓ Cross-references work (you can follow links)
✓ Everyone knows where to look for information
```

---

## 📊 Visual: How It All Connects

```
                    MISSION_CONTROL.md
                    (Guidebook for everyone)
                            ↓
                ┌───────────┼───────────┐
                ↓           ↓           ↓
            ENGINEERING   PRODUCT    OPERATIONS
            ────────────────────────────────────
            • Architecture  • Features   • Deploy
            • Tech stack    • Design     • Runbooks
            • APIs          • Workflows  • Monitoring
            • Testing       • Roadmap    • Incidents
                ↓           ↓           ↓
                └───────────┼───────────┘
                            ↓
                    DOCS_INDEX.md
                    (Central Registry)
```

---

## 🛠️ Optional: Extending Beyond 3 Teams

As your project grows, you can add more docs, but keep them organized:

**Example expansions:**

```
DOCS/ENGINEERING.md          DOCS/OPERATIONS.md
├─ ARCHITECTURE.md           ├─ DEPLOYMENT.md
├─ API_REFERENCE.md          ├─ MONITORING.md
└─ TESTING.md                └─ INCIDENTS.md

DOCS/PRODUCT.md
├─ REQUIREMENTS.md
├─ DESIGN_SYSTEM.md
└─ ROADMAP.md
```

Just update `DOCS_INDEX.md` as you add files. The system scales naturally.

---

## 🔄 Maintenance Schedule

| When | What | Time |
|------|------|------|
| **When editing a doc** | Update timestamp in DOCS_INDEX.md | 30 sec |
| **Weekly** | Glance at DOCS_INDEX.md for any red flags | 2 min |
| **Monthly** | Review if docs still match reality | 5 min |
| **Quarterly** | Check links, fix broken references | 10 min |

---

## 🎓 Real-World Example

**Your project:** A web app for task management

```
DOCS/ENGINEERING.md
├─ Built with React + Node.js
├─ Database: PostgreSQL
├─ Deployed to AWS
└─ REST API v2

DOCS/PRODUCT.md
├─ Core feature: Create/assign/track tasks
├─ Roadmap: Collaboration, mobile app, analytics
├─ User roles: Admin, Team Lead, Member
└─ Key decision: Real-time updates via WebSocket

DOCS/OPERATIONS.md
├─ Deploy: GitHub Actions → AWS ECS
├─ Monitoring: CloudWatch + PagerDuty
├─ Runbook: "Database is slow" → Check indexes
└─ Incident: Service down → Page on-call engineer
```

Someone new reads these 3 docs and understands **exactly** what your app is, how it works, and how to keep it running.

---

## ❓ FAQ

**Q: Isn't this just... a README?**
A: Similar concept, but organized into 3 focused areas + a registry so you know what to read. Makes it work better with AI agents and distributed teams.

**Q: What if we need governance/compliance docs?**
A: Add a `DOCS/COMPLIANCE.md` file and register it in DOCS_INDEX.md. The system scales.

**Q: What if docs get out of sync?**
A: Timestamp check in DOCS_INDEX.md shows you which docs are stale. Review them together when that happens.

**Q: Can we automate this?**
A: Yes! A simple GitHub Actions workflow can check that DOCS_INDEX.md is updated when files change. Optional.

**Q: This feels too simple. Is that OK?**
A: Yes! Simple = used. Complex = ignored. Start simple, extend as needed.

---

## 📝 Creating Your First Doc (Example)

**You want to add a SECURITY.md doc:**

**Step 1:** Create `DOCS/SECURITY.md`
```markdown
# Security

## Vulnerability Reporting
Report security issues to: [email]

## Authentication
We use [method]. See ENGINEERING.md for implementation details.

## Data Protection
[Your policies here]
```

**Step 2:** Update `DOCS_INDEX.md`
```markdown
## DOCS/SECURITY.md
- **Last Updated:** 2025-11-19
- **Team:** Operations
- **Purpose:** Security policies and vulnerability procedures
- **Related:** ENGINEERING.md, OPERATIONS.md
```

**Step 3:** Commit
```bash
git add DOCS/SECURITY.md DOCS_INDEX.md
git commit -m "[Operations] Add security vulnerability reporting procedures"
```

Done!

---

## 🎬 Next Steps

1. **Copy the 4 templates** (MISSION_CONTROL.md, DOCS_INDEX.md, QUICKSTART.md, and team docs)
2. **Customize them** (replace bracketed placeholders)
3. **Add your existing docs** to DOCS_INDEX.md
4. **Commit everything**
5. **Start using it** with your team/AI agents

**Total time: 30 minutes**

---

**Remember:** This bootstrap is a *starting point*, not a rigid framework. Modify it to match your project's needs. The goal is clarity and organization, not bureaucracy.

Good luck! 🚀
