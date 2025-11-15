# [PROJECT_NAME] Documentation Index

**Last Updated:** [YYYY-MM-DD]
**Total Documents:** [NUMBER]

This is the **central registry** of all documentation for [PROJECT_NAME]. All documents are organized by **Teams** (knowledge domains) with descriptions, timestamps, and cross-references.

---

## 🎯 Quick Start

1. **New to the project?** → Read README.md, then claude.md (Mission Control)
2. **Looking for specific info?** → Use the Teams below to find the right domain
3. **Created a document?** → Add it to the appropriate team category immediately
4. **Modified a document?** → Update its timestamp in both the document AND this index

---

## 🏛️ Documentation by Team

### 📚 **The Library** - Documentation Central ([NUMBER] docs)

Meta-documentation, knowledge management, and system documentation.

#### README.md
- **Team:** The Library
- **Purpose:** Project overview, quick start guide, entry point for all users
- **Audience:** Everyone - new contributors, users, stakeholders
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - What is [PROJECT_NAME]?
  - Quick start and installation
  - Links to team-specific documentation
  - How to contribute
- **Related Teams:**
  - All teams (serves as entry point)

---

#### claude.md
- **Team:** The Library
- **Purpose:** Mission Control for all AI agents - workflows, team structure, governance
- **Audience:** AI agents (Claude Code, etc.), human maintainers
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - **Team Structure** (7 teams with clear responsibilities)
  - **Mandatory Workflows** (creating/modifying documents)
  - **Conversational Intent Mapping** (routing user requests to teams)
  - **Governance Rules** and **Policy Hierarchy**
  - **Self-Evolution Protocol** (how system improves itself)
  - AI Agent Protocols and best practices
- **Related Teams:**
  - All teams (coordinates all documentation)

---

#### document-index.md
- **Team:** The Library
- **Purpose:** Central registry of all documents (THIS FILE)
- **Audience:** Everyone - single source of truth for what docs exist
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Complete document listing organized by teams
  - Team-based categorization
  - Timestamp tracking for freshness
  - Cross-reference map by team
  - Document status tracking
  - Quick navigation
- **Related Teams:**
  - All teams (tracks all documentation)

---

### 🔬 **The AI Lab** - AI Agents & Automation ([NUMBER] docs)

AI agent configurations, prompts, conversational intents, and automation rules.

#### AI_AGENTS.md
- **Team:** The AI Lab
- **Purpose:** Registry of all AI agents, their roles, capabilities, and constraints
- **Audience:** AI agents, developers, system administrators
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Agent registry (name, role, capabilities)
  - Agent coordination rules
  - Constraints and limitations
  - Inter-agent communication protocols
- **Related Teams:**
  - The Library: References claude.md for workflows
  - The Vault: Adheres to security policies

---

#### INTENTS.md
- **Team:** The AI Lab
- **Purpose:** Conversational intent mapping - routing user requests to correct teams/actions
- **Audience:** AI agents, prompt engineers
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Intent classification rules
  - Routing table (intent → team → documents)
  - Ambiguity resolution strategies
  - Intent examples and edge cases
- **Related Teams:**
  - The Library: Implements routing defined in claude.md
  - All teams: Maps intents to team documentation

---

#### PROMPTS.md
- **Team:** The AI Lab
- **Purpose:** Reusable prompt templates, patterns, and best practices
- **Audience:** Prompt engineers, AI agents, developers
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Prompt template library
  - Versioning and testing guidelines
  - Team-specific prompt patterns
  - Prompt optimization techniques
- **Related Teams:**
  - The Library: Follows documentation standards
  - The Vault: Respects security and privacy policies

---

#### AUTOMATION.md
- **Team:** The AI Lab
- **Purpose:** Automated workflows, triggers, and orchestration rules
- **Audience:** DevOps, AI agents, automation engineers
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Automation workflows and triggers
  - CI/CD integration for AI agents
  - Self-healing documentation processes
  - Monitoring and alerting for automation
- **Related Teams:**
  - The Command Center: Deployment automation
  - The Vault: Automation security policies

---

### 🏗️ **The Workshop** - Engineering & Architecture ([NUMBER] docs)

Code architecture, technical decisions, development processes, and testing.

#### ARCHITECTURE.md
- **Team:** The Workshop
- **Purpose:** System architecture, technical design, and architectural decisions
- **Audience:** Engineers, architects, technical leads
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - System architecture diagrams
  - Component relationships
  - Data flow and state management
  - Scalability and performance considerations
