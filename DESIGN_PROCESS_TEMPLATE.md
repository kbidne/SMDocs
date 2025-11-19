# 🎬 Design Process: How We Work (With AI)

**Our workflow for creating designs that users love**

> **You are:** Director (not executor)
>
> **AI is:** Tool for exploration (not decision-maker)
>
> **The process:** Explore → Evaluate → Validate → Decide → Document

---

## 🎯 Our Design Philosophy (Process Version)

### What We Believe

**AI is best at:** Generating variations, exploring the design space, suggesting options

**Humans are best at:** Judging what matters, validating with users, making decisions

**Our approach:** Let AI do what it's good at. Save your judgment for what matters.

### The Mindset

```
❌ "Let the AI design it"
   (We don't trust machines with decisions)

✅ "Let AI explore 10 options while I focus on understanding the user"
   (We use AI as a tool to expand possibilities)

✅ "I'll pick the best option based on research"
   (We make the decision)

✅ "I'll test it with users to validate"
   (We verify our judgment)
```

---

## 📋 The Design Process (Step by Step)

### Phase 1: Understand (No AI Yet)

**Goal:** Know what you're actually solving

**Step 1: Define the Problem**

Ask yourself:
- What are users trying to do?
- What's currently hard about it?
- What would make it better?
- How will we know if we succeeded?

**Example:**
```
Problem: Users can't find tasks they created last week

Current state: No filtering, all tasks in one list

Success metric: Users find the task in <30 seconds
```

**Step 2: Set Constraints**

What are the boundaries?
- Brand consistency required?
- Accessibility minimum?
- Mobile or desktop first?
- Space limitations?
- Any technical constraints?

**Example:**
```
Brand color: Blue (#007AFF)
Accessibility: WCAG AA minimum
Platform: Mobile first (iOS/Android)
Space: Must fit in 100px width at 12px font
```

**Step 3: Sketch Core Concept (Hand)**

Before touching AI, draw something:
- Rough wireframe
- Basic layout
- Key elements

This keeps you in the driver's seat.

**Sketch takes:** 15-30 minutes

**Why?** AI will work better if you've already thought through the basics.

---

### Phase 2: Explore (AI Helps)

**Goal:** Generate variations to explore the design space

**Step 1: Write a Design Prompt**

Be specific. The better your prompt, the better the results.

**Prompt Structure:**

```
[WHAT TO CREATE] + [CONSTRAINTS] + [VARIATIONS] + [OUTPUT FORMAT]

Example:
"Create 5 button design variations for a mobile app:
- Each button should be 44px tall minimum
- Blue primary color (#007AFF)
- Explore different visual weights (thin, regular, bold)
- Export as individual PNGs for comparison"
```

**Step 2: Generate Variations**

