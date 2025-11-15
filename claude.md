# Claude Code Instructions for [PROJECT_NAME]

**Last Updated:** [YYYY-MM-DD]

---

## Project Overview

**[PROJECT_NAME]** is [BRIEF_DESCRIPTION_OF_PROJECT].

**Core Innovation:** [WHAT_MAKES_THIS_PROJECT_UNIQUE]

**Current Status:** [PROJECT_PHASE - e.g., Requirements & Planning, Development, Production]
**Next Phase:** [NEXT_MILESTONE]

---

## Documentation System

This project uses a **self-maintaining documentation system** to ensure coherence across multiple AI sessions and human contributors.

### Core Principle: Documents Must Stay in Sync

When you modify one document, you MUST update related documents to maintain consistency. This is critical for long-running projects with multiple contributors and AI sessions.

---

## 🚨 CRITICAL INSTRUCTIONS: Documentation Maintenance

### When You Create a New Document

**MANDATORY STEPS (Execute in this order):**

1. **Create the new document** with appropriate content
2. **Update document-index.md** to include the new document:
   - Add entry with filename, description, last updated date
   - Add to appropriate category
   - Update document count
3. **Update related documents** that should reference the new document:
   - Add cross-reference links where relevant
   - Update "Related Documentation" sections
   - Ensure bidirectional linking (if A links to B, B should link to A when relevant)
4. **Update this file (claude.md)** if the new document changes workflows or processes
5. **Commit all changes together** in a single atomic commit

### When You Modify an Existing Document

**MANDATORY STEPS:**

1. **Make your changes** to the document
2. **Update document-index.md**:
   - Update the "Last Updated" timestamp for that document
   - Update the description if the purpose changed
3. **Review related documents**:
   - Check if cross-references need updating
   - Update any documents that quote or reference the modified content
4. **Update this file (claude.md)** if the changes affect workflows or instructions
5. **Commit all changes together**

### When You Receive Instructions to Update claude.md

**MANDATORY STEPS:**

1. **Update claude.md** with the new instructions
2. **Update document-index.md**:
   - Update the "Last Updated" timestamp for claude.md
   - Add any new document types to the registry
3. **Review ALL documents** listed in document-index.md:
   - Check if the new instructions affect existing documents
   - Update documents that need to align with new instructions
   - Add cross-references where needed
4. **Verify consistency** across the entire documentation system
5. **Commit all changes together**

---

## Documentation Structure

### Primary Documents (Standard Set)

1. **README.md** - Project overview, quick start, high-level features
2. **document-index.md** - Central registry of all documents (THIS IS THE SOURCE OF TRUTH)
3. **claude.md** - This file - instructions for AI agents working on the project

### Common Additional Documents (Add as needed)

- **REQUIREMENTS.md** - Product requirements, features, specifications
- **ARCHITECTURE.md** or **PROJECT_STRUCTURE.md** - Technical architecture, file organization
- **BACKLOG.md** - Future feature ideas, prioritization framework
- **API_REFERENCE.md** - Detailed API documentation
- **CONTRIBUTING.md** - Guidelines for contributors
- **CHANGELOG.md** - Version history and release notes
- **DEPLOYMENT.md** - Deployment instructions
- **TESTING.md** - Testing strategy and test cases
- **SECURITY.md** - Security considerations

---

## Document Cross-Reference Rules

### Always Maintain Bidirectional Links

If Document A references Document B, consider if Document B should reference Document A.

**Example:**
- `REQUIREMENTS.md` links to `ARCHITECTURE.md` ✓
- `ARCHITECTURE.md` should link back to `REQUIREMENTS.md` ✓

### Use Consistent Link Format

```markdown
See [DOCUMENT_NAME.md](./DOCUMENT_NAME.md) for details.

For specific sections:
See [Section Name in DOCUMENT_NAME.md](./DOCUMENT_NAME.md#section-anchor)
```

### "Related Documentation" Sections

Every major document should have a "Related Documentation" section listing:
- Parent documents (higher level)
- Child documents (more detailed)
- Sibling documents (same level, related topics)

---

## Git Workflow

### Branching Strategy

**Current Branch:** [CURRENT_BRANCH_NAME]

**Branch Naming Convention:**
- `claude/[task-description]-[session-id]` - For AI-generated work
- `feature/[feature-name]` - For human-developed features
- `docs/[doc-update]` - For documentation updates
- `bugfix/[issue-description]` - For bug fixes
- `refactor/[what-is-refactored]` - For refactoring