- **Related Teams:**
  - The Studio: Implements product requirements
  - The Vault: Follows security architecture guidelines
  - The Council: Records ADRs

---

#### TECH_STACK.md
- **Team:** The Workshop
- **Purpose:** Technologies, frameworks, libraries, and tools used in the project
- **Audience:** Engineers, new team members, technical stakeholders
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Languages and frameworks
  - Libraries and dependencies
  - Development tools and IDE setup
  - Rationale for technology choices
- **Related Teams:**
  - The Council: Technology decisions
  - The Command Center: Deployment technologies

---

#### API_REFERENCE.md
- **Team:** The Workshop
- **Purpose:** Comprehensive API documentation for all services and modules
- **Audience:** Engineers, API consumers, integration partners
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - API endpoints and methods
  - Request/response formats
  - Authentication and authorization
  - Error codes and handling
  - Examples and code snippets
- **Related Teams:**
  - The Vault: API security policies
  - The Studio: API use cases

---

#### TESTING.md
- **Team:** The Workshop
- **Purpose:** Testing strategy, QA processes, test coverage requirements
- **Audience:** Engineers, QA team, test automation engineers
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Testing strategy (unit, integration, E2E)
  - Coverage requirements and goals
  - Test automation setup
  - Performance and load testing
- **Related Teams:**
  - The Studio: User acceptance testing
  - The Command Center: Production testing

---

### 🎨 **The Studio** - Product & Design ([NUMBER] docs)

Product requirements, UX/UI design, user workflows, and feature backlog.

#### REQUIREMENTS.md
- **Team:** The Studio
- **Purpose:** Product requirements, specifications, and feature definitions
- **Audience:** Product managers, engineers, stakeholders
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Core product requirements
  - Feature specifications
  - User stories and acceptance criteria
  - Success metrics
- **Related Teams:**
  - The Workshop: Technical implementation
  - The Council: Stakeholder approvals
  - The Vault: Compliance requirements

---

#### DESIGN_SYSTEM.md
- **Team:** The Studio
- **Purpose:** Design patterns, UI components, brand guidelines, style guide
- **Audience:** Designers, frontend engineers, brand managers
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Design tokens and variables
  - Component library
  - Typography and color system
  - Accessibility standards
  - Brand guidelines
- **Related Teams:**
  - The Workshop: Component implementation
  - The Vault: Accessibility compliance

---

#### USER_WORKFLOWS.md
- **Team:** The Studio
- **Purpose:** User journeys, interaction patterns, and workflow documentation
- **Audience:** Product designers, UX researchers, product managers
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - User personas
  - Journey maps and flows
  - Interaction patterns
  - Pain points and opportunities
- **Related Teams:**
  - The Workshop: Workflow implementation
  - The Studio: Design system components

---

#### BACKLOG.md
- **Team:** The Studio
- **Purpose:** Feature ideas, product roadmap, prioritization framework
- **Audience:** Product managers, stakeholders, engineering leads
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Feature backlog by priority
  - Roadmap by version/milestone
  - Prioritization criteria
  - Ideas and experiments
- **Related Teams:**
  - The Council: Strategic priorities
  - The Workshop: Technical feasibility

---

### 🛡️ **The Vault** - Security & Governance ([NUMBER] docs)

Security policies, compliance rules, data governance, and business rules.

#### SECURITY.md
- **Team:** The Vault
- **Purpose:** Security policies, threat model, vulnerability reporting
- **Audience:** Security team, engineers, compliance officers
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Security policies and standards
  - Threat model and attack vectors
  - Vulnerability reporting process
  - Security incident response
- **Related Teams:**
  - The Workshop: Security implementation
  - The Command Center: Security monitoring
  - The Council: Security decisions

---

#### COMPLIANCE.md
- **Team:** The Vault
- **Purpose:** Regulatory compliance requirements (GDPR, SOC2, etc.)
- **Audience:** Compliance officers, legal team, engineers
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Applicable regulations
  - Compliance requirements
  - Audit trails and evidence
  - Compliance monitoring
- **Related Teams:**
  - The Vault: Related policies
  - The Command Center: Compliance infrastructure

---

#### BUSINESS_RULES.md
- **Team:** The Vault
- **Purpose:** Critical business logic, policies, and non-negotiable rules
- **Audience:** All teams - these rules override technical preferences
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Business logic rules
  - Policy statements
  - Rule hierarchy and conflicts
  - Exceptions and edge cases
- **Related Teams:**
  - All teams: Must adhere to these rules

---

