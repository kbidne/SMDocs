# 📚 SMDocs: Documentation Bootstrap Systems

**Two lightweight, generic documentation systems for any project:**
1. **Lean Bootstrap** - For teams and general projects
2. **Design Bootstrap** - For designers and UX teams

Choose the one that fits your needs, or use both together.

---

## 🎯 Quick Start: Which System Do I Need?

### 🏢 Lean Bootstrap
**For:** Any project, any team, distributed work, AI agent collaboration

**Solves:**
- Context loss between sessions (AI agents start fresh)
- Documentation staying in sync
- Quick onboarding (understand project in 15 minutes)
- Clear routing of information (who should read what)

**Setup time:** 30 minutes
**Maintenance:** ~1 hour/week

📂 Location: `/bootstrap-lean/`

👉 **Start here:** [`bootstrap-lean/BOOTSTRAP_LEAN.md`](bootstrap-lean/BOOTSTRAP_LEAN.md)

---

### 🎨 Design Bootstrap
**For:** Individual designers, design teams, UX/product designers

**Solves:**
- "Will AI replace designers?" (No, here's why with proof)
- Documenting design thinking (not just aesthetics)
- User-validated decisions (evidence, not guesses)
- Clear handoff to developers (zero revision cycles)

**Setup time:** 30 minutes
**Maintenance:** ~30 min/week

📂 Location: `/bootstrap-design/`

👉 **Start here:** [`bootstrap-design/DESIGN_PHILOSOPHY.md`](bootstrap-design/DESIGN_PHILOSOPHY.md)

---

## 📁 Repository Structure

```
SMDocs/
│
├── bootstrap-lean/              [Generic documentation system]
│   ├── BOOTSTRAP_LEAN.md       → Overview & philosophy
│   ├── MISSION_CONTROL.md      → AI agent instructions & project guide
│   ├── DOCS_INDEX.md           → Central documentation registry
│   ├── QUICKSTART.md           → 30-minute setup guide
│   ├── DOCS_TEMPLATE_ENGINEERING.md    → Tech documentation template
│   ├── DOCS_TEMPLATE_PRODUCT.md        → Product documentation template
│   ├── DOCS_TEMPLATE_OPERATIONS.md     → Operations documentation template
│   └── CLAUDE_MISSION_TEMPLATE.md      → Optional AI agent mission
│
├── bootstrap-design/            [Design-specific documentation system]
│   ├── DESIGN_BOOTSTRAP_OVERVIEW.md    → Overview for designers
│   ├── DESIGN_PHILOSOPHY.md            → Why this matters (career perspective)
│   ├── DESIGN_QUICKSTART.md            → 30-minute setup guide
│   ├── DESIGN_SYSTEM_TEMPLATE.md       → Your design source of truth
│   ├── DESIGN_PROCESS_TEMPLATE.md      → How to work with AI
│   ├── DESIGN_DECISIONS_TEMPLATE.md    → Design Decision Records (DDRs)
│   ├── DESIGN_RESEARCH_TEMPLATE.md     → User feedback & insights
│   └── DESIGN_TO_DEV_TEMPLATE.md       → Developer handoff specs
│
└── README.md                    [This file]
```

---

## 🚀 Getting Started

### Option 1: Use Lean Bootstrap (General Projects)

```bash
# 1. Copy to your project
cp -r bootstrap-lean/* /path/to/your/project/

# 2. Read the overview
cat bootstrap-lean/BOOTSTRAP_LEAN.md

# 3. Follow the quick start
cat bootstrap-lean/QUICKSTART.md

# 4. Customize the 3 templates for your project
# - MISSION_CONTROL.md (project info)
# - DOCS/ENGINEERING.md (tech details)
# - DOCS/PRODUCT.md (features)
# - DOCS/OPERATIONS.md (deployment)
```

**Time to setup:** 30 minutes

---

### Option 2: Use Design Bootstrap (Designers)

```bash
# 1. Copy to your project
cp -r bootstrap-design/* /path/to/your/project/

# 2. Understand the philosophy
cat bootstrap-design/DESIGN_PHILOSOPHY.md

# 3. Follow the quick start
cat bootstrap-design/DESIGN_QUICKSTART.md

# 4. Customize the 5 templates for your project
# - DESIGN_SYSTEM.md (components, colors, typography)
# - DESIGN_PROCESS.md (how you work)
# - DESIGN_DECISIONS.md (why you chose things)
# - DESIGN_RESEARCH.md (user feedback)
# - DESIGN_TO_DEV.md (handoff to developers)
```

**Time to setup:** 30 minutes

---

### Option 3: Use Both (Integrated Teams)

If your team has designers, engineers, and product people, use both:

```bash
# Copy both systems
cp -r bootstrap-lean/* /path/to/your/project/
cp -r bootstrap-design/* /path/to/your/project/

# Engineers/PMs: Read BOOTSTRAP_LEAN.md
# Designers: Read DESIGN_PHILOSOPHY.md
# Everyone: Understand both systems work together
```

**Time to setup:** 45 minutes
**Result:** Integrated documentation from design → code → operations

---

## 📖 What Each System Does

### Lean Bootstrap: The 3-Team Model

```
🔧 ENGINEERING              🎨 PRODUCT              ⚙️ OPERATIONS
Tech, architecture, APIs    Features, design,       Deploy, monitor,
Testing, how we build       requirements, why       runbooks, incidents
│                           │                        │
└───────────────┬───────────┴────────────────┬──────┘
                │
         MISSION_CONTROL.md
         (Project guide for everyone)
```

**Best for:**
- Any technical project
- Distributed teams
- AI agent collaboration
- Clear routing of information

---

### Design Bootstrap: The 5-Document Model

```
DESIGN_SYSTEM.md            DESIGN_PROCESS.md       DESIGN_RESEARCH.md
(Components, rules)         (How you work with AI)   (What users told you)
│                           │                        │
└───────────────┬───────────┴────────────────┬──────┘
                │
     DESIGN_DECISIONS.md
     (Why you chose what)
            │
         DESIGN_TO_DEV.md
         (Handoff to developers)
```

**Best for:**
- Individual designers
- Design teams
- Product + Design collaboration
- Proving design value in AI era

---

## 🎯 Lean Bootstrap: Core Files

| File | Purpose | Time |
|------|---------|------|
| **BOOTSTRAP_LEAN.md** | Overview, visuals, key principles | Read: 5 min |
| **MISSION_CONTROL.md** | AI agent instructions, project overview | Read: 5 min |
| **DOCS_INDEX.md** | Registry of all docs, freshness tracking | Read: 3 min |
| **QUICKSTART.md** | Step-by-step 30-minute setup | Read+Do: 30 min |
| **DOCS_TEMPLATE_ENGINEERING.md** | Tech documentation template | Customize: 15 min |
| **DOCS_TEMPLATE_PRODUCT.md** | Product documentation template | Customize: 15 min |
| **DOCS_TEMPLATE_OPERATIONS.md** | Operations documentation template | Customize: 15 min |
| **CLAUDE_MISSION_TEMPLATE.md** | Optional: AI agent mission briefing | Optional: 10 min |

---

## 🎨 Design Bootstrap: Core Files

| File | Purpose | Time |
|------|---------|------|
| **DESIGN_PHILOSOPHY.md** | Why designers matter in AI era | Read: 15 min |
| **DESIGN_BOOTSTRAP_OVERVIEW.md** | Overview, big picture, benefits | Read: 10 min |
| **DESIGN_QUICKSTART.md** | Step-by-step 30-minute setup | Read+Do: 30 min |
| **DESIGN_SYSTEM_TEMPLATE.md** | Document your design source of truth | Customize: 20 min |
| **DESIGN_PROCESS_TEMPLATE.md** | How to work with AI tools | Read: 10 min |
| **DESIGN_DECISIONS_TEMPLATE.md** | Document design decisions (DDRs) | Read: 10 min |
| **DESIGN_RESEARCH_TEMPLATE.md** | Log user feedback & insights | Read: 10 min |
| **DESIGN_TO_DEV_TEMPLATE.md** | Create developer handoff specs | Read: 15 min |

---

## ✨ Key Principles (Both Systems)

### 1. **Simple Over Complex**
Start lightweight. Both systems are designed to be adopted in 30 minutes with minimal friction.

### 2. **Aligned with How People Work**
- Lean Bootstrap: Uses 3 clear teams that map to real roles
- Design Bootstrap: Uses Figma terminology designers already understand

### 3. **AI-Friendly**
Both systems provide context-rich documentation that AI agents can read and understand across sessions.

### 4. **Documentation as Code**
Everything is markdown in git. Version controlled, reviewed, owned.

### 5. **Iteration Over Perfection**
These are starting points. Customize them to match your workflow.

---

## 🎓 Reading Order

### For Individual Developers/Small Teams
1. **Read:** `bootstrap-lean/BOOTSTRAP_LEAN.md` (5 min)
2. **Do:** `bootstrap-lean/QUICKSTART.md` (30 min)
3. **Customize:** The 3 template files
4. **Use:** Daily

### For Designers (Worried About AI)
1. **Read:** `bootstrap-design/DESIGN_PHILOSOPHY.md` (15 min)
2. **Do:** `bootstrap-design/DESIGN_QUICKSTART.md` (30 min)
3. **Customize:** The 5 template files
4. **Use:** Daily, build institutional knowledge

### For Design + Engineering Teams
1. **Read:** Both PHILOSOPHY files (30 min total)
2. **Do:** Both QUICKSTART files (60 min total)
3. **Customize:** All templates for both systems
4. **Use:** Integrated, designers own design docs, engineers own tech docs

---

## 🤝 How These Systems Work Together

If you're using both:

```
DESIGNERS                          ENGINEERS
    │                                  │
    ├─→ DESIGN_SYSTEM.md    ────→    DOCS/ENGINEERING.md
    │   (components)                  (how to build them)
    │
    ├─→ DESIGN_DECISIONS.md ────→    Understand why you chose X
    │   (why we chose this)
    │
    └─→ DESIGN_TO_DEV.md    ────→    DOCS_INDEX.md entry
        (handoff specs)              (registered as doc)
```

Designers maintain design documentation.
Engineers maintain technical documentation.
Product maintains product documentation.

Everyone reads MISSION_CONTROL.md to understand the project.

---

## 🆘 FAQ

### Q: Which system should I choose?

**A:**
- Small team / general project? → **Lean Bootstrap**
- You're a designer worried about AI? → **Design Bootstrap**
- You have both designers and engineers? → **Both**

### Q: Can I use these for an existing project?

**A:** Yes! Copy the templates and start documenting what you already have.

### Q: How much maintenance is this?

**A:**
- Lean Bootstrap: ~1 hour/week (update timestamps when docs change)
- Design Bootstrap: ~30 min/week (log decisions, research as you work)

### Q: Can I modify these templates?

**A:** Absolutely. These are starting points. Make them yours.

### Q: Do I need to use all files?

**A:** No. Start minimal. Add what you need.

### Q: Will AI agents understand these?

**A:** Yes. Both systems are designed with AI agents in mind. They provide clear context.

---

## 📚 Real-World Examples

### Example 1: Startup Using Lean Bootstrap

```
Day 1: Team copies bootstrap-lean/ files
Day 3: Customized MISSION_CONTROL.md, DOCS/*
Day 1 Week 2: New engineer joins, reads docs, productive same day
Month 2: AI agent (Claude) resumes work from previous session smoothly
Month 3: Clear record of all decisions, documented in git
```

### Example 2: Designer Using Design Bootstrap

```
Day 1: Designer reads DESIGN_PHILOSOPHY.md (confidence restored)
Day 2: Sets up design system documentation (DESIGN_SYSTEM.md)
Week 1: Documents first 3 decisions (DESIGN_DECISIONS.md)
Week 3: Tests design with users, logs feedback (DESIGN_RESEARCH.md)
Month 2: 15 documented decisions, 50 pieces of user feedback
Month 3: Can show stakeholders: "Here's why each decision was intentional"
```

---

## 🚀 Advanced Usage

### Using with Claude Code (AI Agent)

Both systems are optimized for Claude Code sessions:

```bash
# 1. Copy templates to your project
# 2. Customize placeholders
# 3. In Claude Code, reference the files:

"Here's our project setup. Read:
- bootstrap-lean/MISSION_CONTROL.md (how we work)
- bootstrap-lean/DOCS_INDEX.md (what docs exist)
- DOCS/[RELEVANT_FILE] (context for your task)"

# Claude reads these files, understands context, works effectively
```

### Integrating with Git Hooks

Both systems work with git pre-commit hooks:

```bash
# Check that docs are updated when relevant files change
# Check timestamps are current
# Verify cross-references are valid

# This keeps documentation honest
```

---

## 📞 Support & Feedback

Have questions? Want to improve these templates?

- **For Lean Bootstrap:** See `bootstrap-lean/BOOTSTRAP_LEAN.md`
- **For Design Bootstrap:** See `bootstrap-design/DESIGN_PHILOSOPHY.md`

Both files have troubleshooting sections and learning resources.

---

## ✅ Success Criteria

You know these systems are working when:

✅ New people onboard quickly (15-30 minutes)
✅ AI agents understand context in first session
✅ Decisions have clear reasoning documented
✅ Everyone knows where to look for information
✅ Docs stay in sync (not contradicting)
✅ You can explain why you chose something
✅ Developers reduce revision cycles (better handoff)

---

## 🎓 Credits

Both systems were designed to solve real problems:

**Lean Bootstrap:** Extracted from the [domideas project](https://github.com/kbidne/domideas), which maintains 3,700+ lines of documentation while working with AI agents across multiple sessions.

**Design Bootstrap:** Created to answer "How do designers stay valuable in the AI era?" Focuses on proving design is about judgment and validation, not pixel-pushing.

---

## 📄 License

These templates are free to use and modify for any project.

---

**Start small. Document as you go. Let the system evolve.**

Choose your path:
- 👉 [**Lean Bootstrap →**](bootstrap-lean/BOOTSTRAP_LEAN.md)
- 👉 [**Design Bootstrap →**](bootstrap-design/DESIGN_PHILOSOPHY.md)
