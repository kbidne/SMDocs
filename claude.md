# Claude Code Instructions for [PROJECT_NAME]

**Last Updated:** [YYYY-MM-DD]

---

## 🎯 Mission Control

### Project Overview

**[PROJECT_NAME]** is [BRIEF_DESCRIPTION_OF_PROJECT].

**Core Innovation:** [WHAT_MAKES_THIS_PROJECT_UNIQUE]

**Current Status:** [PROJECT_PHASE]
**Next Milestone:** [NEXT_GOAL]

### How to Use This Document

This file is **Mission Control** for all AI agents working on this project. It contains:
- The **Team Structure** (where different types of knowledge live)
- **Mandatory Workflows** for keeping documentation in sync
- **Conversational Intent Mapping** (how to route tasks to the right documentation)
- **Governance Rules** and **Business Logic** that AI agents must follow
- **Self-Evolution Protocol** (how this system improves itself)

---

## 🏛️ The Knowledge Architecture

This project organizes documentation into **knowledge domains** - think of them as specialized teams, each with their own expertise and documentation.

### The Teams (Documentation Domains)

#### 📚 **The Library** - Documentation Central
- **What:** Meta-documentation, knowledge management, this file
- **Documents:**
  - `claude.md` (this file) - AI agent instructions
  - `document-index.md` - Central registry of all documents
  - `README.md` - Project overview and quick start
- **When to update:** Adding/modifying any documentation, changing workflows
- **Responsible for:** Maintaining documentation consistency, cross-references, timestamps

#### 🔬 **The AI Lab** - AI Agents & Automation
- **What:** AI agent configurations, prompts, conversational intents, automation rules
- **Documents:**
  - `AI_AGENTS.md` - Registry of AI agents, their roles, and capabilities
  - `INTENTS.md` - Conversational intent mapping and routing rules
  - `PROMPTS.md` - Reusable prompt templates and patterns
  - `AUTOMATION.md` - Automated workflows and triggers
- **When to update:** Adding AI capabilities, changing how AI agents work, new automation
- **Responsible for:** AI governance, prompt engineering, agent coordination

#### 🏗️ **The Workshop** - Engineering & Architecture
- **What:** Code architecture, technical decisions, development processes
- **Documents:**
  - `ARCHITECTURE.md` - System architecture and technical design
  - `TECH_STACK.md` - Technologies, frameworks, and tools
  - `API_REFERENCE.md` - API documentation
  - `TESTING.md` - Testing strategy and QA processes
- **When to update:** Architectural changes, new tech choices, API updates
- **Responsible for:** Technical standards, code quality, architecture decisions

#### 🎨 **The Studio** - Product & Design
- **What:** Product requirements, UX/UI design, user workflows
- **Documents:**
  - `REQUIREMENTS.md` - Product requirements and specifications
  - `DESIGN_SYSTEM.md` - Design patterns, UI components, brand guidelines
  - `USER_WORKFLOWS.md` - User journeys and interaction patterns
  - `BACKLOG.md` - Feature ideas and product roadmap
- **When to update:** Product changes, design updates, new requirements
- **Responsible for:** Product vision, user experience, feature prioritization

#### 🛡️ **The Vault** - Security & Governance
- **What:** Security policies, compliance rules, data governance, business rules
- **Documents:**
  - `SECURITY.md` - Security policies and vulnerability reporting
  - `COMPLIANCE.md` - Regulatory compliance requirements
  - `BUSINESS_RULES.md` - Critical business logic and policies
  - `DATA_GOVERNANCE.md` - Data handling, privacy, retention policies
- **When to update:** Security changes, compliance updates, new business rules
- **Responsible for:** Risk management, policy enforcement, compliance

#### ⚙️ **The Command Center** - Operations
- **What:** Deployment, monitoring, incident response, infrastructure
- **Documents:**
  - `DEPLOYMENT.md` - Deployment procedures and infrastructure
  - `RUNBOOK.md` - Operational procedures and troubleshooting
  - `MONITORING.md` - Observability, metrics, alerts
  - `INCIDENTS.md` - Incident response and post-mortems