#### DATA_GOVERNANCE.md
- **Team:** The Vault
- **Purpose:** Data handling, privacy policies, retention rules, data lifecycle
- **Audience:** Data engineers, compliance officers, engineers
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Data classification
  - Privacy policies
  - Retention and deletion rules
  - Data access controls
- **Related Teams:**
  - The Workshop: Data architecture
  - The Command Center: Data backups

---

### ⚙️ **The Command Center** - Operations ([NUMBER] docs)

Deployment, monitoring, incident response, and infrastructure management.

#### DEPLOYMENT.md
- **Team:** The Command Center
- **Purpose:** Deployment procedures, infrastructure as code, CI/CD pipelines
- **Audience:** DevOps, SREs, release managers
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Deployment procedures
  - Environment configuration
  - CI/CD pipeline setup
  - Rollback procedures
- **Related Teams:**
  - The Workshop: Build artifacts
  - The Vault: Deployment security

---

#### RUNBOOK.md
- **Team:** The Command Center
- **Purpose:** Operational procedures, troubleshooting guides, on-call playbooks
- **Audience:** On-call engineers, SREs, support team
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Common operational tasks
  - Troubleshooting guides
  - Emergency procedures
  - Escalation paths
- **Related Teams:**
  - The Workshop: Technical troubleshooting
  - The Vault: Security incidents

---

#### MONITORING.md
- **Team:** The Command Center
- **Purpose:** Observability, metrics, alerts, dashboards, SLOs
- **Audience:** SREs, engineers, on-call team
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Monitoring strategy
  - Key metrics and SLIs/SLOs
  - Alert definitions and thresholds
  - Dashboard locations
- **Related Teams:**
  - The Workshop: Application metrics
  - The Vault: Security monitoring

---

#### INCIDENTS.md
- **Team:** The Command Center
- **Purpose:** Incident response procedures, post-mortems, lessons learned
- **Audience:** Incident commanders, SREs, engineering leadership
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Incident response process
  - Post-mortem template
  - Historical incidents
  - Action items and improvements
- **Related Teams:**
  - The Council: Major incident communication
  - The Workshop: Technical root causes

---

### 🤝 **The Council** - Stakeholders & Decisions ([NUMBER] docs)

Business context, stakeholder decisions, organizational knowledge, and glossary.

#### STAKEHOLDERS.md
- **Team:** The Council
- **Purpose:** Key stakeholders, roles, responsibilities, communication channels
- **Audience:** All team members, especially leadership
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Stakeholder directory
  - Roles and responsibilities
  - Communication channels
  - Decision-making authority
- **Related Teams:**
  - All teams: Stakeholder alignment

---

#### DECISIONS.md
- **Team:** The Council
- **Purpose:** Architecture Decision Records (ADRs), major choices, rationale
- **Audience:** All team members, especially architects and leadership
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Decision log (ADR format)
  - Context and rationale
  - Consequences and trade-offs
  - Status (proposed, accepted, deprecated)
- **Related Teams:**
  - The Workshop: Technical decisions
  - The Studio: Product decisions
  - The Vault: Governance decisions

---

#### GLOSSARY.md
- **Team:** The Council
- **Purpose:** Business terminology, domain language, acronyms, standard terms
- **Audience:** All team members, especially new joiners
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Business terminology
  - Technical acronyms
  - Team names and roles
  - Domain-specific language
- **Related Teams:**
  - All teams: Consistent terminology

---

#### CONTEXT.md
- **Team:** The Council
- **Purpose:** Business background, organizational knowledge, "why we exist"
- **Audience:** All team members, especially new joiners and stakeholders
- **Last Updated:** [YYYY-MM-DD]
- **Key Sections:**
  - Business context
  - Company/product history
  - Market positioning
  - Strategic goals
- **Related Teams:**
  - The Studio: Product vision
  - The Council: Strategic decisions

---

## 📊 Cross-Team Reference Map

This shows how teams collaborate and reference each other:

```
🏛️ The Library (Mission Control)
    ├── Coordinates all teams
    ├── claude.md defines team structure
    └── document-index.md tracks all docs

🔬 The AI Lab
    ├── References: The Library (workflows)
    ├── References: The Vault (security policies)
    └── Supports: All teams (automation)

🏗️ The Workshop
    ├── References: The Studio (requirements)
    ├── References: The Vault (security architecture)
    ├── References: The Council (tech decisions)
    └── Implements: Product features

🎨 The Studio
    ├── References: The Council (strategic direction)
    ├── References: The Vault (compliance requirements)
    └── Defines: User experience

🛡️ The Vault (Highest Priority)
    ├── Governs: All teams
    ├── Overrides: Technical preferences when needed
    └── Ensures: Security, compliance, business rules

⚙️ The Command Center
    ├── References: The Workshop (deployment artifacts)
    ├── References: The Vault (operational security)
    └── Operates: Production systems

🤝 The Council
    ├── Provides: Business context to all teams
    ├── Records: Major decisions
    └── Maintains: Stakeholder alignment
```

