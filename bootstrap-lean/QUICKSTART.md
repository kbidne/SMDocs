# 🚀 Quick Start: Bootstrap Your Project

**Goal:** Get your documentation system set up in 30 minutes

**Status:** [Not started] → [In progress] → [Complete]

---

## ⏱️ Timeline

- **Total Time:** 30 minutes
- **Setup:** 10 minutes
- **Customization:** 10 minutes
- **First Commit:** 5 minutes
- **Verification:** 5 minutes

---

## 📋 Step 1: Copy the Files (5 minutes)

You'll need these 5 files in your project root:

1. **MISSION_CONTROL.md** - AI agent instructions
2. **DOCS_INDEX.md** - Documentation registry
3. **DOCS/ENGINEERING.md** - Tech documentation
4. **DOCS/PRODUCT.md** - Product documentation
5. **DOCS/OPERATIONS.md** - Operations documentation

### Option A: Copy from SMDocs Repository

```bash
# If you have the SMDocs repo cloned
cp /path/to/SMDocs/MISSION_CONTROL.md ./
cp /path/to/SMDocs/DOCS_INDEX.md ./
cp /path/to/SMDocs/DOCS_TEMPLATE_ENGINEERING.md ./DOCS/ENGINEERING.md
cp /path/to/SMDocs/DOCS_TEMPLATE_PRODUCT.md ./DOCS/PRODUCT.md
cp /path/to/SMDocs/DOCS_TEMPLATE_OPERATIONS.md ./DOCS/OPERATIONS.md
```

### Option B: Download Directly

```bash
# Create DOCS directory if needed
mkdir -p DOCS

# Download files
wget https://raw.githubusercontent.com/kbidne/SMDocs/main/MISSION_CONTROL.md
wget https://raw.githubusercontent.com/kbidne/SMDocs/main/DOCS_INDEX.md
wget https://raw.githubusercontent.com/kbidne/SMDocs/main/DOCS_TEMPLATE_ENGINEERING.md -O DOCS/ENGINEERING.md
wget https://raw.githubusercontent.com/kbidne/SMDocs/main/DOCS_TEMPLATE_PRODUCT.md -O DOCS/PRODUCT.md
wget https://raw.githubusercontent.com/kbidne/SMDocs/main/DOCS_TEMPLATE_OPERATIONS.md -O DOCS/OPERATIONS.md
```

### Option C: Manual Copy-Paste

Copy the content of each template file into your project.

✅ **Done!** You now have the structure.

---

## 📝 Step 2: Customize Templates (10 minutes)

Open **MISSION_CONTROL.md** and find all the bracketed placeholders `[LIKE_THIS]`:

### Required Placeholders

```
[PROJECT_NAME]
Replace with: Your project name
Example: "TaskMaster" or "PaymentAPI"

[BRIEF_DESCRIPTION_OF_PROJECT]
Replace with: One sentence on what your project does
Example: "A lightweight task management tool for distributed teams"

[DEVELOPMENT_PHASE]
Replace with: Current status
Example: "Beta", "Early alpha", "In development", "Live"

[NEXT_GOAL]
Replace with: What's next?
Example: "Launch mobile app", "Optimize performance", "Add authentication"

[BRIEF_LIST_OF_TECH]
Replace with: Your tech stack (brief)
Example: "React, Node.js, PostgreSQL, AWS"
```

### Where Placeholders Are

- **MISSION_CONTROL.md:** Top section (Project Overview)
- **DOCS_INDEX.md:** Top section and throughout
- **DOCS/ENGINEERING.md:** Quick Facts, API sections
- **DOCS/PRODUCT.md:** Quick Facts, Features sections
- **DOCS/OPERATIONS.md:** Quick Facts, Infrastructure sections

### Quick Search & Replace

```bash
# Find all placeholders
grep -r "\[YYYY-MM-DD\]" .
grep -r "\[PROJECT_NAME\]" .

# Replace (Mac/Linux)
sed -i 's/\[PROJECT_NAME\]/MyProject/g' MISSION_CONTROL.md
sed -i 's/\[YYYY-MM-DD\]/2025-11-19/g' MISSION_CONTROL.md

# Replace (if sed doesn't work)
find . -name "*.md" -exec sed -i 's/\[PROJECT_NAME\]/MyProject/g' {} \;
```

✅ **Done!** Your docs are customized.

---

## 📚 Step 3: Add Your Existing Docs (5 minutes)

If you already have documentation, register it in **DOCS_INDEX.md**:

### Example: You Have a README

In `DOCS_INDEX.md`, add:

```markdown
### README.md
**Purpose:** Project introduction and quick start
**Last Updated:** [TODAY'S DATE]
**Freshness:** ✅ Recent
**Owner:** [YOUR_NAME]
**Contains:**
- [ ] What the project does
- [ ] How to install/set up
- [ ] Quick start guide

**Read This If:** You're completely new to the project
```