- **When to update:** Ops changes, new deployment processes, infrastructure updates
- **Responsible for:** System reliability, performance, operational excellence

#### 🤝 **The Council** - Stakeholders & Decisions
- **What:** Business context, stakeholder decisions, organizational knowledge
- **Documents:**
  - `STAKEHOLDERS.md` - Key stakeholders, roles, communication channels
  - `DECISIONS.md` - Architecture Decision Records (ADRs) and major choices
  - `GLOSSARY.md` - Business terminology and domain language
  - `CONTEXT.md` - Business background and organizational knowledge
- **When to update:** Stakeholder changes, major decisions, new business context
- **Responsible for:** Business alignment, decision tracking, institutional knowledge

---

## 🔄 Core Principle: The Self-Documenting Loop

This system is designed to **evolve and improve itself**. Every interaction makes the documentation better.

### The Loop

```
1. AI Agent receives task
   ↓
2. Reads claude.md (Mission Control)
   ↓
3. Routes to appropriate Team (domain)
   ↓
4. Reads team-specific documentation
   ↓
5. Executes task following rules
   ↓
6. Updates documentation (keeps knowledge fresh)
   ↓
7. Updates document-index.md (maintains registry)
   ↓
8. Commits changes atomically
   ↓
9. System is smarter for next interaction
```

### Why This Works

- **Conversational Intent Mapping:** When user says "update the AI Lab", agent knows to update AI_AGENTS.md, INTENTS.md, etc.
- **Domain Expertise:** Each team owns specific knowledge, preventing confusion
- **Mandatory Synchronization:** Documents stay in sync through enforced workflows
- **Continuous Improvement:** Every task adds to the knowledge base
- **Multi-Session Continuity:** New AI sessions pick up exactly where previous ones left off

---

## 🚨 CRITICAL INSTRUCTIONS: Documentation Maintenance

### Mandatory Workflow: Creating a New Document

**Execute these steps in order (no skipping!):**

1. **Identify the Team** - Which domain does this document belong to?
   - Use the Teams list above to categorize
   - If unclear, it probably belongs in The Library

2. **Create the document** with this structure:
   ```markdown
   # [Document Title]

   **Team:** [Team Name]
   **Last Updated:** [YYYY-MM-DD]
   **Maintained By:** [Primary maintainer or "AI Agents"]

   ---

   ## Purpose
   [What this document covers and why it exists]

   ## Related Documentation
   - [Related docs with brief descriptions]

   ---

   [Document content]
   ```

3. **Update document-index.md:**
   - Add entry with filename, description, team, last updated date
   - Update document count
   - Add to appropriate team category

4. **Update the Team's parent document** (if one exists):
   - Reference the new document
   - Explain its relationship to other team docs

5. **Update this file (claude.md)** if the document:
   - Changes workflows or processes
   - Adds new AI agent capabilities
   - Modifies governance rules

6. **Create bidirectional links:**
   - Add references in related documents
   - Ensure links go both ways

7. **Commit all changes atomically:**
   ```bash
   git add [new-doc].md document-index.md claude.md [related-docs].md
   git commit -m "[Team] Add [document name] - [brief description]"
   ```

### Mandatory Workflow: Modifying an Existing Document

**Execute these steps in order:**

1. **Make your changes** to the document
   - Update the "Last Updated" timestamp in the document header
   - Note what changed in a changelog section if significant

2. **Update document-index.md:**
   - Update the timestamp for this document
   - Update description if the purpose changed

3. **Review related documents:**
   - Check if cross-references need updating
   - Update any docs that quote or reference the modified content
   - Verify bidirectional links still make sense

4. **Update team coordination:**
   - If changes affect other teams, update their documents
   - Example: Changing API (Workshop) → update BUSINESS_RULES.md (Vault)

5. **Update claude.md** if changes affect:
   - How AI agents should work
   - Workflow processes
   - Team responsibilities

