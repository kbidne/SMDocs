# 🎤 Design Research: What Users Tell Us

**User feedback, insights, and learnings for [YOUR_BRAND]**

> Your designs should be based on what users actually need, not what you think they need.
> Document what users tell you, so you (and your team) learn over time.

---

## 📋 What This Is

A **running log of user feedback** organized by topic.

**Why document feedback?**
- Pattern recognition (see trends across users)
- Evidence-based design (prove your decisions with data)
- Institutional knowledge (new designers learn what works)
- Accountability (show why you made changes)
- Iteration loop (old feedback informs new decisions)

**How much to document?**
- Every user interview or test: YES
- General feedback/surveys: YES
- Casual "I like this" comments: Sometimes
- Personal opinions (not from users): NO

---

## 🏗️ Research Log Entry Template

For each user research session, create an entry:

```markdown
## Research Session: [Date] - [What You Were Testing]

**Date:** [YYYY-MM-DD]
**Participants:** [Number of users, brief description]
**Testing:** [What design/feature]
**Method:** [Interview / User test / Survey / Observation]
**Duration:** [How long]

### Key Questions Asked

- [Question 1?]
- [Question 2?]
- [Question 3?]

### Findings

**Insight 1:** [What surprised you?]
- User quote: "[What they said?]"
- Observation: [What you noticed?]
- Implication: [What this means for design]

**Insight 2:** [Another pattern]
- User quote: "[What they said?]"
- Observation: [What you noticed?]
- Implication: [What this means for design]

### What Users Liked

- ✅ [Good thing they mentioned]
- ✅ [Another thing]

### What Users Struggled With

- ❌ [Problem they faced]
- ❌ [Another friction]

### Next Steps

Based on this feedback:
- [ ] Change X component
- [ ] Test Y option
- [ ] Document learning in DESIGN_DECISIONS.md
- [ ] Update DESIGN_SYSTEM.md if needed

### Related

- Design being tested: [Link]
- Related decision: [Link to DDR if exists]
- Follow-up research: [Scheduled for when?]
```

---

## 📚 Example: Complete Research Entry

---

## Research Session: 2025-11-19 - Button Size Testing

**Date:** 2025-11-19
**Participants:** 5 mobile users, ages 25-45, varied tech comfort
**Testing:** Button height (36px vs 40px vs 44px vs 48px)
**Method:** Moderated user test (live)
**Duration:** 1 hour (10 min per user)

### Key Questions Asked

- "Which button size feels most natural to tap?"
- "Did you ever mis-tap on any of these?"
- "If this was your phone, which would you choose?"
- "Any concerns about any size?"

### Findings

**Insight 1: 44px is the sweet spot**
- User quote: "36px feels cramped. 44px feels right. 48px is overkill."
- Observation: Users consistently chose 44px without prompting
- Implication: 44px should be our minimum button height

**Insight 2: Mis-taps happen below 40px**
- User quote: "I keep hitting the wrong button with 36px"
- Observation: 3-4 mis-taps per user with 36px, 0 with 44px
- Implication: 36px is not acceptable for mobile

**Insight 3: Users don't notice 44px vs 48px**
- User quote: "Both feel fine, 44px is fine"
- Observation: No strong preference between 44px and 48px
- Implication: 44px is minimum, no need to go larger

### What Users Liked

- ✅ 44px "feels natural"
- ✅ Easy to tap without thinking
- ✅ Feels professional (not too big, not too small)
- ✅ Clear that it's clickable

### What Users Struggled With

- ❌ 36px buttons caused confusion ("is this tappable?")
- ❌ 36px buttons caused mis-taps (3+ per session)
- ❌ 36px felt cramped ("tight")

### Next Steps

- ✅ CONFIRMED: 44px minimum button height
- ✅ Created DDR-001 documenting this decision
- ✅ Updated DESIGN_SYSTEM.md > Button section with 44px rule
- ✅ Locked in button sizes across all components

### Related

- Design tested: Button sizes (Figma link)
- Design decision created: DDR-001 (Button Height 44px)
- Follow-up: Monitor mis-tap complaints in production (none so far)

---