Use your tool (Figma + plugins, Midjourney, Claude, etc.):
- Get 5-10 options
- Don't overthink — just generate
- Save everything (you'll pick later)

**Time:** 5-15 minutes depending on complexity

**Step 3: Compare & Initial Sort**

Look at all variations:
- Which ones feel right?
- Which ones are way off?
- Do any surprise you?

Narrow to top 3-4 candidates.

**Time:** 10-15 minutes

---

### Phase 3: Evaluate (Human Judgment)

**Goal:** Select the best option based on your constraints

**Step 1: Test Against Constraints**

Go back to Phase 1 constraints:

```
Constraint: 44px tall minimum
✅ Option A: 48px (passes)
❌ Option B: 36px (fails)
✅ Option C: 44px (passes)
```

Eliminate any that fail constraints.

**Step 2: Consider Users**

For each remaining option:
- Would users understand this?
- Does it match their expectations?
- Is it accessible?
- Does it work at all screen sizes?

Test with accessibility tools:
- Color contrast checker
- Screen reader simulation
- Zoom to 200%

**Step 3: Select Your Winner**

Pick ONE that best meets:
1. Constraints
2. User expectations
3. Brand consistency
4. Technical feasibility

**Time:** 15-20 minutes

---

### Phase 4: Validate (Get User Feedback)

**Goal:** Confirm your judgment with real users

**Step 1: Prepare for Testing**

Get your winning design ready:
- Show it clearly
- Show it in context (not isolated)
- Have 1-2 alternatives ready

**Step 2: Test with Users**

Talk to 2-3 users (not a formal study, just conversations):

```
"I'm exploring a new design for [feature].
Here's what we're thinking. What do you think?"

Listen for:
- Do they understand what it does?
- Do they like it?
- Would they use it?
- Any concerns?
```

**Script:**
```
"What do you see in this design?"
[Wait for answer]

"What would you do with it?"
[Wait for answer]

"Any concerns?"
[Wait for answer]

"Would you use this?"
[Wait for answer]
```

**Time:** 30-45 minutes for 2-3 users

**Step 3: Interpret Results**

```
✅ Users understand it → Good sign
✅ Users like it → Good sign
⚠️ Users confused → Refine and re-test
❌ Users don't like it → Pick different option and re-test
```

Document what you learned in DESIGN_RESEARCH.md.

---

### Phase 5: Decide & Document

**Goal:** Lock in the decision and explain why

**Step 1: Create a Decision Record**

Write 1 entry in DESIGN_DECISIONS.md:

```markdown
## DDR-005: Button Style for Primary CTA

**Status:** Approved
**Date:** 2025-11-19
**Designer:** You

**Decision:** Use solid button style with slight shadow

**Why:**
- Tested 5 variations with users
- Users understood solid style fastest
- Meets 44px minimum for accessibility
- Works at mobile sizes (tested at 375px)

**The Process:**
- Hand-sketched initial concept (15 min)
- Generated 5 variations with AI (10 min)
- Compared against constraints (15 min)
- Tested with 3 users (45 min)
- Selected solid style (5 min)

**Trade-offs:**
✅ Clear and understood
✅ Accessible
⚠️ Less unique than alternative
✅ Easier to implement

**User Feedback:**
"That looks like something I'd click"
"Very clear what it does"
"Nice and simple"

**Next Steps:**
- Hand off to developers (see DESIGN_TO_DEV.md)
- Monitor real usage
```

**Time:** 10 minutes to write

**Step 2: Prep for Handoff**

Add entry to DESIGN_TO_DEV.md:

```markdown
## Button: Primary CTA Style

See DDR-005 for decision reasoning.

Specs:
- Height: 44px
- Background: Blue (#007AFF)
- Text: White, 14px, bold
- Padding: 12px top/bottom, 16px left/right
- Border radius: 6px
- Shadow: 0 1px 3px rgba(0,0,0,0.1)

States:
- Hover: Darker blue (#0056CC)
- Active: Pressed effect (shadow down)
- Disabled: Gray (#D1D5DB), opacity 50%

Accessibility:
- Minimum height: 44px ✅
- Color contrast: >4.5:1 ✅
- Keyboard accessible ✅
- Screen reader compatible ✅
```

---

## 🏆 Complete Workflow (Visual)

```
┌─ Phase 1: UNDERSTAND ────────────────────┐
│ • Define the problem                     │
│ • Set constraints                        │
│ • Hand-sketch concept                    │
│ Time: 30-45 minutes                      │
└──────────────────┬──────────────────────┘
                   ↓
┌─ Phase 2: EXPLORE ──────────────────────┐
│ • Write prompt                           │
│ • Generate 5-10 variations               │
│ • Compare & narrow to top 3              │
│ Time: 20-30 minutes                      │
└──────────────────┬──────────────────────┘
                   ↓
┌─ Phase 3: EVALUATE ─────────────────────┐
│ • Test against constraints               │
│ • Consider user impact                   │
│ • Select winner                          │
│ Time: 15-20 minutes                      │
└──────────────────┬──────────────────────┘
                   ↓
┌─ Phase 4: VALIDATE ─────────────────────┐
│ • Test with 2-3 users                    │
│ • Gather feedback                        │
│ • Confirm choice                         │
│ Time: 45 minutes                         │
└──────────────────┬──────────────────────┘
                   ↓
┌─ Phase 5: DECIDE & DOCUMENT ────────────┐
│ • Write decision record                  │
│ • Prepare handoff specs                  │
│ • Ready for implementation               │
│ Time: 15 minutes                         │
└──────────────────────────────────────────┘

TOTAL TIME: 2-2.5 hours per component
RESULT: Intentional design, user-validated, documented
```

---

## 💎 Winning Prompts (Templates)

Save these prompts — they've been tested and work well.

### Prompt Template 1: Button Variations

```
[TOOL: Figma with Generative Fill OR Claude]

"Generate 5 button style variations for a mobile task management app.

Constraints:
- Minimum height: 44px
- Color: Must use primary blue (#007AFF)
- Text should be clear and readable
- Should work well on light backgrounds
- Should look modern but professional

Variations to explore:
1. Solid button
2. Outline button
3. Soft fill button
4. Button with subtle shadow
5. Button with minimal design

Please provide each as a separate option showing:
- Default state
- Hover state
- Pressed state
- Disabled state

Output: PNG files for comparison"
```

**Best tool:** Figma (Generative Fill) or Claude for conceptual

**Time:** 10 minutes to generate + 10 minutes to compare

**Success rate:** 80% (most options are usable)

---

### Prompt Template 2: Spacing Exploration

```
"Generate 5 explorations of spacing and layout for a form with:
- Input fields (email, password)
- Checkbox (remember me)
- Submit button
- Forgot password link

Current spacing uses 16px between elements. Explore:
1. Compact (12px spacing)
2. Standard (16px spacing - current)
3. Spacious (24px spacing)
4. Very spacious (32px spacing)
5. Minimal (8px spacing)

Show how each looks on mobile (375px width).

I want to understand which spacing feels right for mobile users.
Output: Mockups showing all 5 options at mobile size"
```

**Best tool:** Figma or design tool that shows responsive

**Time:** 15 minutes to generate + 15 minutes to evaluate

**Success rate:** 90% (AI is good at variations)

---

### Prompt Template 3: Color Exploration

```
"Generate 5 color palette variations for a productivity app.

Base constraints:
- Primary action color must be blue (but explore shades)
- Must maintain WCAG AA accessibility
- Should feel modern and professional
- Should work for international audience

Explore:
1. Vibrant blue (current: #007AFF)
2. Muted blue
3. Deep blue
4. Light blue
5. Cool blue tone

For each, show:
- Color swatches
- Sample button (to verify contrast)
- Sample form field
- Sample badge/notification

Output: Side-by-side comparison showing all 5 palettes"
```

**Best tool:** Claude or Figma with color tools

**Time:** 10 minutes to generate + 15 minutes to evaluate

**Success rate:** 70% (sometimes needs refinement)

---

### Prompt Template 4: Icon Variations

```
"Generate 5 variations of an icon for [action: e.g., 'save task'].

Requirements:
- Must be simple and recognizable
- Must work at 16px, 24px, and 32px sizes
- Should look professional
- Should match our blue color scheme (#007AFF)

Explore:
1. Checkmark variation
2. Star variation
3. Folder/save variation
4. Document variation
5. Your creative suggestion

For each, show:
- Icon at 16px (small)
- Icon at 24px (medium)
- Icon at 32px (large)
- Icon in button (in context)

Output: PNG file showing all sizes"
```

**Best tool:** Claude or icon tools

**Time:** 10 minutes to generate + 10 minutes to evaluate

**Success rate:** 85% (AI is good at icons)

---

## 🚫 When NOT to Use AI

There are times AI can't help, or makes things worse:

**DON'T use AI for:**
- ❌ Core brand identity (logo, main colors)
- ❌ Major UX decisions (layout strategy, user flows)
- ❌ Accessibility-critical elements (always verify manually)
- ❌ Unique/custom interactions (use your judgment)
- ❌ Final decision-making (that's your job)

**DO use AI for:**
- ✅ Variation generation (10 sizes? Let AI do it)
- ✅ Exploration (what if we tried this?)
- ✅ Speeding up execution (spacing variations)
- ✅ Inspiration (what haven't I considered?)
- ✅ Tedious work (icon alternatives, color combos)

---

## 📊 Time Savings with AI

### Old Way (Without AI)

```
Button design: 3-4 hours
- Sketch concept: 30 min
- Create 1st version: 1 hour
- Create variations: 1.5 hours
- Pick best: 30 min
- Test: 45 min
```

### New Way (With AI)

```
Button design: 2-2.5 hours
- Sketch concept: 15 min
- Write prompt: 10 min
- Generate variations: 10 min
- Compare: 15 min
- Pick best: 10 min
- Test: 45 min
- Document: 10 min
```

**Time saved:** 40% faster
**Quality gained:** User tested (didn't skip this step)
**Value created:** Documented decision (new value)

---

## 🎓 Version Control for Designs

### Design Versions

Track significant design changes:

```
v1.0 - Initial button design (hand-crafted)
  └─ Red/blue variants
  └─ Size: 40px only

v1.1 - Add hover state (based on user feedback)
  └─ Darker color on hover
  └─ Added shadow

v2.0 - Button size variants (AI-generated)
  └─ 32px, 40px, 48px sizes
  └─ All states (default, hover, active, disabled)
  └─ User tested all 3 sizes

v2.1 - Accessibility improvements
  └─ Increased contrast ratio (4.5:1 → 7:1)
  └─ Better focus state
  └─ Verified screen reader compatible
```

### Naming Convention

```
component-variant-version

Examples:
button-primary-v1.0
button-secondary-v2.0
avatar-v3.1
input-text-v1.0
```

---

## 🤝 Collaboration Points

### Where to involve developers

- **After Phase 1 (Understand):** Ping them with constraint list
  - "Is 44px doable?"
  - "Any tech constraints I should know?"

- **After Phase 2 (Explore):** Show top 3 options
  - "Which of these is easiest to implement?"
  - "Any implementation concerns?"

- **After Phase 5 (Decide):** Full handoff
  - See DESIGN_TO_DEV.md for spec

### Where to involve product/stakeholders

- **After Phase 3 (Evaluate):** Show your pick (not all variations)
  - "Here's what we're doing and why"
  - "User tested and confirmed"

- **After Phase 5 (Decide):** Share decision record
  - "Here's the thinking behind this"
  - "Here's what users said"

---

## 🔄 The Iteration Loop

Design is not linear. You might:

```
Phase 1: Understand → Phase 2: Explore → Phase 3: Evaluate
                                              ↓
Phase 1: "Wait, this constraint doesn't work" ← Loop back
                                              ↓
Phase 2: Explore different direction
                                              ↓
Phase 3: Evaluate again
                                              ↓
Phase 4: Validate with users
                                              ↓
Phase 4: Users say "actually could you try..."
                                              ↓
Phase 2: Quick exploration of their idea
                                              ↓
Phase 3: Compare to original
                                              ↓
Phase 4: Final test
                                              ↓
Phase 5: Decide
```

That's normal. Design is iterative.

---

## 📝 Tools We Use

### For Exploration
- Figma (Generative Fill plugin)
- Claude (conceptual exploration)
- Midjourney (visual inspiration)

### For Implementation
- Figma (design file)
- Component libraries (code components)

### For Validation
- User interviews (Zoom + screen share)
- Feedback tools (Figma comments, email)
- Analytics (which designs do users prefer?)

### For Documentation
- Markdown files (this system)
- Git (version control)
- Figma (visual source of truth)

---

## ✅ Checklist for Each Design Decision

Before you move to Phase 5, confirm:

```
PHASE 1: UNDERSTAND
☐ Problem is clearly defined
☐ Constraints documented
☐ Hand sketch exists

PHASE 2: EXPLORE
☐ Prompt written clearly
☐ 5-10 variations generated
☐ Top 3-4 selected

PHASE 3: EVALUATE
☐ All options tested against constraints
☐ Accessibility verified (contrast, size)
☐ Winner selected based on criteria

PHASE 4: VALIDATE
☐ Tested with 2-3 users
☐ User feedback documented
☐ Confirmed choice is right

PHASE 5: DECIDE
☐ Decision record written (DESIGN_DECISIONS.md)
☐ Handoff specs prepared (DESIGN_TO_DEV.md)
☐ Ready for implementation
```

---

## 🚀 Getting Better at This

### First design (this process): 2.5 hours
### Second design: 2 hours (you're faster)
### Third design: 1.5 hours (you know the pattern)
### Tenth design: 1 hour (you're efficient)

The process stays the same, but you get faster at execution.

---

## 🔗 Related Files

- **DESIGN_SYSTEM.md** - The standards you're working within
- **DESIGN_DECISIONS.md** - Where you document each choice
- **DESIGN_RESEARCH.md** - Where you log user feedback
- **DESIGN_TO_DEV.md** - Where you handoff the final design

---

**This process ensures:**
✅ AI does what it's good at (exploration)
✅ You do what you're good at (judgment)
✅ Users validate the choice (reality check)
✅ Everything is documented (institutional knowledge)
✅ Developers understand the why (better implementation)

**That's how you stay valuable in the AI era.**

---

**Next:** DESIGN_DECISIONS.md — How to document your thinking
