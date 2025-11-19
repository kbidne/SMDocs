# 🤖 Claude Code: Mission for [PROJECT_NAME]

**How Claude Code should help with this project**

---

## 🎯 Your Mission (In 3 Sentences)

You're helping develop **[PROJECT_NAME]**, which [BRIEF_DESCRIPTION].

Your job is to help the team by:
1. [Most important task: build features, fix bugs, maintain docs]
2. [Second priority: what else do you do]
3. [Third priority: anything else relevant]

---

## 📚 Required Reading (15 minutes)

When you start a session, **read these 3 files in order:**

1. **MISSION_CONTROL.md** (5 min)
   - Gives you project context
   - Shows you documentation map
   - Tells you how to commit changes

2. **DOCS_INDEX.md** (3 min)
   - Shows what documentation exists
   - Helps you find information quickly
   - Tracks which docs are fresh vs. stale

3. **Relevant DOCS/ file** (7 min)
   - If working on features → Read DOCS/PRODUCT.md
   - If working on code → Read DOCS/ENGINEERING.md
   - If working on deployment → Read DOCS/OPERATIONS.md

**After reading:** You'll understand project state and can proceed with work.

---

## 🛠️ Your Main Responsibilities

### Primary: [MAIN_TASK]

```
When you work on [main task]:
1. Read DOCS/[RELEVANT_FILE].md
2. Make changes to code/docs
3. Update relevant DOCS/ file
4. Update DOCS_INDEX.md timestamp
5. Commit atomically with clear message
```

**Example commit:**
```
[ENGINEERING] Add authentication endpoints

- Implement JWT-based login
- Add password hashing with bcrypt
- Update API reference in DOCS/ENGINEERING.md
- Update DOCS_INDEX.md timestamp
```

### Secondary: Keep Documentation Fresh

Whenever you learn something:
- Update the relevant DOCS/ file
- Update timestamp in DOCS_INDEX.md
- Commit the change

**Examples:**
- Discovered a faster way to do X? → Update ENGINEERING.md
- Found why users struggled with Y feature? → Update PRODUCT.md
- Learned how deployment works? → Update OPERATIONS.md

---

## 📍 Decision Tree: What to Do

```
User asks me to...?

  → Build a feature
       ↓
     Update PRODUCT.md + ENGINEERING.md
     ↓

  → Fix a bug
       ↓
     Update ENGINEERING.md troubleshooting section
     ↓

  → Deploy or run system
       ↓
     Follow OPERATIONS.md
     Update it if you learned something new
     ↓

  → Improve documentation
       ↓
     Update relevant DOCS/ file
     Update DOCS_INDEX.md timestamp
     ↓

  → Something else?
       ↓
     Ask the user which DOCS/ file owns this
```

---

## ✅ Quality Standards

### Before Committing

- [ ] Code works (tests pass, no errors)
- [ ] Relevant DOCS/ file is updated
- [ ] DOCS_INDEX.md timestamp is updated
- [ ] Commit message explains WHY, not just WHAT
- [ ] No contradictions with other docs

### When Unsure

- Check DOCS_INDEX.md to see which doc owns this topic
- Read that doc to understand current state
- Update it based on your work
- Ask if still unclear

### When Discovering Issues

If you find:
- Confusing documentation → Clarify it
- Outdated information → Update it
- Missing documentation → Add it
- Broken links → Fix them

**Never just note it.** Fix it immediately and commit.

---

## 🔄 The Feedback Loop

```
You make change
    ↓
Update docs
    ↓
Commit together
    ↓
Next session reads updated docs
    ↓
Understands more context
    ↓
Makes better changes
    ↓
[Loop improves infinitely]
```

This is how the system gets better with every session.

---

## 🚫 Things NOT to Do

❌ **Don't** commit code without updating docs
❌ **Don't** update docs without updating DOCS_INDEX.md timestamp
❌ **Don't** make conflicting changes across different DOCS/ files
❌ **Don't** create new documentation without registering it in DOCS_INDEX.md
❌ **Don't** assume something works; verify in code/tests

---

## ✅ Things You SHOULD Do

✅ **Do** read MISSION_CONTROL.md when you start
✅ **Do** update timestamps whenever you edit a doc
✅ **Do** commit related changes atomically
✅ **Do** check DOCS_INDEX.md when you're unsure
✅ **Do** add troubleshooting steps when you solve problems
✅ **Do** fix documentation issues you find, don't just note them

---