6. **Commit all changes atomically:**
   ```bash
   git add [modified-docs].md document-index.md [related-docs].md
   git commit -m "[Team] Update [document name] - [what and why]"
   ```

### Mandatory Workflow: Routing Conversational Intents

When you (AI agent) receive a task, **route it properly**:

| User Says... | Maps To Team | Update These Docs |
|-------------|--------------|-------------------|
| "Update the AI Lab" | The AI Lab | AI_AGENTS.md, INTENTS.md, PROMPTS.md |
| "Tell the Workshop" | The Workshop | ARCHITECTURE.md, TECH_STACK.md, API_REFERENCE.md |
| "Notify the Studio" | The Studio | REQUIREMENTS.md, DESIGN_SYSTEM.md, BACKLOG.md |
| "Check with the Vault" | The Vault | SECURITY.md, BUSINESS_RULES.md, COMPLIANCE.md |
| "Update the Command Center" | The Command Center | DEPLOYMENT.md, RUNBOOK.md, MONITORING.md |
| "Inform the Council" | The Council | STAKEHOLDERS.md, DECISIONS.md, CONTEXT.md |
| "Add to the Library" | The Library | document-index.md, README.md, claude.md |

**Examples:**

```
User: "Add a new authentication rule and update the AI Lab"
→ Update SECURITY.md (Vault) + AI_AGENTS.md (AI Lab)

User: "We decided to use PostgreSQL - tell the Workshop and Council"
→ Update TECH_STACK.md (Workshop) + DECISIONS.md (Council)

User: "New design pattern, update the Studio"
→ Update DESIGN_SYSTEM.md (Studio)
```

---

## 🎭 AI Agent Protocols

### For Claude Code and Similar AI Agents

#### Starting a New Session

1. **Read in this order:**
   - `claude.md` (this file) - Understand mission control
   - `document-index.md` - See what documents exist
   - Relevant team documents for your task

2. **Confirm understanding:**
   - State which team(s) you'll be working with
   - List documents you plan to read/modify
   - Propose your approach

3. **Execute with discipline:**
   - Follow mandatory workflows
   - Update documentation as you work
   - Maintain cross-references

#### Communication Style

- **Be direct and precise** - This is a professional environment
- **Avoid excessive emojis** - Unless user requests them
- **Focus on accuracy** - Over validation or cheerleading
- **Propose solutions** - Don't just describe problems
- **Think in teams** - Use the team language ("The Workshop needs this update")

#### Handling Ambiguity

| Situation | Action |
|-----------|--------|
| **Conflicting info between teams** | Point out conflict, propose resolution, ask for user decision |
| **Missing documentation** | Create it following mandatory workflow, assign to appropriate team |
| **Unclear intent** | Ask user to clarify using team language ("Is this for the Vault or the Workshop?") |
| **Outdated timestamps** | Update them as you go |
| **Broken cross-references** | Fix them immediately |

### Context Sharing Between Sessions

**User should provide:**
- Current branch name
- Current milestone/phase
- Specific task or goal
- Which team(s) are involved

**You (AI agent) should:**
- Read claude.md and document-index.md
- Identify which teams are involved
- Read team-specific documents
- Confirm understanding before proceeding
- Propose plan using team language

---

## 📋 Document Cross-Reference Rules

### Bidirectional Linking (Mandatory)

If Document A references Document B, Document B **MUST** reference Document A (when relevant).

**Example:**
```markdown
# In ARCHITECTURE.md (Workshop)
See [BUSINESS_RULES.md](./BUSINESS_RULES.md) for governance policies.

# In BUSINESS_RULES.md (Vault)
See [ARCHITECTURE.md](./ARCHITECTURE.md) for technical implementation.
```

### Cross-Team References

When teams interact, documents MUST cross-reference:

```markdown
# In REQUIREMENTS.md (Studio)
## Related Documentation
- **The Workshop:** See ARCHITECTURE.md for technical implementation
- **The Vault:** See SECURITY.md for security requirements
- **The Council:** See DECISIONS.md for stakeholder approvals
```