### Commit Message Guidelines

**Format:**
```
[Category] Brief description

Detailed explanation:
- What changed
- Why it changed
- Impact on other documents/systems

Related documents updated:
- document-index.md
- [OTHER_DOCS]
```

**Categories:**
- `[Docs]` - Documentation updates
- `[Feature]` - New feature implementation
- `[Fix]` - Bug fixes
- `[Refactor]` - Code refactoring
- `[Test]` - Test additions/updates
- `[Meta]` - Project structure, build config, etc.

### Atomic Commits for Documentation

When updating documentation, **always commit related changes together**:

```bash
# Good: All related doc updates in one commit
git add document-index.md REQUIREMENTS.md claude.md
git commit -m "[Docs] Update requirements and sync documentation"

# Bad: Separate commits that break consistency temporarily
git add REQUIREMENTS.md
git commit -m "[Docs] Update requirements"
git add document-index.md
git commit -m "[Docs] Update index"  # <- Index is out of sync between commits!
```

---

## Development Workflow

### Current Phase: [CURRENT_PHASE_NAME]

[DESCRIPTION_OF_CURRENT_DEVELOPMENT_PHASE]

**Tech Stack:**
- [FRAMEWORK/LANGUAGE]
- [BUILD_TOOL]
- [TESTING_FRAMEWORK]
- [OTHER_TOOLS]

### When Starting a New Phase

1. **Review all documentation** to understand current state
2. **Check document-index.md** for the latest version of each document
3. **Read this file (claude.md)** for any updated instructions
4. **Create a new branch** following naming convention
5. **Update relevant documents** to mark phase as "in progress"
6. **Update document-index.md** when you create new files
7. **Commit regularly** with descriptive messages

---

## Code Organization Instructions

### When Creating New Code Files

1. **Follow [ARCHITECTURE_DOCUMENT]** for file organization
2. **Update [ARCHITECTURE_DOCUMENT]** if you deviate from the plan (with justification)
3. **Add documentation comments** for public APIs
4. **Update document-index.md** to include new code documentation files

### Directory Structure

```
[PROJECT_ROOT]/
├── [MAIN_SOURCE_DIR]/
│   ├── [SUBDIRECTORIES]
│   └── [FILES]
├── [TESTS_DIR]/
├── [DOCS_DIR]/
└── [CONFIG_FILES]
```

---

## AI-Specific Instructions

### For Claude Code (or similar AI agents)

When you're asked to work on this project:

1. **Start by reading these files in order:**
   - `claude.md` (this file) - Understand the workflow
   - `document-index.md` - See what documents exist
   - Relevant documents for your specific task

2. **Before making changes:**
   - Announce which documents you plan to modify
   - Explain how they relate to each other
   - Confirm the user agrees with the approach

3. **After making changes:**
   - List all documents you modified
   - Confirm they're all in sync
   - Update document-index.md timestamps
   - Commit atomically

4. **Communication style:**
   - Be direct and concise (this is a CLI tool)
   - Avoid excessive emojis unless user requests them
   - Focus on technical accuracy over validation
   - Propose solutions, don't just describe problems

### Context Sharing Between Sessions

When starting a new session:

1. **User should provide context** by sharing:
   - Current branch name
   - Current phase or milestone
   - Specific task or goal

2. **You should respond** by:
   - Reading claude.md (this file)
   - Reading document-index.md
   - Confirming your understanding of the current state
   - Proposing a plan before executing

### Handling Conflicts or Ambiguity

If you notice:
- **Conflicting information** between documents → Point it out, propose a fix
- **Missing cross-references** → Add them
- **Outdated timestamps** → Update them
- **Unclear requirements** → Ask for clarification before proceeding

---

## Quality Standards

### Documentation Quality

Every document should:
- Have a clear purpose stated at the top
- Use consistent markdown formatting
- Include a "Last Updated" timestamp (in document-index.md)
- Cross-reference related documents
- Be readable by both humans and AI agents

### Code Quality

Every code file should:
- Follow the project's style guide
- Include documentation comments for public APIs
- Have corresponding tests (unit or integration)
- Be referenced in architecture/structure documentation

### Commit Quality

Every commit should:
- Have a descriptive message explaining WHY, not just WHAT
- Include all related changes (atomic commits for related files)
- Pass linting and tests (once set up)
- Update documentation if behavior changes

---

## Testing Strategy

### Documentation Testing (Manual)