## 🎯 Success Criteria

You've done a great job when:

1. **Code works** - Features are built, bugs are fixed
2. **Docs are updated** - Someone can understand your work from reading DOCS/
3. **Registry is current** - DOCS_INDEX.md timestamps are fresh
4. **Next session is easy** - AI agent in next session can quickly understand state
5. **No contradictions** - DOCS/ files agree with each other

---

## 📊 Project Quick Facts

**Project:** [PROJECT_NAME]

**What it does:** [BRIEF_DESCRIPTION]

**Tech stack:** [YOUR_TECH_STACK]

**Current status:** [DEVELOPMENT_PHASE]

**Next goal:** [NEXT_MILESTONE]

---

## 🔗 Key Files

| File | Purpose | Read When |
|------|---------|-----------|
| `MISSION_CONTROL.md` | Project guide, workflows | Starting a session |
| `DOCS_INDEX.md` | Registry of all docs | Need to find information |
| `DOCS/ENGINEERING.md` | Technical info | Working on code |
| `DOCS/PRODUCT.md` | Feature info | Working on features |
| `DOCS/OPERATIONS.md` | Deployment info | Deploying or running |

---

## 👥 Team Members

| Role | Name | Responsibilities |
|------|------|---|
| [ROLE_1] | [NAME] | [What they own] |
| [ROLE_2] | [NAME] | [What they own] |
| [ROLE_3] | [NAME] | [What they own] |

**Questions?** Ask in order: team member → MISSION_CONTROL.md → DOCS_INDEX.md

---

## 🔑 Important Constraints

Things I **must** always do:
- [Constraint 1: e.g., "never commit secrets to git"]
- [Constraint 2: e.g., "always run tests before committing"]
- [Constraint 3: e.g., "follow the branching strategy"]

Things I **must never** do:
- [Never 1: e.g., "never force push to main"]
- [Never 2: e.g., "never modify production data directly"]
- [Never 3: e.g., "never skip security checks"]

---

## 🚀 Getting Started This Session

**Your task:** [USER_WILL_SPECIFY_THIS]

**Steps:**
1. Read MISSION_CONTROL.md (4 min)
2. Check DOCS_INDEX.md (2 min)
3. Read relevant DOCS/ file (5-10 min)
4. Confirm understanding with user
5. Proceed with work

---

## 📝 Commit Message Template

For consistency, use this format:

```
[TEAM] Brief description of change

Longer explanation:
- What changed and why
- What docs were updated
- Any important notes

Fixes: [Issue number if applicable]
Related: [Related files or docs]
```

**Example:**
```
[ENGINEERING] Optimize database query performance

- Added index to users.email column
- Reduced query time from 2s to 50ms
- Updated ENGINEERING.md with new schema
- Updated OPERATIONS.md with monitoring

Related: ENGINEERING.md, OPERATIONS.md
```

---

## 🎓 Learning

If you discover something useful:
- Add it to the relevant DOCS/ file
- Update DOCS_INDEX.md
- Commit it

This way, next session will know what you learned.

---

## ❓ When You're Stuck

**Decision tree:**

```
I'm stuck on...?

  → Understanding code
     Read: ENGINEERING.md Architecture section

  → Understanding features
     Read: PRODUCT.md Features section

  → Understanding deployment
     Read: OPERATIONS.md Deployment section

  → Something not documented
     → Ask the user
     → Document the answer in DOCS/
     → Commit

  → Unsure which doc to update
     Check: DOCS_INDEX.md "Which doc owns this?"
     Ask: If still unclear

  → Technical problem
     Check: ENGINEERING.md Troubleshooting
     Check: OPERATIONS.md Troubleshooting
     Try: Google + testing
     Document: Once you solve it
```

---

## 🏁 End of Session

Before finishing:

```
☐ All code changes committed
☐ All relevant docs updated
☐ DOCS_INDEX.md timestamps fresh
☐ Commit messages are clear
☐ No uncommitted changes
☐ Handoff notes left (if needed)
```

---

## 💬 Message to Next Session

[USER: Leave notes here about what you worked on, what's next, any gotchas]

```
Session [DATE] focused on:
- [Thing 1]
- [Thing 2]
- [Thing 3]

Next session should:
- [Task 1]
- [Task 2]

Gotchas:
- [Watch out for this]
- [This is tricky]
```

---

**Remember:** You're not just building features. You're building a knowledge system that gets smarter every session.

Good luck! 🚀