### Link Format (Standard)

```markdown
# Simple reference
See [DOCUMENT_NAME.md](./DOCUMENT_NAME.md) for details.

# Section reference
See [Section Name](./DOCUMENT_NAME.md#section-anchor) for specifics.

# Cross-team reference
See [DOCUMENT_NAME.md](./DOCUMENT_NAME.md) in The [Team Name] for [what info].
```

---

## 🔐 Governance & Business Rules

### Critical Rules AI Agents Must Follow

These rules are **non-negotiable**. AI agents MUST follow them:

1. **Never skip documentation updates** - If you change code/config, update docs
2. **Always commit atomically** - Related changes go together
3. **Respect team boundaries** - Don't put Studio content in Workshop docs
4. **Verify timestamps** - Always update "Last Updated" dates
5. **Maintain bidirectional links** - Links must go both ways
6. **Follow security policies** - Check The Vault before handling sensitive data
7. **Respect business rules** - The Vault and Council override technical preferences

### Policy Hierarchy

When conflicts arise, this is the decision hierarchy:

```
1. Security & Compliance (The Vault) - HIGHEST PRIORITY
   ↓
2. Business Rules & Stakeholder Decisions (The Council)
   ↓
3. Product Requirements (The Studio)
   ↓
4. Technical Architecture (The Workshop)
   ↓
5. AI Agent Preferences (The AI Lab) - LOWEST PRIORITY
```

**Example:** If The Vault says "no customer data in logs" but The Workshop's logging architecture does it, **The Vault wins**. Update The Workshop.

---

## 🛠️ Git Workflow

### Branching Strategy

**Current Branch:** [CURRENT_BRANCH_NAME]

**Naming Conventions:**
- `claude/[task]-[session-id]` - AI agent work
- `feature/[name]` - New features
- `docs/[team]/[update]` - Documentation updates (team-specific)
- `fix/[issue]` - Bug fixes
- `security/[update]` - Security patches

### Commit Message Format

```
[Team] Brief description

Team(s) involved: [Team names]

Changes:
- What changed in each document
- Why it changed
- Impact on other teams

Related docs updated:
- document-index.md
- [other files]
```

**Commit Categories by Team:**
- `[Library]` - Meta-documentation updates
- `[AI Lab]` - AI agent, prompt, or automation changes
- `[Workshop]` - Code, architecture, or technical updates
- `[Studio]` - Product, design, or requirements changes
- `[Vault]` - Security, compliance, or governance updates
- `[Command Center]` - Operations, deployment, or infrastructure changes
- `[Council]` - Stakeholder, decision, or business context updates

### Atomic Commits (Mandatory)

**Always commit related changes together:**

```bash
# GOOD - All related team updates in one commit
git add document-index.md ARCHITECTURE.md SECURITY.md claude.md
git commit -m "[Workshop + Vault] Add encryption layer

Team(s) involved: The Workshop, The Vault

Changes:
- Added encryption architecture to ARCHITECTURE.md
- Updated security policies in SECURITY.md
- Added cross-references between teams
- Updated document-index.md timestamps

Related docs updated:
- document-index.md
- ARCHITECTURE.md
- SECURITY.md
- claude.md (team coordination notes)"

# BAD - Separate commits break consistency
git add ARCHITECTURE.md
git commit -m "Add encryption"
# ← document-index.md is now out of sync!
```

---

## 📊 Quality Standards

### Documentation Quality (All Teams)

Every document MUST have:
- **Team assignment** - Clear team ownership
- **Last Updated timestamp** - In the document and document-index.md
- **Purpose statement** - Why this document exists
- **Related Documentation** - Cross-references to other teams
- **Readable by AI and humans** - Clear, structured, scannable

### Team-Specific Standards

#### The Library
- Meta-documentation is always current
- document-index.md is the source of truth
- Cross-reference map is accurate

#### The AI Lab
- AI agent roles are clearly defined
- Conversational intents are unambiguous
- Prompts are tested and versioned

