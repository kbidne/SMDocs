# 🔗 Design → Developer Handoff

**Complete specs for implementing design components**

> Your job: Give developers everything they need to build correctly the first time
>
> Their job: Build it to spec
>
> How to succeed: Clear communication of what matters and why

---

## 🎯 Handoff Philosophy

### What Developers Need

❌ A Figma file (they can't implement visual design directly)
❌ Your opinions ("I think this looks better")
❌ Vague suggestions ("make it look good")

✅ Clear specifications (sizes, colors, spacing)
✅ Visual examples + specs
✅ Edge cases documented
✅ Implementation guidance
✅ The reasoning (why you chose this)

### How to Hand Off

```
Step 1: Prepare specs
Step 2: Create visual guide
Step 3: Link to decision record (why you chose this)
Step 4: Document edge cases
Step 5: Share with developer, ask for questions
```

---

## 🏗️ Handoff Template

For each component you're handing off:

```markdown
## Component: [Component Name]

### Overview

**What it is:** [One sentence describing the component]

**Used for:** [What do users do with this?]

**Where it appears:** [What pages/features]

**Figma reference:** [Link to component in Figma]

### Design Decision

This component design came from:
- See DDR-### for decision reasoning
- [Link to design decision record]

Users tested this and preferred it because:
- [Insight from user research]

### Visual Spec

**Desktop (1024px+):**
```
[ASCII diagram or description]
```

**Tablet (768px):**
```
[ASCII diagram or description]
```

**Mobile (375px):**
```
[ASCII diagram or description]
```

### Detailed Specifications

#### Sizing

| Element | Size | Reasoning |
|---------|------|-----------|
| Component height | 44px | Accessibility minimum, users tested |
| Button text | 14px | Readable on mobile, matches system |
| Internal padding | 12px V, 16px H | Spacing system (8px grid) |

#### Colors

| Element | Color | Value | Contrast | Notes |
|---------|-------|-------|----------|-------|
| Background | Blue | #007AFF | 4.5:1 | Primary action color |
| Text | White | #FFFFFF | 19:1 | High contrast for accessibility |
| Hover | Dark Blue | #0056CC | 6.5:1 | Still accessible |
| Disabled | Gray | #D1D5DB | N/A | Not interactive |

#### Typography

| Element | Font | Size | Weight | Line Height |
|---------|------|------|--------|------------|
| Button text | System font | 14px | 600 bold | 1.4 (20px) |

#### Spacing

- Padding: 12px top/bottom, 16px left/right
- Minimum spacing from other elements: 16px
- Spacing between multiple buttons: 8px

### States & Interactions

#### Default State
```
Visual: Solid blue button, text white, no shadow
Color: #007AFF on white background
Cursor: pointer
```

#### Hover State (Desktop Only)
```
Visual: Darker blue, slight shadow
Color: #0056CC
Shadow: 0 2px 8px rgba(0,0,0,0.15)
Transition: 150ms ease
```

#### Active State (Click/Tap)
```
Visual: Even darker, shadow goes down
Color: #004085
Shadow: 0 1px 4px rgba(0,0,0,0.2) inset
Transition: immediate
```

#### Focus State (Keyboard)
```
Visual: 2px blue outline around button
Outline: 2px solid #007AFF, 2px offset
Shown: When user tabs to button
Cursor: pointer
```

#### Disabled State
```
Visual: Gray, 50% opacity, no interaction
Color: #D1D5DB
Opacity: 50%
Cursor: not-allowed
Text: Gray (#9CA3AF)
No hover effect
```

#### Loading State (If Applicable)
```
Visual: Spinner inside button, text hidden
Spinner: 16px animated circle (100ms per rotation)
Disabled: Can't click during loading
```

### Responsive Behavior

#### Desktop (1024px+)
- [Size/spacing details]
- [Behavior]

#### Tablet (768px - 1023px)
- [Size/spacing details]
- [Behavior]

#### Mobile (< 768px)
- [Size/spacing details]
- [Important: Never less than 44px height]

### Accessibility Requirements

All implementations must:

- ✅ **Size:** Minimum 44px height (48px with padding)
- ✅ **Contrast:** All text >4.5:1 ratio
- ✅ **Focus:** Visible focus state on keyboard
- ✅ **Keyboard:** Fully operable via keyboard (Tab, Enter)
- ✅ **Screen readers:** Clear label/aria-label
- ✅ **Icons:** If icon-only button, must have aria-label

**Test with:**
- Keyboard-only navigation (Tab through page)
- Screen reader (Chrome + ChromeVox extension)
- Color blindness simulator
- Zoom at 200%

### Implementation Notes

**Important edge cases:**

```
Edge Case 1: Very long button text
- If text is longer than button width
- Text should wrap to 2 lines
- Button height increases to 56px minimum
- Show example in Figma

Edge Case 2: Icon + Text
- Icon on left, text on right
- Icon: 20px square
- Icon spacing: 8px from text
- Total button can be 48px+ height

Edge Case 3: Disabled with Tooltip
- Some buttons show tooltip on hover explaining why disabled
- Only on hover, not visible by default
- Use .sr-only or aria-label for screen readers

Edge Case 4: Loading State Duration
- User sees spinner during API call
- If takes >3 seconds, show percentage or message
- After 60 seconds, show error state
```

### Design Variations

This component has variants. Implement all:

#### Variant 1: Primary Button
[Colors, sizing, when to use]

#### Variant 2: Secondary Button
[Colors, sizing, when to use]

#### Variant 3: Danger Button
[Colors, sizing, when to use]

### Animation & Transitions

**Hover transition:** 150ms ease-in-out
- Smoothly changes color
- Shadow appears gradually

**Active transition:** Immediate (no delay)
- Should feel responsive

**Focus outline:** Static (no animation)
- Always visible when focused

### Browser Support

This component must work on:
- Chrome (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Edge (latest 2 versions)
- iOS Safari (12+)
- Chrome Mobile (latest)

**Test on actual devices if possible.** Simulators miss touch feels.

### Related Components

This component relates to:
- [Other buttons] - Keep sizing consistent
- [Inputs] - Use same spacing
- [Forms] - Works as part of form groups

See DESIGN_SYSTEM.md for complete system.

### Questions for Implementation

Before you start, please confirm:

1. "Is 44px minimum height a hard requirement or flexible?"
   - **Answer:** Hard requirement (accessibility/user testing)

2. "Should the button take full width on mobile?"
   - **Answer:** [Yes/No] — [Reasoning]

3. "What happens if button text is very long?"
   - **Answer:** [Wrap/Truncate/Grow] — [Show in Figma]

4. "How should loading state work?"
   - **Answer:** [Show spinner/message] — [See Figma mockup]

5. "Any browser-specific considerations?"
   - **Answer:** [None known, but test Safari on iOS]

### Testing Checklist

Once you build this, please test:

```
☐ Looks correct in Figma (pixel perfect if possible)
☐ All states work (default, hover, active, focus, disabled)
☐ Responsive (test at 375px, 768px, 1024px)
☐ Keyboard accessible (Tab, Enter, Space)
☐ Screen reader reads button correctly
☐ Meets color contrast (4.5:1 minimum)
☐ Touch target 44px+ on mobile
☐ Touch feels responsive (not laggy)
☐ Works on Chrome, Firefox, Safari
☐ Works on iOS Safari
☐ Edge cases handled (long text, etc)
```

### Review Process

Once you finish:

1. Share a link to the implementation
2. I'll review against specs
3. We'll iterate if needed
4. Once approved, move to production

### Success Criteria

✅ You built this exactly as specified
✅ All states look correct
✅ It's accessible
✅ It's responsive
✅ No surprises or deviations

If anything is confusing, ask before building. Saves re-work later.

### Support

Questions during implementation?
- "What does this spec mean?" → Ask me
- "Should I do X or Y?" → Ask me
- "This constraint seems wrong" → Ask me
- "I found a better way" → Tell me, show me

I'm here to help you build this right.

### Links

- **Figma:** [Link to component]
- **Design Decision:** [Link to DDR]
- **Design System:** [Link to DESIGN_SYSTEM.md]
- **User Research:** [Link to DESIGN_RESEARCH.md]
```

---

## 📚 Example: Complete Button Handoff

---

## Component: Primary Action Button

### Overview

**What it is:** Large blue button for primary calls-to-action

**Used for:** Main actions users should take (Create, Save, Submit, etc.)

**Where it appears:** Forms, modals, action bars, cards

**Figma reference:** [Link to Figma file]

### Design Decision

See **DDR-001: Button Height (44px Minimum)** for reasoning.

Users tested this design and preferred it because:
- 44px felt natural and easy to tap on mobile
- Users had zero mis-taps compared to 3-4 mis-taps at 36px
- Blue color clearly indicates "clickable action"

### Visual Spec

**Mobile (375px):**
```
┌─────────────────────────┐
│                         │
│    [ Create Task ]      │ ← 44px tall
│                         │
└─────────────────────────┘
  Blue background, white text
```

**Desktop (1024px+):**
```
[Create Task]  ← 40px tall (can be smaller on desktop)
```

### Detailed Specifications

#### Sizing

| Element | Mobile | Desktop | Reasoning |
|---------|--------|---------|-----------|
| Height | 44px | 40px | Users need larger tap target on mobile |
| Width | Full width or 200px | 200px | Full width on mobile, fixed on desktop |
| Text size | 14px | 14px | Readable on all sizes |
| Padding | 12px V, 16px H | 12px V, 16px H | Consistent spacing |

#### Colors

| State | Color | Value | Contrast | Accessibility |
|-------|-------|-------|----------|---|
| Default | Primary Blue | #007AFF | 4.5:1 on white | ✅ AA |
| Hover | Dark Blue | #0056CC | 6.5:1 on white | ✅ AAA |
| Active | Even darker | #004085 | 8:1 on white | ✅ AAA |
| Disabled | Gray | #D1D5DB | N/A | Not interactive |

**Important:** Never use color alone to convey state. Use text/shadow/outline changes.

#### Typography

- Font: System default (-apple-system, Segoe UI, Roboto)
- Size: 14px
- Weight: 600 (bold)
- Color: White (#FFFFFF)
- Line height: 1.4 (20px)
- Letter spacing: 0 (normal)

#### Spacing

- Internal padding: 12px top/bottom, 16px left/right
- Minimum spacing from other elements: 16px
- When two buttons side by side: 8px gap between them

### States & Interactions

#### Default State
```
Visual: Solid blue button
Color: #007AFF (Primary)
Text: White, bold, 14px
Shadow: 0 1px 3px rgba(0,0,0,0.1) (subtle)
Cursor: pointer
```

#### Hover State (Desktop/Tablet with mouse)
```
Visual: Slightly darker blue, more shadow
Color: #0056CC
Shadow: 0 4px 12px rgba(0,0,0,0.15)
Transition: 150ms ease-in-out
Do NOT change on touch (mobile shouldn't have hover)
```

#### Active State (Pressing/Tapping)
```
Visual: Pressed feeling (shadow goes down)
Color: #004085
Shadow: 0 1px 4px rgba(0,0,0,0.2) inset
Transition: Immediate (feels responsive)
```

#### Focus State (Keyboard Navigation)
```
Visual: 2px blue outline, 2px offset from button
Outline: 2px solid #007AFF
Offset: 2px away from button edge
Visible: When Tab to button, should always be visible
Do NOT remove for accessibility reasons
```

#### Disabled State (Button Can't Be Used)
```
Visual: Grayed out, no interaction
Color: #D1D5DB (Gray)
Text: #9CA3AF (Darker gray)
Opacity: 50% (looks faded)
Cursor: not-allowed
No hover effect: Should not change on hover
No click: Clicking does nothing
Reason text: Optional tooltip explaining why
```

#### Loading State (If Applicable)
```
Visual: Spinner inside, text hidden
Spinner: 16px circular loader, 100ms per rotation
Color: White (visible on blue background)
Button disabled: Can't click during loading
After 3 seconds: Show "Loading..." text if still loading
After 60 seconds: Timeout error
```

### Responsive Behavior

#### Mobile (< 768px)
- Width: Full width (minus safe margins)
- Height: 44px minimum (user testing)
- Margin: 16px on sides, 16px spacing below
- Text: 14px (readable without zoom)

#### Tablet (768px - 1023px)
- Width: 200px (centered or grouped with other buttons)
- Height: 40px
- Text: 14px

#### Desktop (1024px+)
- Width: 200px (can be 160px to 240px)
- Height: 40px
- Text: 14px
- Spacing from other elements: 16px

### Accessibility Requirements

✅ **Height:** Minimum 44px (including padding) on touch devices

✅ **Contrast:** White on blue is 4.5:1 (meets WCAG AA)

✅ **Focus State:** Always visible blue outline when tabbed to

✅ **Keyboard:** Activated by Enter or Space key

✅ **Screen Readers:** Has clear label or aria-label
```
Bad: <button>→</button> (icon only, no label)
Good: <button aria-label="Create task">→</button>
```

✅ **Not disabled by visual design alone:** Color + opacity + text

**Must test with:**
- Keyboard navigation (Tab key)
- Screen reader (NVDA on Windows or VoiceOver on Mac)
- Chrome color blindness simulator
- Zoom at 200%

### Implementation Notes

**Edge Case 1: Very Long Button Text**
```
Text: "Create a new task and assign it to team"
Behavior: Wrap to 2 lines (width: 200px max)
Height: Increase to 56px to accommodate
Padding: Still 12px top/bottom
Never truncate important text
```

**Edge Case 2: Icon + Text**
```
[→ Create Task]
Icon: 20px square
Icon-to-text spacing: 8px
Button height: 48px minimum
Text: Still 14px
```

**Edge Case 3: Icon Only**
```
[✓]
Must have aria-label="Confirm"
Never an unlabeled icon button
Touch target: Still 44px minimum
```

**Edge Case 4: Mobile vs. Desktop Hover**
```
Desktop: Show hover effect (change color, shadow)
Mobile: Do NOT show hover (there's no hover on touch)
Only show active/pressed state on mobile

CSS solution:
@media (hover: hover) {
  button:hover { /* hover effect */ }
}
```

### Design Variations

While this is "Primary Button," related buttons:

**Secondary Button:**
- Same height (44px)
- White background, blue border
- Blue text
- Used for secondary actions

**Danger Button:**
- Same height (44px)
- Red background (#EF4444)
- White text
- Used for destructive actions (Delete, Remove)

All variants follow the same structure and spacing.

### Animation & Transitions

**Color transitions:** 150ms ease-in-out
- Smooth color change on hover
- Makes it feel responsive

**Shadow transitions:** 150ms ease-in-out
- Smooth shadow appearance
- Reinforces depth

**Active state:** 0ms (no delay)
- Should feel immediate when clicked
- User feedback that action was registered

**Focus outline:** Static (no animation)
- Always visible, doesn't pulse
- Clear keyboard navigation

### Browser Support

Must work on:
- Chrome 90+ (desktop)
- Firefox 88+ (desktop)
- Safari 14+ (desktop)
- Edge 90+ (desktop)
- iOS Safari 14+ (mobile)
- Chrome Mobile 90+ (mobile)
- Samsung Internet 14+ (mobile)

**Important:** Test on real devices if possible. Simulators miss touch feels.

### Related Components

Consistency across related items:

- **Secondary Button:** Same height, different color
- **Input Fields:** Also 44px on mobile (consistent touch targets)
- **Checkboxes:** 44px touch target
- **Tabs:** 44px height on mobile

See DESIGN_SYSTEM.md for full system.

### Questions for Implementation

Before you build, confirm:

**Q: Should the button be full width on mobile or fixed width?**
A: Full width (with 16px margins). User testing showed users expect this on mobile.

**Q: How does loading state show? Spinner only?**
A: Spinner inside button + text hidden. After 3 seconds, show "Loading..." if still going.

**Q: What if button text is very long?**
A: Wrap to 2 lines, increase height to 56px, keep padding consistent.

**Q: Should this button redirect or submit a form?**
A: [Context dependent — specify in your case] Typically submits form (use `<button type="submit">`)

**Q: Any browser-specific concerns?**
A: None known, but test on iOS Safari (sometimes different touch behavior).

### Testing Checklist

Once you build this:

```
☐ Visual matches Figma (pixel perfect if possible)
☐ Works on mobile (375px width)
☐ Works on tablet (768px width)
☐ Works on desktop (1024px width)
☐ Hover state works (change color + shadow)
☐ Active state feels responsive (pressed effect)
☐ Focus outline visible on Tab
☐ Disabled state grayed out
☐ Loading state shows spinner if applicable
☐ Keyboard: Activates on Enter or Space
☐ Screen reader announces button + label
☐ Contrast meets WCAG AA (test with tool)
☐ Touch target 44px+ on mobile
☐ No console errors
☐ Works on Chrome, Firefox, Safari
☐ Works on iOS and Android
```

### Review Process

1. **Before building:** Ask questions if specs unclear
2. **While building:** Reach out if you hit issues
3. **When done:** Share implementation link
4. **I review:** Compare against specs
5. **You iterate:** Fix any mismatches
6. **Approval:** Once perfect, move to production

### Success Criteria

✅ Matches Figma pixel-perfect (or close)
✅ All states work correctly
✅ Responsive and mobile-friendly
✅ Fully accessible (keyboard, screen reader)
✅ No surprises or undocumented behaviors

If anything is confusing, **ask before you build**. Clear communication now saves re-work later.

### Support & Communication

- **Questions?** Slack/email me anytime
- **Stuck?** Show me what you have, we'll figure it out
- **Better idea?** Show me, explain, we'll discuss
- **Concerns?** Tell me, we'll solve together

Let's build this right the first time.

---

## 🎯 Handoff Checklist

Before you give specs to developer:

```
PREPARATION
☐ Figma component is finalized
☐ All states are designed (default, hover, active, focus, disabled)
☐ All sizes are specified (mobile, tablet, desktop)
☐ Accessibility verified (contrast, size, keyboard)
☐ Design decision record written (DDR)
☐ Edge cases documented
☐ User research available

DOCUMENTATION
☐ Specs document is clear
☐ Visual examples shown (ASCII or screenshots)
☐ Colors with hex values
☐ Sizes in pixels
☐ Spacing documented
☐ States clearly explained
☐ Accessibility requirements listed

COMMUNICATION
☐ Shared with developer
☐ Walked through specs together (sync call)
☐ Developer confirmed understanding
☐ Questions answered
☐ Concerns addressed
☐ Developer knows to ask if unclear

POST-HANDOFF
☐ Developer builds it
☐ You review implementation
☐ You give feedback
☐ Developer iterates
☐ Final approval
☐ Shipped to production
```

---

## 🤝 Developer-Designer Collaboration

### What Developers Need From You

✅ **Clear specs** (not ambiguous)
✅ **Edge cases documented** (what if text is long?)
✅ **Rationale** (why you chose this)
✅ **Visual examples** (show me, don't just describe)
✅ **Accessibility requirements** (how should this work?)
✅ **Browser/device details** (what needs to work?)

### What You Need From Developers

✅ **Questions** (if specs are unclear)
✅ **Challenges** (technical constraints you didn't know about)
✅ **Implementation feedback** (does this feel right?)
✅ **Performance concerns** (will this be slow?)
✅ **Browser compatibility** (any issues on old Safari?)

### The Best Collaboration

```
Designer: "Here's the spec and why"
Developer: "Looks good, I see one edge case: what if...?"
Designer: "Good catch! [Answers]"
Developer: "Perfect, building now"
[Developer builds]
Developer: "Done, check it out"
Designer: "Looks great! One tiny adjustment..."
Developer: "Fixed"
Both: "Ship it!"
```

Clear communication > perfect specs

---

**Remember:**

Your job: Give developers everything they need.
Their job: Build it right.
Both jobs: Ask questions early.

---

**This completes the Design Bootstrap. Next: DESIGN_QUICKSTART.md**
