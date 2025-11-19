# 🎨 Design System: [YOUR_BRAND]

**Your design source of truth**

> **For:** Designers (building in Figma), Developers (implementing), Stakeholders (understanding)
>
> **Use this to:** Explain WHY each component exists and behaves the way it does
>
> **Link to:** Your Figma file for visual reference

---

## 🎯 Design System Philosophy

Before we list components, here's why we do design this way:

**Our Approach:**
- [Consistency over creativity] - Users should recognize patterns
- [Accessibility first] - Works for everyone, not most people
- [User research informed] - Decisions based on what we learned
- [Developer-friendly] - Can be built reliably
- [Flexible within constraints] - Designers have options, but within system

**What This Means:**
- All buttons look similar (but have purpose variants)
- Spacing follows a grid (usually 8px)
- Colors are accessible (WCAG AA minimum)
- Components are documented (developers understand why)

---

## 📚 Navigation

- [Color System](#-color-system) - Our palette
- [Typography](#-typography) - Type scale and rules
- [Spacing](#-spacing) - Grid system
- [Components](#-components) - Buttons, inputs, cards, etc.
- [Patterns](#-patterns) - Reusable solutions
- [States & Interactions](#-states--interactions) - How things respond
- [Accessibility Standards](#-accessibility-standards) - Everyone included
- [Using This System](#-using-this-system) - Rules and flexibility

---

## 🎨 Color System

### Primary Palette

| Color | Value | Use | WCAG AA | Notes |
|-------|-------|-----|---------|-------|
| **Brand Blue** | #007AFF | Primary actions, links | ✅ On white | Main CTA buttons |
| **Neutral Dark** | #1F2937 | Text, primary content | ✅ On any | 95% of body text |
| **Neutral Light** | #F3F4F6 | Backgrounds, dividers | ✅ With dark text | Card backgrounds |
| **Success Green** | #10B981 | Completed states, success | ✅ On white | Forms, status |
| **Warning Amber** | #F59E0B | Warnings, caution | ✅ On white | Alert states |
| **Error Red** | #EF4444 | Errors, dangerous actions | ✅ On white | Validation, delete |

### How We Use Color

**Primary Action:**
- Brand Blue (#007AFF) on light backgrounds
- Always uses sufficient contrast

**Text:**
- Dark text on light backgrounds (#1F2937)
- Light text on dark backgrounds (#F3F4F6)

**Status Colors:**
- Green = Success / Completed
- Amber = Warning / In progress
- Red = Error / Blocked

### Why This Matters

Users worldwide expect:
- Blue = clickable
- Green = good
- Red = danger
- Gray = disabled

Deviating confuses people.

---

## 🔤 Typography

### Type Scale

```
Heading 1    32px  bold   line-height: 1.2  [Page titles]
Heading 2    24px  bold   line-height: 1.3  [Section titles]
Heading 3    18px  semi   line-height: 1.3  [Subsections]

Body Large   16px  normal line-height: 1.5  [Primary content]
Body         14px  normal line-height: 1.5  [Default]
Caption      12px  normal line-height: 1.4  [Metadata, timestamps]
Tiny         11px  normal line-height: 1.3  [Error messages]
```

### Font Stack

```
Sans-serif: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial
Serif:      Georgia, serif
Mono:       "Courier New", monospace
```

### When to Use Each

| Level | Use Case | Example |
|-------|----------|---------|
| **Heading 1** | Page title only | "Your Tasks" (main page) |
| **Heading 2** | Major section | "Assigned to me", "In progress" |
| **Heading 3** | Subsection | "Due this week" |
| **Body Large** | First paragraph of explanation | Form descriptions |
| **Body** | 90% of text | Copy in buttons, labels, etc. |
| **Caption** | Secondary info | "Created on Nov 19" |
| **Tiny** | Error messages, helper text | "Email is required" |

### Line Length Rule

Keep text to 50-75 characters per line for readability.

```
Good:  This is easy to read because
       the line length is reasonable.

Bad:   This is harder to read because the line length is too long and your eye has to travel too far across the screen which is exhausting.
```

---

## 📏 Spacing System

### The 8px Grid

Everything aligns to 8px increments:

```
8px   - Tight spacing (rarely used)
16px  - Default spacing between elements
24px  - Larger spacing (section breaks)
32px  - Page-level spacing
48px  - Major section spacing
```

### Common Spacing Patterns

| Component | Spacing | Example |
|-----------|---------|---------|
| **Button padding** | 12px vertical, 16px horizontal | Button interior |
| **Input padding** | 12px vertical, 16px horizontal | Form fields |
| **Card padding** | 24px | Card interior |
| **Element margins** | 16px between | List items, cards |
| **Section spacing** | 32-48px | Between major sections |

### Why 8px?

- Divides into 16, 24, 32, 48 evenly
- Feels consistent to the human eye
- Easier for developers to implement
- Works at any screen size

---

## 🔘 Components

This is your component library, documented. Each component should have:
- **What it is** - Purpose
- **Variants** - Different versions
- **States** - How it responds
- **Accessibility** - Who can use it
- **When to use** - Guidelines

### Button

**Purpose:** Call user to action. Make them click something.

**Variants:**

| Variant | Color | Use | Example |
|---------|-------|-----|---------|
| **Primary** | Blue (#007AFF) | Main CTA | "Create task", "Save" |
| **Secondary** | Gray outline | Alternative action | "Cancel", "Skip" |
| **Danger** | Red (#EF4444) | Destructive | "Delete", "Remove" |
| **Disabled** | Gray faded | Not available | (Any button when no data) |

**Sizes:**

```
Button Sizes:
┌────────────────┐
│   24px button  │  [Extra small - rarely used]
├────────────────┤
│   32px button  │  [Small - sidebars, compact]
├────────────────┤
│   40px button  │  [Standard - most common]
├────────────────┤
│   48px button  │  [Large - mobile CTAs]
└────────────────┘
```

**Minimum touch target:** 44px x 44px (WCAG standard)

**States:**

```
Default:    Blue, full opacity, cursor: pointer
Hover:      Slightly darker blue, shadow appears
Active:     Pressed effect (shadow down)
Disabled:   Gray, 50% opacity, cursor: not-allowed
Loading:    Spinner inside, text hidden
```

**Accessibility:**

- ✅ Minimum 44x44px (easy to tap on mobile)
- ✅ Clear contrast (>4.5:1 color ratio)
- ✅ Clear text label (never icon-only without aria-label)
- ✅ Focus state visible (border or outline on tab)
- ❌ Never rely on color alone (add text or icon)

**When to use:**

- ✅ Primary action user should take
- ✅ Form submission
- ❌ Navigation (use links instead)
- ❌ Destructive action without confirmation

**Related:**
- See DESIGN_DECISIONS.md for why we chose 44px minimum
- See DESIGN_TO_DEV.md for implementation specs

---

### Input Field

**Purpose:** Get information from users (text, email, password, etc.)

**Variants:**

```
Text input:     [User types here]
Email input:    [user@example.com]
Password:       [••••••••]
Search:         [🔍 Search...]
Textarea:       [Multi-line input]
Number:         [  123  ]
```

**States:**

```
Empty:      Placeholder text visible, gray border
Focused:    Blue border, cursor inside
Filled:     User has entered text
Error:      Red border, error message below
Disabled:   Gray, no interaction possible
Loading:    Spinner inside (during validation)
```

**Sizes:**

- **Minimum height:** 40px (44px with padding)
- **Width:** Should adapt to container (not fixed)
- **Padding:** 12px vertical, 16px horizontal

**Labels & Help Text:**

```
Label (required)
[Input field]
Helper text or error message below
```

Every input needs:
- A visible label (not placeholder alone)
- Optional: Help text explaining what we want
- Optional: Error message if wrong

**Accessibility:**

- ✅ Always paired with visible label
- ✅ Placeholder is NOT a label substitute
- ✅ Error messages linked to input (aria-describedby)
- ✅ Password fields have "show password" option
- ✅ Minimum 44px height (easy to tap)

**When to use:**

- ✅ Getting user information
- ✅ Search functionality
- ❌ If it's a yes/no → Use toggle instead
- ❌ If it's multiple choice → Use dropdown instead

---

### Card

**Purpose:** Container for grouped information.

**Structure:**

```
┌─ Card ─────────────────────────┐
│ (24px padding)                 │
│                                │
│  Heading (optional)            │
│  Some content goes here        │
│                                │
│  [Secondary Action] [Primary]  │
│ (optional buttons)             │
│                                │
└────────────────────────────────┘
```

**Styling:**

- Background: White (#FFFFFF)
- Border: 1px light gray (#E5E7EB)
- Padding: 24px all around
- Border radius: 8px
- Shadow: Light (0 1px 3px rgba(0,0,0,0.1))

**Variations:**

| Variant | Use | Example |
|---------|-----|---------|
| **Outlined** | Default card | Task card, profile |
| **Elevated** | Important card | Featured item |
| **Flat** | Minimal emphasis | List items |

**When to use:**

- ✅ Grouping related information
- ✅ List items
- ✅ Dashboard widgets
- ❌ If it's just text → Use plain text section

---

### (Add more components here)

Continue the pattern for:
- Modals
- Dropdowns
- Checkboxes
- Radio buttons
- Toggles
- Tabs
- Breadcrumbs
- Badges
- etc.

---

## 🎭 Patterns

Patterns are solutions to common design problems.

### Pattern: Form Validation

**Problem:** Users submit invalid forms and get confused by errors

**Solution:**
```
1. Real-time validation (as they type)
2. Clear error messages (not "Error" — say what's wrong)
3. Highlighting the field that has the issue
4. Helper text showing what's required

Example:
┌─────────────────────────────┐
│ Email (required)            │
│ [user@example    ]          │
│ ⚠️ Must be valid email      │
└─────────────────────────────┘
```

**When to use:** Every form

**Edge cases:**
- Async validation (check if email exists)
- Match fields (password confirmation)
- Conditional validation (show if X is selected)

---

### Pattern: Empty States

**Problem:** What shows when there's no data?

**Solution:**
```
┌─────────────────────────────┐
│                             │
│    📭 No tasks yet         │
│                             │
│  Create your first task     │
│   [Create New Task] ────────→ Button
│                             │
└─────────────────────────────┘
```

**Include:**
- Icon (visual, not text)
- Friendly message
- Clear next action (button)

---

### Pattern: Loading States

**Problem:** Users don't know if something is working

**Solution:**
```
Show something happening:
- Skeleton screens (gray boxes where content goes)
- Spinners (animated circle)
- Progress bar (if you know how long)

Never: Silent loading, blank screen, or lag
```

---

## 🔄 States & Interactions

### Standard States (All Components)

```
DEFAULT     Component is ready to use
HOVER       User is pointing at it
ACTIVE      User is clicking/selecting it
FOCUS       User tabbed to it (keyboard)
DISABLED    Can't be used right now
LOADING     In progress
ERROR       Something went wrong
SUCCESS     Action completed
```

### State Transitions

States should transition smoothly:

```
Default → Hover (150ms fade)
Hover → Active (immediate)
Active → Success (200ms)
Success → Default (after action)
```

### Focus States (Keyboard Navigation)

Every interactive element needs visible focus:

```
Default:  [Button]
Focused:  [Button with 2px blue outline]
```

Why? People use keyboards. Show them where they are.

---

## ♿ Accessibility Standards

Every component must meet:

**WCAG Level AA (legal minimum):**
- ✅ 4.5:1 color contrast (text)
- ✅ 3:1 color contrast (large text)
- ✅ 44x44px minimum touch target
- ✅ Keyboard navigation (everything accessible)
- ✅ Alt text for images
- ✅ Form labels properly associated
- ✅ Focus visible (outline/border)

**Our stretch goal: WCAG Level AAA** (even better)
- 7:1 contrast ratio
- Better keyboard support
- Voice control compatible

**Test with:**
- Keyboard only (no mouse)
- Screen reader (NVDA or JAWS)
- Color blindness simulator
- Zoom at 200%
- At 18px text minimum

---

## 📋 Using This System

### For Designers

**When creating new components:**

1. **Check if it already exists**
   - Browse this system (DESIGN_SYSTEM.md)
   - Check your Figma file
   - Don't duplicate

2. **If creating new, document it here**
   - Purpose
   - Variants & sizes
   - States
   - Accessibility requirements
   - When to use

3. **Add to Figma**
   - Create component
   - Add variants
   - Publish to library
   - Link in this doc

**When using existing components:**

- Follow the variants (don't create custom sizes)
- Respect spacing rules
- Maintain color consistency
- Test accessibility (you're responsible)

### For Developers

**When implementing:**

1. **Read this file** for understanding
2. **Check the Figma file** for visuals
3. **Follow the specs exactly**
   - Sizes, colors, spacing
   - States and interactions
   - Accessibility requirements

4. **Ask if you're unsure**
   - "Is this flexible or fixed?"
   - "What's the intention here?"
   - "Any edge cases I should know?"

### For Stakeholders

**To understand the system:**

1. **See the Figma file** for visuals
2. **Read this document** for rationale
3. **Understand it's intentional**
   - These choices are made for reasons
   - Consistency over uniqueness
   - Accessibility from start, not bolted on

---

## 🔄 Maintaining This System

**Weekly:**
- Check: Any new components created? Document them.

**Monthly:**
- Review: Do components still feel right?
- Test: Accessibility still good?

**Quarterly:**
- Audit: Is everything being used?
- Cleanup: Remove components no longer needed

---

## 🎨 Visual Reference

Your Figma file is the visual source of truth.

**This document** explains the why, the rules, and the thinking.

**Use both together:**
- Figma = See it
- This doc = Understand it
- Combined = Use it correctly

---

## 📝 Design Decisions Related to This System

Each major component has a decision record:

- **DDR-001: Why 44px minimum buttons?** [Link]
- **DDR-002: Why 8px grid?** [Link]
- **DDR-003: Color palette choices** [Link]

See DESIGN_DECISIONS.md for the reasoning.

---

## 🤔 Common Questions

**Q: Can I use a color outside this palette?**
A: No, unless approved by design lead. Consistency matters more than uniqueness.

**Q: Can I make a button 36px instead of 40px?**
A: No. 40px is our standard. If 40px doesn't work, we have a 32px variant.

**Q: What if 44px minimum doesn't fit my design?**
A: 44px is not optional — it's for accessibility. If it doesn't fit, rethink the design.

**Q: When can I deviate from this system?**
A: Rarely. Maybe 5% of components. Document why in DESIGN_DECISIONS.md.

---

## 🔗 Related Files

- **DESIGN_PROCESS.md** - How to extend this system with AI
- **DESIGN_DECISIONS.md** - Why each choice was made
- **DESIGN_TO_DEV.md** - How to hand off components
- **Figma** - Visual reference

---

**This system is your north star.**
When in doubt, reference it.
When you want to break it, document why first.

---

**Next:** DESIGN_PROCESS.md — How to use AI to extend this system