#### The Workshop
- Architecture decisions are documented
- Code references match documentation
- APIs are fully documented

#### The Studio
- Requirements are testable
- User workflows are complete
- Design patterns are consistent

#### The Vault
- Security policies are enforced
- Business rules are non-negotiable
- Compliance requirements are tracked

#### The Command Center
- Runbooks are executable
- Deployment procedures are tested
- Monitoring is comprehensive

#### The Council
- Stakeholder decisions are recorded
- Context is maintained
- Terminology is consistent

---

## 🧪 Testing & Validation

### Documentation Testing (Pre-Commit)

Before committing, verify:

1. **Link validity:**
   ```bash
   # Check all internal links work
   grep -r "\[.*\](\.\/.*\.md)" *.md
   ```

2. **Timestamp accuracy:**
   - Updated in both document header AND document-index.md
   - Format is YYYY-MM-DD

3. **Team assignment:**
   - Every doc is assigned to a team
   - Team categorization makes sense

4. **Cross-reference completeness:**
   - Bidirectional links are present
   - Cross-team references are accurate

5. **Business rule compliance:**
   - Changes don't violate Vault policies
   - Council decisions are respected

---

## 🎯 Common Task Patterns

### Adding a New AI Agent

1. **Update The AI Lab:**
   - Add to `AI_AGENTS.md` with role, capabilities, constraints
   - Define conversational intents in `INTENTS.md`
   - Create prompt templates in `PROMPTS.md`

2. **Update cross-team docs:**
   - Add to `document-index.md`
   - Reference in `claude.md` if affects workflows

3. **Commit:**
   ```bash
   git commit -m "[AI Lab] Add [agent name] agent"
   ```

### Adding a Security Rule

1. **Update The Vault:**
   - Add rule to `SECURITY.md` or `BUSINESS_RULES.md`
   - Mark as CRITICAL if non-negotiable

2. **Notify affected teams:**
   - Update Workshop docs if affects code
   - Update AI Lab if affects agent behavior
   - Update Command Center if affects deployment

3. **Commit atomically:**
   ```bash
   git commit -m "[Vault + Workshop] Add [rule name] security requirement"
   ```

### Recording a Major Decision

1. **Update The Council:**
   - Add ADR (Architecture Decision Record) to `DECISIONS.md`
   - Update `CONTEXT.md` with business rationale

2. **Update affected teams:**
   - Workshop: Technical implications
   - Studio: Product impact
   - Vault: Governance considerations

3. **Commit:**
   ```bash
   git commit -m "[Council] Record decision: [decision name]"
   ```

---

## 🔍 Troubleshooting

### "Which team should I update?"

Use this decision tree:

```
Is it about AI agents/prompts/automation?
  → The AI Lab

Is it about code/architecture/technical design?
  → The Workshop

Is it about product/design/user experience?
  → The Studio

Is it about security/compliance/business rules?
  → The Vault

Is it about deployment/operations/infrastructure?
  → The Command Center

Is it about stakeholders/decisions/business context?
  → The Council

Is it about documentation itself?
  → The Library
```

### "Documents are conflicting"

**Resolution process:**
1. Identify which teams are involved
2. Check policy hierarchy (Vault > Council > Studio > Workshop > AI Lab)
3. Higher priority team wins
4. Update lower priority team's docs
5. Add cross-reference explaining the relationship
6. Commit atomically

### "Can't find the right document"

1. Check `document-index.md` first
2. Use team categories to narrow search
3. Grep across team docs:
   ```bash
   grep -r "search term" *.md
   ```
4. If truly missing, create it following mandatory workflow

---

## 📖 Project-Specific Conventions

### File Naming