## 🗂️ Organization By Topic

Instead of chronological, organize by theme:

### Avatar Design Research

**Session 1: 2025-11-15 - Avatar Shape Testing**
- Users prefer circular avatars
- Square feels "corporate"
- Gradients tested poorly

**Session 2: 2025-11-18 - Avatar Sizing**
- Need at least 36px to see details
- 48px+ feels excessive
- 40px is optimal

**Session 3: 2025-11-22 - Avatar Fallback Text**
- Initials only (not full name)
- Two characters (first + last initial)
- Centered and bold

**Pattern:** Circular, 40px, initials only → Used in DDR-003

---

### Form Design Research

**Session 1: 2025-11-10 - Input Field Testing**
- Users expect placeholder text to disappear
- Label must be visible (not replaced by placeholder)
- Error messages below field work better than above

**Session 2: 2025-11-17 - Form Layout**
- Single column better than multi-column
- Spacing between fields: 16px
- Submit button at bottom, centered

**Session 3: 2025-11-25 - Mobile Form Entry**
- Users struggle with small inputs on mobile
- Need larger touch targets
- Better to have longer form than tiny inputs

**Pattern:** Vertical form, labeled inputs, errors below → Used in DESIGN_SYSTEM.md

---

## 📊 Running Insights Database

Create a summary of patterns you're noticing:

### General Insights

| Insight | Evidence | Impact |
|---------|----------|--------|
| Users prefer clarity over cleverness | 8 sessions of feedback | Influences all copy |
| Mobile users tap harder than desktop clicks | Observation from tests | Larger minimum touch targets |
| Accessibility benefits everyone | Users with/without disabilities preferred AA standard | Became non-negotiable |
| Users don't read help text | Observed in 12 sessions | Make it unnecessary by good design |
| Colors convey meaning | Color-blind users proved this wrong | Never rely on color alone |

---

## 🎯 Quick Research Methods

### 1. Quick User Interview (10 minutes)

```
Setup: Show design, ask questions

Script:
"I'm testing this design. Your feedback helps us improve.
1. What do you see?
2. What would you do?
3. Any concerns?
4. Scale 1-10: How much would you use this?"

Log findings in research template
```

**Time:** 10 min per user × 3 users = 30 minutes
**Value:** High (direct feedback)

### 2. Unmoderated User Test

```
Setup: Send design to users, ask them to complete task

Task: "Create a task called 'Finish project'"

Observations:
- Where did they click?
- What confused them?
- Did they complete the task?
- Time taken?

Log findings
```

**Time:** 5 min per user × 5 users = 25 minutes
**Value:** Very high (real task performance)

### 3. Quick Survey

```
Question 1: What's your biggest challenge with [feature]?
Question 2: Rate our design 1-10
Question 3: What would make it better?

Log findings by category
```

**Time:** 1 min per user × 10 users = 10 minutes
**Value:** Medium (quantity over depth)

### 4. Observation

```
Watch real users using your design
- Don't prompt them
- Note where they struggle
- Note what they figure out easily
- Log patterns

Example: Notice users always clicking wrong button?
That's research telling you to redesign.
```

**Time:** Varies
**Value:** High (unbiased)

---

## 🔄 The Feedback Loop

```
Session 1: Test Design A
    ↓
Log findings in DESIGN_RESEARCH.md
    ↓
Identify patterns
    ↓
Update DESIGN_DECISIONS.md
    ↓
Update DESIGN_SYSTEM.md
    ↓
Session 2: Test Design B (improved based on feedback)
    ↓
[Loop continues]
```

Each research session should inform the next design decision.

---

## 📋 Common Research Topics

### Usability Research

```
"Can users accomplish their task?"

Document:
- Task assigned
- Did they succeed?
- How long did it take?
- What was confusing?
- What was clear?
```

### Preference Research

```
"Which design do users prefer?"

Document:
- Option A vs Option B
- Which did they choose?
- Why did they choose it?
- Any reservations?
```

### Accessibility Research

```
"Does this work for everyone?"

Document:
- Tested with color-blind users? Result?
- Tested with screen reader? Result?
- Tested on mobile? Result?
- Tested at zoom 200%? Result?
```