---

## 🔄 Policy Hierarchy

When teams conflict, this priority order applies:

1. 🛡️ **The Vault** (Security & Compliance) - HIGHEST PRIORITY
2. 🤝 **The Council** (Business Rules & Stakeholder Decisions)
3. 🎨 **The Studio** (Product Requirements)
4. 🏗️ **The Workshop** (Technical Architecture)
5. 🔬 **The AI Lab** (AI Agent Preferences) - LOWEST PRIORITY

**Example:** If The Vault prohibits something, all other teams must comply.

---

## 📋 Document Status Tracking

### ✅ Complete & Up-to-Date

**The Library:**
- README.md
- claude.md
- document-index.md

**The AI Lab:**
- (Add docs as created)

**The Workshop:**
- (Add docs as created)

**The Studio:**
- (Add docs as created)

**The Vault:**
- (Add docs as created)

**The Command Center:**
- (Add docs as created)

**The Council:**
- (Add docs as created)

### 🚧 In Progress
- (List docs currently being written)

### 📝 Planned
- (List planned future documents)

---

## 🧪 Maintenance Checklist

When creating or modifying documents:

- [ ] Document assigned to correct team
- [ ] Listed in this index under team category
- [ ] Timestamp current (YYYY-MM-DD) in doc AND index
- [ ] Description accurate and clear
- [ ] Related teams cross-referenced
- [ ] Bidirectional links present
- [ ] Policy hierarchy respected
- [ ] Changes committed atomically

---

## 📅 Document Freshness

**Recently Updated (Last 7 Days):**
- (List docs updated in last 7 days)

**Needs Review (>30 Days Old):**
- (List docs older than 30 days)

**Stale (>90 Days Old):**
- (List docs older than 90 days that need refresh)

---

## 🎯 Quick Navigation by Need

**Setting up as new AI agent?**
→ Read README.md, then claude.md (entire file), then document-index.md

**Need to understand AI capabilities?**
→ The AI Lab: AI_AGENTS.md, INTENTS.md, PROMPTS.md

**Working on features?**
→ The Studio: REQUIREMENTS.md, DESIGN_SYSTEM.md, BACKLOG.md

**Implementing code?**
→ The Workshop: ARCHITECTURE.md, TECH_STACK.md, API_REFERENCE.md

**Checking security/compliance?**
→ The Vault: SECURITY.md, BUSINESS_RULES.md, COMPLIANCE.md

**Deploying or operating systems?**
→ The Command Center: DEPLOYMENT.md, RUNBOOK.md, MONITORING.md

**Understanding business context?**
→ The Council: STAKEHOLDERS.md, DECISIONS.md, CONTEXT.md

---

## 📈 Document Statistics

- **Total Documents:** [NUMBER] (current) + [NUMBER] (planned) = [TOTAL]
- **Teams:** 7 (Library, AI Lab, Workshop, Studio, Vault, Command Center, Council)
- **Total Words:** ~[ESTIMATE] across all current documents
- **Documentation Coverage:** [PHASE_DESCRIPTION]

---

## 📚 Version History

**[YYYY-MM-DD]** - Team-based architecture implementation
- Reorganized all documentation by teams
- Created 7 knowledge domains with clear responsibilities
- Implemented conversational intent mapping
- Established policy hierarchy
- Added cross-team reference map

**[Future updates will be listed here]**

---

## 📝 Notes

**About This System:**
- Documentation organized by **Teams** (knowledge domains)
- Each team owns specific types of knowledge
- Teams reference each other through cross-links
- Policy hierarchy resolves conflicts
- System is self-documenting and self-evolving

**Maintenance:**
- Update this index **every time** a document is created/modified/deleted
- Use YYYY-MM-DD format for all timestamps
- Assign every document to exactly one primary team
- Update cross-team references when teams interact
- Respect policy hierarchy when conflicts arise

**For Template Users:**
- This is a template - customize for your project
- Add/remove teams based on your needs
- Keep team names memorable and fun
- Ensure conversational intents map clearly to teams

---

**This document is the source of truth for what documentation exists in [PROJECT_NAME].**