**By Team:**
- Library: `README.md`, `claude.md`, `document-index.md`
- AI Lab: `AI_AGENTS.md`, `INTENTS.md`, `PROMPTS.md`, `AUTOMATION.md`
- Workshop: `ARCHITECTURE.md`, `TECH_STACK.md`, `API_REFERENCE.md`, `TESTING.md`
- Studio: `REQUIREMENTS.md`, `DESIGN_SYSTEM.md`, `USER_WORKFLOWS.md`, `BACKLOG.md`
- Vault: `SECURITY.md`, `COMPLIANCE.md`, `BUSINESS_RULES.md`, `DATA_GOVERNANCE.md`
- Command Center: `DEPLOYMENT.md`, `RUNBOOK.md`, `MONITORING.md`, `INCIDENTS.md`
- Council: `STAKEHOLDERS.md`, `DECISIONS.md`, `GLOSSARY.md`, `CONTEXT.md`

**Placeholders:**
- `[BRACKETS]` for user-customizable content
- `[TEAM_NAME]` for team-specific information
- Include inline comments for guidance

### Terminology (Standard Across All Teams)

- **Team** - A documentation domain with specific responsibilities
- **The Library** - Meta-documentation and knowledge management
- **The AI Lab** - AI agents, prompts, automation
- **The Workshop** - Engineering and architecture
- **The Studio** - Product and design
- **The Vault** - Security, compliance, governance
- **The Command Center** - Operations and infrastructure
- **The Council** - Stakeholders and decisions
- **Mandatory Workflow** - Required steps that cannot be skipped
- **Atomic Commit** - All related changes committed together
- **Bidirectional Link** - Cross-reference that goes both ways
- **Policy Hierarchy** - Priority order when teams conflict
- **Conversational Intent** - Mapping user requests to teams/actions
- **Self-Documenting Loop** - System that improves itself

---

## ✅ Success Criteria

### System-Level Success

You're doing well if:

✅ All documents have team assignments
✅ document-index.md is comprehensive and current
✅ Cross-references are bidirectional
✅ Timestamps are accurate
✅ AI agents can route requests correctly
✅ Teams don't have overlapping responsibilities
✅ Business rules are clear and enforced
✅ New team members (human or AI) can onboard quickly
✅ Documentation evolves with every interaction

### Team-Level Success

Each team is successful when:
- **The Library:** All meta-docs are current, index is accurate
- **The AI Lab:** Agents work correctly, intents route properly
- **The Workshop:** Code matches documentation, architecture is clear
- **The Studio:** Requirements are complete, designs are documented
- **The Vault:** Policies are enforced, rules are clear
- **The Command Center:** Systems run smoothly, procedures work
- **The Council:** Decisions are tracked, stakeholders are aligned

---

## 🔄 Self-Evolution Protocol

This documentation system improves itself. Here's how:

### Continuous Improvement

1. **Every task teaches the system:**
   - New patterns → Add to relevant team docs
   - Edge cases → Update workflows
   - Confusion → Clarify terminology

2. **AI agents suggest improvements:**
   - "This workflow could be clearer..."
   - "The AI Lab needs a document for..."
   - "Cross-team coordination could improve if..."

3. **Regular reviews:**
   - Monthly: Review document timestamps, update stale docs
   - Quarterly: Review team boundaries, adjust if needed
   - Yearly: Major restructuring if project has evolved

### Evolution Guidelines

When evolving this system:
1. Propose changes before implementing
2. Update claude.md first (the blueprint)
3. Update affected team documents
4. Update document-index.md
5. Announce changes to all teams
6. Commit atomically with clear changelog

---

## 📚 Version History

**[YYYY-MM-DD]** - Initial creation
- Established team-based architecture
- Created mandatory workflows
- Defined conversational intent mapping
- Set up self-evolution protocol

**[Future updates will be listed here]**

---

## 🎓 For New AI Agents

If you're a new AI agent joining this project:

1. **Read this entire file** - It's your operating manual
2. **Study document-index.md** - Know what docs exist
3. **Learn the teams** - Understand each team's domain
4. **Practice routing** - Map user requests to teams
5. **Follow workflows** - They exist for good reasons
6. **Ask questions** - Point out ambiguities
7. **Suggest improvements** - Help this system evolve

**Remember:** You're not just executing tasks - you're making this project smarter.

---

**Welcome to [PROJECT_NAME]. Let's build something remarkable together.**