### Example: You Have an API Doc

```markdown
### DOCS/ENGINEERING.md - API Reference Section
**Purpose:** REST API endpoint documentation
**Last Updated:** [TODAY'S DATE]
**Freshness:** ✅ Recent
**Owner:** [YOUR_NAME]
**Related Docs:** PRODUCT.md, OPERATIONS.md
**Contains:**
- [ ] All API endpoints
- [ ] Request/response examples
- [ ] Error codes
```

### If You Have No Existing Docs

That's fine! Use the templates we provided. They're starting points.

✅ **Done!** Your existing docs are registered.

---

## 🔄 Step 4: First Commit (5 minutes)

### Verify Files Exist

```bash
# Should see these files:
ls -la MISSION_CONTROL.md
ls -la DOCS_INDEX.md
ls -la DOCS/
# → ENGINEERING.md
# → PRODUCT.md
# → OPERATIONS.md
```

### Stage Files

```bash
git add MISSION_CONTROL.md DOCS_INDEX.md DOCS/
git status  # Verify files are staged
```

### Create Commit

```bash
git commit -m "[Docs] Initialize project documentation system

- Add MISSION_CONTROL.md for project overview and guidelines
- Add DOCS_INDEX.md as central documentation registry
- Add DOCS/ENGINEERING.md for technical documentation
- Add DOCS/PRODUCT.md for product documentation
- Add DOCS/OPERATIONS.md for operational documentation

Customized templates for [PROJECT_NAME]"
```

### Push (Optional)

```bash
git push origin main
# or your current branch
```

✅ **Done!** Your documentation system is initialized.

---

## ✅ Step 5: Verify Setup (5 minutes)

### Check 1: Can You Read All Files?

```bash
# All files should be readable
cat MISSION_CONTROL.md | head -20
cat DOCS_INDEX.md | head -20
cat DOCS/ENGINEERING.md | head -20
cat DOCS/PRODUCT.md | head -20
cat DOCS/OPERATIONS.md | head -20
```

### Check 2: Can You Find Information?

**Test:** "I need to know how to deploy this"
- Open DOCS_INDEX.md
- Search for "OPERATIONS"
- Open DOCS/OPERATIONS.md
- Should find deployment steps

**Test:** "I need to understand the tech stack"
- Open DOCS_INDEX.md
- Search for "ENGINEERING"
- Open DOCS/ENGINEERING.md
- Should find technology stack table

### Check 3: Are Timestamps Current?

In `DOCS_INDEX.md`, check the "Last Updated" dates:
- Should be today or very recent
- Not dates from template

✅ **All checks pass!** You're ready to go.

---

## 🎯 What's Next?

### Immediate (Today)

1. Share the documentation with your team
2. Point new team members to **MISSION_CONTROL.md**
3. Update docs as you work on features

### Short Term (This Week)

1. Flesh out the 3 documentation files:
   - DOCS/ENGINEERING.md → Add your actual architecture
   - DOCS/PRODUCT.md → Add your actual features
   - DOCS/OPERATIONS.md → Add your actual deployment process

2. Add any missing sections to DOCS_INDEX.md

### Ongoing (Weekly)

- When you change something → Update the relevant doc
- When you update a doc → Update its timestamp in DOCS_INDEX.md
- Commit changes together

---

## 📖 How to Use Once Set Up

### When Starting New Work

```
1. Read MISSION_CONTROL.md (5 min)
   └─ Understand project, workflows, conventions

2. Check DOCS_INDEX.md (2 min)
   └─ See what docs exist, find what you need

3. Read relevant DOCS/ files (5-10 min)
   └─ Understand engineering/product/ops side
```

**Total: 15-20 minutes to full context**

### When Making Changes

```
1. Update relevant DOCS/ file
   └─ DOCS/ENGINEERING.md if tech changes
   └─ DOCS/PRODUCT.md if features change
   └─ DOCS/OPERATIONS.md if deployment changes

2. Update DOCS_INDEX.md timestamp
   └─ Mark file as recently updated

3. Commit both files together
   └─ git add [file] DOCS_INDEX.md
   └─ git commit -m "[TEAM] Description"
```

---

## 🧠 Memory Aid

### The 3 Teams

```
🔧 ENGINEERING          🎨 PRODUCT              ⚙️ OPERATIONS
Tech, APIs, testing     Features, design        Deploy, monitor, incidents
How we build it         What we're building     How we run it
```

### The 2-Step Workflow

```
Step 1: Edit the doc
   ↓
Step 2: Update registry + commit together
   ↓
Done!
```

### The Registry

```
DOCS_INDEX.md tells you:
- What docs exist
- When they were last updated
- Which ones are fresh vs. stale
```

