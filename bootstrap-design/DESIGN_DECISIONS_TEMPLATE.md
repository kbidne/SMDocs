# ✍️ Design Decisions: Our Thinking

**Design Decision Records (DDRs) for [YOUR_BRAND]**

> Why we made the choices we made, so future designers can learn from our thinking

---

## 📋 What This Is

A **decision record** for each significant design choice.

**Why document this?**
- Future you will forget why you chose something
- New designers can learn from your thinking
- You have proof that decisions were intentional
- It helps when someone asks "why did we do it that way?"

**How much to document?**
- Major component designs: YES
- Color palette: YES
- Spacing system: YES
- One-off UI tweaks: NO

---

## 🏗️ DDR Template

Copy this template for each decision:

```markdown
## DDR-###: [Decision Name]

**Status:** [Proposed / In Review / Approved / Deprecated]
**Date:** [YYYY-MM-DD]
**Designer:** [Your name]

### The Decision

[One sentence summary of what you decided]

**Example:** "Use 44px minimum button height for all interactive elements"

### Why This Decision?

[2-3 sentences explaining the reasoning]

**Example:** "Mobile users need large touch targets to tap accurately.
Standard is 44px minimum. Smaller buttons cause mis-taps and frustration."

### What We Explored

[What options did you consider?]

**Example:**
- Option A: 36px (too small, users struggled in testing)
- Option B: 40px (awkward, not standard)
- Option C: 44px (standard, users comfortable)
- Option D: 48px (works but bigger than needed)

### User Validation

[What did users say?]

**Example:**
"Tested with 5 users on mobile. 44px felt natural to tap.
36px caused mis-taps. 44px is the minimum."

### Trade-offs

[What did we give up by choosing this?]

```
✅ Advantage 1: Clear benefit
✅ Advantage 2: Clear benefit
⚠️ Trade-off 1: What we're not getting
❌ Disadvantage 1: What we're avoiding
```

**Example:**
```
✅ Mobile friendly (easy to tap)
✅ Accessible by default
✅ Standard across industry
⚠️ Takes more vertical space (might feel "big")
❌ Not as compact as we initially wanted
```

### Related Components/Decisions

[Does this affect other things?]

**Example:**
- Related: All buttons now follow this rule
- Related: DDR-002 (Spacing system) built around this
- Related: DESIGN_SYSTEM.md > Button section

### What We Learned

[What did this teach us?]

**Example:**
"Mobile design is different from desktop. What works on desktop
might be too small on mobile. User testing revealed this immediately."

### What We'd Do Differently

[Anything you'd change if you did it again?]

**Example:**
"Nothing. This decision has proven solid across all products."

OR

"Next time, test on actual devices earlier instead of in Figma.
Would've caught this faster."

### Status & Next Steps

[Where does this stand?]

**Example:**
- ✅ **APPROVED** - Implemented in design system
- ✅ **IN USE** - All new buttons follow this
- 🔄 **PENDING** - Waiting for dev feedback
- ⚠️ **UNDER REVIEW** - Considering alternatives
- 🚫 **DEPRECATED** - No longer used (v2.0 changed this)

### Links & References

[Link to related docs]

- See DESIGN_SYSTEM.md > Button section
- See DESIGN_TO_DEV.md > Button specs
- Figma: [Link to component]
- Decision record in git: [Link]
```

---

## 📚 Example: Complete DDR

Here's a real example to follow:

---

## DDR-001: Button Height (44px Minimum)

**Status:** Approved
**Date:** 2025-11-19
**Designer:** Sarah Chen

### The Decision

Establish 44px minimum height for all touch-interactive elements (buttons, inputs, etc.)

### Why This Decision?

Mobile users need sufficient touch targets to tap accurately without mis-taps.
44px is the industry standard (both Apple and Google recommend this).
Testing confirmed users were more comfortable with 44px than 36px.

### What We Explored

- **36px:** Too small, caused mis-taps in testing
- **40px:** Awkward number, not standard anywhere
- **44px:** Industry standard, users comfortable, matches accessibility guidelines
- **48px:** Works great but noticeably larger than needed

### User Validation

Tested button heights with 5 mobile users:

```
"Try tapping these buttons rapidly..."

36px buttons: Users mis-tapped 3-4 times per minute
40px buttons: Users mis-tapped 1 time per minute
44px buttons: Users had 0-1 mis-taps per minute
48px buttons: Users comfortable but remarked "feels a bit big"
```