Before committing documentation changes:

1. **Link validity:**
   - Check for broken internal links
   - Verify linked files exist

2. **Consistency check:**
   - All documents mentioned in document-index.md exist?
   - All timestamps in document-index.md are accurate?
   - All cross-references are bidirectional?

3. **Readability:**
   - Can a new contributor understand the project from README.md?
   - Are technical terms explained or linked?
   - Is the information architecture logical?

### Code Testing

[PROJECT_SPECIFIC_TESTING_STRATEGY]

---

## Common Tasks Quick Reference

### Adding a New Feature to Backlog

1. Open `BACKLOG.md` (or create if doesn't exist)
2. Add feature to appropriate category/priority
3. Update feature count if tracked
4. Update `document-index.md` timestamp for BACKLOG.md
5. Commit: `[Docs] Add [feature name] to backlog`

### Creating a New Planning Document

1. Create the document with proper structure
2. Add "Related Documentation" section
3. Update `document-index.md` with new entry
4. Update related documents to link to new document
5. Update this file (`claude.md`) if it affects workflows
6. Commit all changes together

### Starting New Development Phase

1. Read relevant documentation thoroughly
2. Create branch following naming convention
3. Set up project structure as documented
4. Update `document-index.md` with any new docs
5. Commit: `[Feature] Initialize [phase/component name]`

---

## Troubleshooting

### "Documents are out of sync"

**Solution:**
1. Check git diff to see what changed
2. Read document-index.md to find related documents
3. Update all related documents to be consistent
4. Update timestamps in document-index.md
5. Commit all changes atomically

### "Can't find information about X"

**Solution:**
1. Check document-index.md for the most likely document
2. Use grep to search across all docs: `grep -r "search term" *.md`
3. If not found, ask user or check BACKLOG.md (might be a future feature)

### "Conflicting requirements between documents"

**Solution:**
1. Point out the conflict to the user
2. Ask for clarification on which is correct
3. Update all documents to be consistent
4. Update document-index.md timestamps
5. Commit with explanation of the conflict resolution

---

## Project-Specific Conventions

### Naming Conventions

**Files:**
- Documents: `UPPERCASE_NAME.md` (e.g., REQUIREMENTS.md) OR `lowercase-name.md`
- Code: [YOUR_CONVENTION - e.g., kebab-case.ts, camelCase.js, PascalCase.tsx]
- Tests: [YOUR_CONVENTION - e.g., *.test.ts, *.spec.ts, *_test.py]

**Variables/Functions:**
- [YOUR_LANGUAGE]: [YOUR_CONVENTION - e.g., camelCase, snake_case]
- Constants: [YOUR_CONVENTION - e.g., UPPER_SNAKE_CASE]
- Types/Classes: [YOUR_CONVENTION - e.g., PascalCase]

### Terminology

Use consistent terminology across all documents:

- **[TERM_1]** - [DEFINITION] (not "[AVOID_TERM]")
- **[TERM_2]** - [DEFINITION] (not "[AVOID_TERM]")
- **[TERM_3]** - [DEFINITION] (not "[AVOID_TERM]")

[Add project-specific terms that should be used consistently]

---

## Success Criteria

You're doing well if:

✅ All documents listed in document-index.md actually exist
✅ All timestamps in document-index.md are accurate
✅ Cross-references are bidirectional and working
✅ No conflicting information between documents
✅ New contributors can onboard using just the documentation
✅ AI agents can resume work from a new session seamlessly
✅ Commits are atomic and include all related doc updates
✅ The documentation tells a coherent story about the project

You need to improve if:

❌ Documents contradict each other
❌ Links are broken or outdated
❌ document-index.md is missing documents
❌ Timestamps are wrong or missing
❌ Changes aren't committed atomically
❌ New documents aren't cross-referenced
❌ Code doesn't match architecture/structure documentation

---

## Version History of This File

**[YYYY-MM-DD]** - Initial creation
- Established documentation maintenance workflow
- Defined mandatory steps for document updates
- Created cross-reference rules
- Added project-specific conventions

**[Future updates will be listed here]**

---

## Questions or Improvements?

If you (as an AI agent) notice:
- Missing instructions that would be helpful
- Ambiguous guidelines
- Conflicts in this file
- Better ways to structure the documentation

→ Point it out to the user and suggest improvements
→ This file should evolve as the project grows

---

**Remember: Documentation is code. Keep it consistent, tested, and up-to-date.**