---

## ❓ Troubleshooting

### "I don't understand what goes in [TEAM_NAME]"

**Solution:** Read the template section headings. Each template has:
- **Purpose** - What this doc covers
- **Contains** - Checklist of what should be in here
- **Read This If** - When you should read it

### "We have way more docs than 3"

**Solution:** That's OK! Add them to DOCS_INDEX.md:
- Still use the 3 main teams as core
- Add custom docs as needed
- Keep DOCS_INDEX.md updated

**Example:**
```
DOCS/ENGINEERING/
├─ ARCHITECTURE.md
├─ API_REFERENCE.md
└─ DATABASE.md

DOCS/PRODUCT/
├─ FEATURES.md
└─ ROADMAP.md
```

### "Updating timestamps is tedious"

**Solution:** Automate it! Add to your git hooks:
```bash
# .git/hooks/pre-commit
# Auto-update timestamp when you commit doc changes
```

Or just accept it takes 10 seconds.

### "My team won't use the system"

**Solution:**
1. Start with just the 3 core docs
2. Show value (faster onboarding, better AI results)
3. Make it part of PR checklist
4. Lead by example

### "Should we add more governance/frameworks?"

**Solution:** The lean version is intentionally simple. If you need:
- Complex AI governance → See SMDocs main repo
- Compliance docs → Add a DOCS/COMPLIANCE.md
- Security → Add a DOCS/SECURITY.md
- Custom workflows → Add to MISSION_CONTROL.md

Start simple, extend as needed.

---

## 🎓 Example: Complete Setup (Real Project)

**Project:** Simple todo API

### Files Setup

```
todo-api/
├── README.md
├── MISSION_CONTROL.md       ← Customized
├── DOCS_INDEX.md            ← Customized
├── DOCS/
│   ├── ENGINEERING.md       ← Customized
│   ├── PRODUCT.md           ← Customized
│   └── OPERATIONS.md        ← Customized
```

### Customization Example

In MISSION_CONTROL.md:

```markdown
# 🎯 Mission Control: Todo API

**[PROJECT_NAME]** → **Todo API**
**[BRIEF_DESCRIPTION]** → **A simple REST API for managing todo lists**
**[DEVELOPMENT_PHASE]** → **Beta (private testing)**
**[NEXT_GOAL]** → **Launch public API v1.0**
**[BRIEF_LIST_OF_TECH]** → **Node.js, Express, PostgreSQL, AWS**
```

In DOCS/ENGINEERING.md:

```markdown
| | |
|---|---|
| **Primary Language** | JavaScript (Node.js) |
| **Framework** | Express.js |
| **Database** | PostgreSQL 14 |
| **Deployment** | AWS Lambda + RDS |
```

In DOCS/PRODUCT.md:

```markdown
### What We're Building

Todo API is a simple REST API that lets users create, update, and track todo items. It's designed to be:
- Simple to use (no complex UI)
- Fast (optimized queries)
- Reliable (99.9% uptime)

### Core Features

- Create/read/update/delete todos
- Mark todos as complete
- Filter todos by status
- Basic authentication

### Roadmap

- Q4: Launch v1.0
- Q1 2026: Add teams/sharing
- Q2 2026: Add mobile apps
```

In DOCS/OPERATIONS.md:

```markdown
| Service | Purpose | Provider |
|---------|---------|----------|
| API | Run application | AWS Lambda |
| Database | Store todos | AWS RDS |
| File Storage | Backups | AWS S3 |
```

### First Commit

```bash
git add MISSION_CONTROL.md DOCS_INDEX.md DOCS/
git commit -m "[Docs] Initialize documentation system for Todo API

- Customized MISSION_CONTROL.md with Todo API context
- Created DOCS_INDEX.md registry
- Added ENGINEERING.md with Node.js/Express/PostgreSQL stack
- Added PRODUCT.md with todo feature list and roadmap
- Added OPERATIONS.md with AWS deployment details

Setup time: 25 minutes"
```

✅ **Done!** Todo API is bootstrapped and ready.

---

## 🏁 Success Checklist

```
☐ All 5 files copied to project
☐ All placeholders customized
☐ Existing docs added to registry
☐ Files committed to git
☐ Can read all files without errors
☐ Can find documentation by team
☐ Timestamps are current
☐ Team knows where to look for info
```

All checked? **You're done!** 🎉

---

## 📞 Getting Help

If something's unclear:
1. Check the template files themselves (they have detailed explanations)
2. Read BOOTSTRAP_LEAN.md for philosophy
3. Check MISSION_CONTROL.md for workflow questions
4. Ask your team lead

---

**Remember:** This system is a starting point. Customize it, extend it, make it yours. The goal is clarity and organization, not bureaucracy.

Good luck! 🚀