### Brand Research

```
"Does this feel like us?"

Document:
- Users' first impression
- Does it match brand?
- Professional vs playful?
- Trust level?
```

---

## 🚨 Red Flags (Research Telling You Something's Wrong)

Watch for patterns indicating design problems:

| Red Flag | Meaning | Action |
|----------|---------|--------|
| Users consistently mis-tap button | Too small | Make it bigger |
| Users skip a field | Unnecessary | Remove it or clarify |
| Users confused about next step | Unclear CTA | Redesign call-to-action |
| Users can't find feature | Hidden or undiscovered | Better positioning |
| Users take 2x longer than expected | Complex interaction | Simplify |
| Users with accessibility tools struggle | Not accessible | Fix accessibility |

---

## 💬 Template for Research Quotes

When documenting user quotes:

```
Full quote: "[Exactly what they said, including filler words]"

Cleaned quote: "[Meaningful part without 'ums' and 'likes']"

Context: "[What they were doing when they said this]"

Implication: "[What this tells us about design]"
```

**Example:**

```
Full quote: "Um, like, I don't know, this button is kind of,
like, hard to hit? My finger keeps missing it."

Cleaned quote: "This button is hard to hit. My finger keeps missing it."

Context: User was trying to delete a task on mobile

Implication: 36px button is too small. Need 44px minimum.
```

---

## 📊 Tracking Research Over Time

Keep a summary:

```
# Research Summary 2025

## November
- Sessions: 12
- Participants: 28
- Key finding: 44px button minimum confirmed by 15+ users

## December
- Sessions: [In progress]
- Participants: [In progress]
- Key finding: [What are you learning?]

## Patterns Across Months
- [What's consistent?]
- [What changed?]
- [What surprised you?]
```

---

## 🎓 How to Use Research

### When Making a Design Decision

```
You're deciding between Option A and Option B

Check DESIGN_RESEARCH.md:
"Have users weighed in on this?"

Option A: 3 users preferred it
Option B: 1 user preferred it, 2 were neutral

Choose Option A with confidence (based on evidence)
```

### When Someone Questions Your Design

```
Stakeholder: "Why is the button 44px?"

You: "Check DESIGN_RESEARCH.md > Button Size Testing

Users mis-tapped 36px buttons but not 44px buttons.
Multiple sessions confirmed this. That's why."
```

### When Designing Similar Components

```
You're designing a new button-like component

Check DESIGN_RESEARCH.md:
"What did we learn from the last button design?"

Apply those learnings to the new component
```

---

## ✅ Research Checklist

Before launching a design:

```
☐ Tested with at least 2-3 users
☐ Tested on target devices (mobile if mobile app)
☐ Tested with accessibility tools
☐ Gathered feedback from at least one source
☐ Documented findings in DESIGN_RESEARCH.md
☐ Created/updated DDR if significant finding
☐ Updated DESIGN_SYSTEM.md if it affects patterns
☐ Identified next research to conduct
```

---

## 🔗 Related Files

- **DESIGN_PROCESS.md** - How you validate designs (Phase 4)
- **DESIGN_DECISIONS.md** - Where you explain decisions informed by research
- **DESIGN_SYSTEM.md** - Where patterns become standards

---

## 💡 Pro Tips

### Recruit Real Users
- Not friends/family
- Not designers (they think differently)
- Actual target users

### Document Immediately
Don't wait until later. Memory fades. Document while fresh.

### Share Findings
Post in Slack, email team, mention in standup.
Feedback is only valuable if people know about it.

### Look for Patterns
- 1 user saying something: interesting
- 3 users saying same thing: design change needed
- 10 users saying same thing: this is a standard now

### Test Early and Often
- Test sketches (not just polished designs)
- Test with fewer users early (3-5)
- Test with more users for confidence (10+)
- Test continuously, not just at launch

---

**Remember:**

Your opinion doesn't matter. Users' opinions matter.

If you think something is good but users disagree, users are right.

Document what users tell you, follow the evidence, and your designs will be great.

---

**Next:** DESIGN_TO_DEV.md — How to hand off to developers
