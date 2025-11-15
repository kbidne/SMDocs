# Self-Documenting Project Bootstrap

This directory contains templates for bootstrapping a self-documenting process in any project, optimized for working with AI agents like Claude Code across multiple sessions.

## What's Included

### Core Templates

1. **claude.md** - Instructions for AI agents working on your project
   - Documentation maintenance workflow
   - Git and commit guidelines
   - Quality standards
   - Project-specific conventions

2. **document-index.md** - Central registry of all project documentation
   - Tracks all documents with timestamps
   - Maintains cross-reference map
   - Monitors document freshness
   - Provides quick navigation

## Why Use This System?

This self-documenting system solves common problems in projects that use AI agents:

- **Context Loss Between Sessions** - New AI sessions can quickly understand the project state
- **Documentation Drift** - Mandatory sync rules keep docs consistent
- **Missing Cross-References** - Bidirectional linking ensures no orphaned documents
- **Outdated Information** - Timestamp tracking highlights stale docs
- **Onboarding Friction** - New contributors (human or AI) can navigate easily

## How to Bootstrap a New Project

### Step 1: Copy Templates

Copy these files to your project root:
```bash
cp claude.md /path/to/your/project/
cp document-index.md /path/to/your/project/
```

### Step 2: Customize claude.md

Replace all placeholders (marked with `[BRACKETS]`):

- `[PROJECT_NAME]` - Your project name
- `[BRIEF_DESCRIPTION_OF_PROJECT]` - What your project does
- `[CORE_INNOVATION]` - What makes it unique
- `[PROJECT_PHASE]` - Current development phase
- `[NEXT_MILESTONE]` - Next goal or milestone
- `[CURRENT_BRANCH_NAME]` - Your current git branch
- `[CURRENT_PHASE_NAME]` - Name of current development phase
- `[TECH_STACK]` - Technologies, frameworks, languages used
- `[DIRECTORY_STRUCTURE]` - Your project's file organization
- `[PROJECT_SPECIFIC_CONVENTIONS]` - Naming conventions, terminology, style guides

### Step 3: Customize document-index.md

1. Update `[PROJECT_NAME]` with your project name
2. Update `[YYYY-MM-DD]` with today's date
3. Add entries for any existing documents in your project
4. Remove template sections you don't need
5. Add custom categories relevant to your project

### Step 4: Create Initial Documents

Start with the minimum viable documentation:

1. **README.md** - If you don't have one, create it
   - Project overview
   - Quick start guide
   - Link to claude.md and document-index.md

2. Add any other existing docs to document-index.md

### Step 5: Commit Everything Together

```bash
git add claude.md document-index.md README.md
git commit -m "[Docs] Initialize self-documenting system"
```

## Quick Start: AI Agent Instructions

When working with AI agents like Claude Code, you can bootstrap using simple instructions:

### Simple One-Liner
```
Bootstrap this project with the self-documenting system from
https://github.com/kbidne/SMDocs - copy claude.md and document-index.md
templates and customize them for this project.
```

### Detailed Instructions
```
Set up SMDocs for this project:
1. Fetch templates from https://github.com/kbidne/SMDocs
2. Copy claude.md and document-index.md to project root
3. Customize all [BRACKETED] placeholders
4. Update README to reference the documentation system
5. Commit everything together
```

### Direct File URLs
For faster access, reference the raw files:
```
Fetch and customize these templates:
- https://raw.githubusercontent.com/kbidne/SMDocs/main/claude.md
- https://raw.githubusercontent.com/kbidne/SMDocs/main/document-index.md
```

The AI will fetch the templates, customize them for your project, and set up the self-documenting system automatically.

## Core Principles

### 1. Documents Must Stay in Sync

When you modify one document, you MUST update related documents. This is enforced through:
- Mandatory maintenance steps in claude.md
- Timestamp tracking in document-index.md
- Atomic commits that update all related docs together

### 2. Bidirectional Cross-References

If Document A links to Document B, Document B should link back to A when relevant. This prevents:
- Orphaned documents
- Missing context
- Broken information flows

### 3. Central Registry is Source of Truth

`document-index.md` is the single source of truth for:
- What documents exist
- When they were last updated
- How they relate to each other
- Who should read them

### 4. AI-First Design

These templates are designed to work seamlessly with AI agents by:
- Providing explicit, unambiguous instructions
- Maintaining context across sessions
- Making project state easily discoverable
- Standardizing workflows and conventions

## Daily Usage

### When Creating a Document

1. Create the document
2. Update document-index.md (add entry, update count)
3. Add cross-references in related docs
4. Update claude.md if it changes workflows
5. Commit all changes together

### When Modifying a Document

1. Make your changes
2. Update document-index.md timestamp
3. Review related docs for consistency
4. Update claude.md if needed
5. Commit all changes together

### When Starting a New AI Session

As a user, provide the AI with:
- Current branch name
- Current phase/milestone
- Specific task or goal

The AI will:
- Read claude.md for workflow instructions
- Read document-index.md to see what exists
- Confirm understanding before proceeding

## Best Practices

### Documentation Quality

- Keep documents focused on a single topic
- Use consistent markdown formatting
- Include "Related Documentation" sections
- Update timestamps immediately when changing docs
- Write for both humans and AI

### Commit Strategy

- Commit related doc changes atomically
- Use descriptive commit messages with [Category] prefix
- Explain WHY changes were made, not just WHAT
- List all related documents in commit message

### Maintenance Schedule

- **Daily:** Update timestamps when modifying docs
- **Weekly:** Review document-index.md for accuracy
- **Monthly:** Check for stale docs (>30 days old)
- **Quarterly:** Audit cross-references and links

## Success Metrics

You'll know the system is working when:

✅ AI agents can resume work seamlessly in new sessions
✅ New contributors can onboard using just the documentation
✅ Documents never contradict each other
✅ All cross-references work and are bidirectional
✅ The documentation tells a coherent story
✅ Timestamps accurately reflect document freshness

## Advanced Customization

### Adding Custom Document Categories

In `document-index.md`, add sections like:
- 🧪 Testing & Quality
- 🚀 Deployment & Operations
- 🎨 Design & UX
- 📊 Analytics & Metrics

### Project-Specific Conventions

In `claude.md`, define:
- Terminology standards (what terms to use/avoid)
- Naming conventions (files, variables, branches)
- Code style guidelines
- Testing requirements
- Security practices

### Custom Workflows

Add sections to `claude.md` for:
- Release process
- Hotfix procedure
- Feature development workflow
- Code review standards

## Real-World Example

This system was extracted from the [domideas project](https://github.com/kbidne/domideas), which uses it to maintain 3,700+ lines of documentation across 7 major documents while working with AI agents across multiple sessions.

## Troubleshooting

### "Too much overhead for small projects"

Start minimal:
- Just README.md, claude.md, and document-index.md
- Add more docs only as needed
- The system scales with your project

### "Timestamps are tedious to update"

- It takes 10 seconds per document
- Prevents hours of debugging inconsistent docs
- Can be automated with git hooks if needed

### "My team won't follow the process"

- Lead by example
- Show the value (faster onboarding, better AI results)
- Make it part of PR review checklist
- Automate checks where possible

## Questions or Issues?

This bootstrap system is designed to be adapted to your needs. Feel free to:
- Modify templates to match your workflow
- Add/remove sections as needed
- Create custom categories and conventions
- Evolve the system as your project grows

The templates are a starting point, not a rigid framework. Make them yours!

---

**Remember: Documentation is code. Keep it consistent, tested, and up-to-date.**