**Conclusion:** 44px is the sweet spot.

### Trade-offs

```
✅ Mobile friendly (lowest mis-tap rate)
✅ Accessible by default (WCAG standard)
✅ Matches web standards (Apple, Google, Bootstrap)
✅ Works at any screen size
⚠️ Takes more vertical space (forms are taller)
⚠️ Sometimes feels "big" on desktop
❌ Can't make it smaller even when space is tight
```

### Related Components/Decisions

- **Button component** (all variants now 44px min)
- **Input fields** (also 44px min — consistency)
- **Checkboxes** (tap target 44px min)
- **Touch areas** (44px minimum for any interactive element)
- **DDR-002:** Spacing system (built around 44px module)

### What We Learned

**Mobile is different:**
Users on phones have different needs than desktop users. Designing for mobile
first forced better thinking about touch targets. This decision cascaded into
other components.

**User testing validates:**
Our gut said 40px might work. Users proved us wrong. Never skip testing.

**Standards exist for a reason:**
44px is standard because it works. Following standards means your product
works like users expect.

### What We'd Do Differently

Nothing. This decision has been validated across 3 products and 100+ users.

### Status & Next Steps

- ✅ **APPROVED** - Decision locked
- ✅ **IN PRODUCTION** - Used in all current products
- ✅ **DOCUMENTED** - All new designers learn this first
- 🔄 **MONITORING** - Will re-evaluate if we see mis-tap complaints

### Links & References

- DESIGN_SYSTEM.md > Button section
- DESIGN_TO_DEV.md > Button specs
- Figma: [Link to Button component]
- User testing notes: [Link to research doc]

---

## 🗂️ Other Decision Record Examples

Here are other common decisions you'd document:

### Example: Color Palette Decision

```
## DDR-002: Primary Color (Blue #007AFF)

**Decision:** Use blue #007AFF as primary brand color

**Why:**
- Users perceive blue as "safe" and "trustworthy"
- 7:1 contrast ratio (exceeds accessibility standard)
- Tested with color-blind users (visible to all types)
- Differentiates us from competitors (most use blue, ours is distinctive)

**What We Explored:**
- Red: Too aggressive, tested poorly
- Green: Seemed environmental (not our market)
- Orange: Too playful for our serious use case
- Blue: Tested best with users

**Trade-offs:**
✅ Most trustworthy color
✅ Excellent contrast/accessibility
⚠️ Common (many brands use blue)
❌ Slightly less distinctive

**Status:** ✅ APPROVED - In use since Day 1
```

### Example: Spacing System Decision

```
## DDR-003: 8px Grid System

**Decision:** All spacing follows 8px increments (8, 16, 24, 32, 48px)

**Why:**
- 8px divides cleanly into other measurements
- Feels consistent to human eye
- Gives developers predictable values
- Works at all screen sizes

**What We Explored:**
- 10px grid: Doesn't divide evenly
- 8px grid: Clean, standard, works great
- 12px grid: Too large, wasted space

**Trade-offs:**
✅ Predictable spacing
✅ Divides evenly
⚠️ Can't do 7px or 9px spacing (seems pedantic but useful)
✅ Forces consistency

**Status:** ✅ APPROVED - Foundation of design system
```

### Example: Accessibility Decision

```
## DDR-004: WCAG AA Minimum (Aiming for AAA)

**Decision:** All designs must meet WCAG Level AA (aiming for AAA where possible)

**Why:**
- Legal requirement in many jurisdictions
- Ensures product works for everyone
- Better design for all users (not just disabled users)
- Builds brand trust

**What We Explored:**
- A (minimum): Too permissive
- AA (legal standard): What we chose
- AAA (gold standard): Aiming for this

**Trade-offs:**
✅ Inclusive by default
✅ Legal compliance
✅ Better for all users
⚠️ Limits some color combinations
⚠️ Requires testing

**Status:** ✅ APPROVED - Non-negotiable standard
```

---

## 📊 Decision Timeline

Track decisions in order they were made:

```
DDR-001: Button Height (44px)        [2025-11-19] ✅
DDR-002: Primary Color (Blue)        [2025-11-20] ✅
DDR-003: Spacing Grid (8px)          [2025-11-21] ✅
DDR-004: Accessibility (WCAG AA)     [2025-11-22] ✅
DDR-005: Button Style (Solid)        [2025-11-23] ✅
DDR-006: Typography Scale            [2025-11-24] ✅ (In Review)
DDR-007: Icon Style                  [Proposed]
DDR-008: Animation Principles        [Planned]
```

---

## 🎓 Using This to Learn

### For New Designers

Read the DDRs in order:

1. Start with **DDR-001 through DDR-004** (foundational)
2. Then read **DDR-005+** (component decisions)
3. See why each choice was made
4. Apply the same thinking to new decisions

### For Feedback

If someone questions a decision:

```
Engineer: "Why is the button 44px? Seems large."
You: "Check DDR-001. We tested with users and it's the sweet spot."
Engineer: [Reads DDR] "Oh, that makes sense."
```

Instead of explaining it again, you reference the record.

---

## 🔄 Decision Lifecycle

### 1. PROPOSED
```
- You have an idea
- Write DDR with rationale
- Share with team
- Wait for feedback
```

### 2. IN REVIEW
```
- Team gives feedback
- You refine based on input
- Decide if you want to change it
- Gather more data if needed
```

### 3. APPROVED
```
- Decision is locked
- Implement across system
- Update related docs
- Train team on new standard
```

### 4. IN USE
```
- Actively using this decision
- Monitor for issues
- Document learnings
- Share results with team
```

### 5. DEPRECATED (Optional)
```
- Decided to change approach
- Update DDR with rationale
- Create new DDR for new approach
- Update all affected docs
- Example: "We initially chose X, but learned Y. Now doing Z."
```

---

## 🚀 Quick Template (5 Minutes)

If you're in a hurry, use the quick version:

```markdown
## DDR-###: [Decision Name]

**Decision:** [One sentence]

**Why:** [One paragraph]

**Explored:** Option A, Option B, Option C (chose Option B)

**Trade-off:** [One trade-off]

**Status:** [PROPOSED / APPROVED / IN USE]
```

Then expand later if needed.

---

## 📝 When to Create a DDR

### Definitely Create DDR For:
- ✅ Major color choice
- ✅ Component sizing standard
- ✅ Spacing system
- ✅ Typography decisions
- ✅ Accessibility standards
- ✅ Significant design direction

### Maybe Create DDR For:
- ⚠️ Small component updates
- ⚠️ Minor adjustments
- ⚠️ Seasonal updates

### Don't Create DDR For:
- ❌ Pixel-level tweaks
- ❌ One-off exceptions
- ❌ Small bug fixes

**Guideline:** If you spent 30+ minutes deciding it, document it.

---

## 🔗 Related Files

- **DESIGN_PROCESS.md** - How you made the decision
- **DESIGN_SYSTEM.md** - Where the decision lives
- **DESIGN_RESEARCH.md** - User feedback that informed it
- **DESIGN_TO_DEV.md** - How developers implement it

---

## 💡 Pro Tips

### Make Decisions Reversible (When Possible)

Design some decisions as reversible:

```
✅ REVERSIBLE: "We'll use blue for 3 months, measure results, decide"
❌ LOCKED IN: "We'll use blue forever because logo is blue"

Better approach: Make it reversible, measure, then lock in if it works
```

### Document Uncertainty

```
"We think X is best, but we're not 100% sure.
We'll test in 2 weeks and confirm."

[Later: confirmed OR changed to Y based on evidence]
```

### Show Your Work

Include:
- Why you rejected other options
- What users said
- What you tried vs. what worked
- What surprised you

### Update as You Learn

```
Original decision: [What we thought]
What we learned: [What testing revealed]
Updated approach: [New direction based on learning]
```

---

## ✅ Checklist for Each DDR

Before publishing a DDR:

```
☐ Decision is clearly stated in one sentence
☐ Rationale is explained (why this matters)
☐ Options explored are listed (and rejected why)
☐ User validation included (did users agree?)
☐ Trade-offs documented (what did we give up?)
☐ Status is clear (approved? in use? proposed?)
☐ Related decisions are linked
☐ Learnings are captured
```

---

**Remember:**

Your design decisions are valuable institutional knowledge.
Document them so the next designer doesn't reinvent the wheel.
And so you don't forget why you chose blue instead of red.

---

**Next:** DESIGN_RESEARCH.md — What did users tell us?
