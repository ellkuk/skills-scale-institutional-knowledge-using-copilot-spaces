# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

---

## Additional / Operational Personas (proposed additions)

The following operational and cross-functional personas are commonly needed for production-grade delivery. Adding them clarifies ownership across release, reliability, security, documentation, and customer-facing activities.

### Release Engineer / Build & Release Lead
Role Summary
- Owns build pipelines, release automation, and deployment processes.

Responsibilities
- Maintain and improve CI/CD pipelines and release automation.
- Coordinate deployments and ensure rollback strategies are tested and documented.
- Ensure artifacts are reproducible and promote release safety (e.g., gating, canaries).
- Validate pre-release checks (tests, security scans) and coordinate release approvals.

Interactions
- Works closely with Developers (to integrate build changes), SRE/Operations (for deployment hooks), and the Project Manager (for scheduling).
- Triggers stakeholder communications with the Release Coordinator or PM for major releases.

Example artifacts
- Deployment runbooks, CI pipeline definitions, release checklists, rollback playbooks.

---

### Release Coordinator
Role Summary
- Manages release scheduling, cross-team coordination, and stakeholder communications for releases.

Responsibilities
- Maintain release calendar and coordinate cross-team windows.
- Draft and publish release notes and stakeholder announcements.
- Ensure release cutoffs and approvals are observed.
- Coordinate with Support for customer-facing communications.

Interactions
- Works with Release Engineer (technical execution), PM (business timing), and Support/Product (communication and readiness).

Example artifacts
- Release calendar, release notes template, announcement checklist.

---

### SRE / Production Operations
Role Summary
- Responsible for production reliability, monitoring, and operational readiness.

Responsibilities
- Define and maintain production monitoring and alerting.
- Own incident response and run incident post-mortems.
- Partner on capacity planning and performance tuning.
- Perform post-deploy verification and health checks.

Interactions
- Works with Developers to improve observability and resolve production issues.
- Reports health and availability metrics to PM and Product Lead.
- Collaborates with Release Engineer on safe deployment practices.

Example artifacts
- Runbooks, dashboards, SLO/SLA definitions, post-incident reports.

---

### Security / Compliance Champion
Role Summary
- Ensures security and compliance requirements are applied during design, development, and release.

Responsibilities
- Conduct security reviews and threat modeling for new features.
- Ensure vulnerabilities found in scans are triaged and remediated.
- Maintain compliance checklists and coordinate audits as needed.
- Escalate critical security issues to Product Lead and Security team.

Interactions
- Works with Developers to remediate issues, with CI owners to automate scans, and with Product/PM to prioritize fixes for release readiness.

Example artifacts
- Threat models, security review notes, scan reports, compliance checklist.

---

### UX / Design Lead
Role Summary
- Owns user-facing design direction, usability, and accessibility considerations.

Responsibilities
- Create and validate design assets, flows, and prototypes.
- Define design acceptance criteria and accessibility requirements.
- Participate in acceptance reviews and usability testing.

Interactions
- Collaborates with Product Managers on user goals and acceptance criteria.
- Works with Developers to ensure design fidelity and with QA to include usability checks.

Example artifacts
- Design specs, accessibility checklist, user research summaries.

---

### Accessibility / Inclusive Design Advocate
Role Summary
- Ensures accessibility and inclusive design practices are embedded into delivery.

Responsibilities
- Review acceptance criteria for accessibility requirements.
- Run accessibility audits and guide remediation.
- Advocate for inclusive design practices during planning and reviews.

Interactions
- Partners with UX, QA, and Developers to incorporate fixes into sprints and release plans.

Example artifacts
- Accessibility audit reports, acceptance criteria checklists, remediation plans.

---

### Data / Analytics Owner
Role Summary
- Defines measurement strategy and ensures telemetry is in place to validate outcomes.

Responsibilities
- Define key metrics and success criteria for features.
- Ensure telemetry and event tracking are implemented correctly.
- Validate post-release metrics and generate analysis for Product/PM.

Interactions
- Works with PdM to define metrics, Developers to implement instrumentation, and PM to report outcomes.

Example artifacts
- Metrics definitions (dashboard specs), instrumentation checklists, post-release metric reports.

---

### Support / Customer Success Representative
Role Summary
- Connects product delivery with customer feedback and support readiness.

Responsibilities
- Provide input on customer impact and urgency for issues.
- Prepare support playbooks and knowledge base updates.
- Surface recurring or systemic customer issues and patterns.

Interactions
- Coordinates with PM for communications, with Developers for bug fixes, and with Documentation Owner for knowledge base updates.

Example artifacts
- Support playbooks, KB articles, triage reports.

---

### Documentation Owner / Technical Writer
Role Summary
- Produces and maintains user-facing and internal documentation, including runbooks and release notes.

Responsibilities
- Create and update user guides, runbooks, API docs, and release notes.
- Ensure documentation is reviewed and published alongside releases.
- Align docs with product behavior and maintain versioning.

Interactions
- Works with Developers for technical accuracy, with PM for release notes content, and with Support to keep KB up to date.

Example artifacts
- User guides, runbooks, release notes, API docs.

---

## Mapping & Handoff Guidance (summary)
- Initiation & Planning: Product Manager, PM, UX, and Data Owner define goals and success criteria; Security and Accessibility should be consulted early for constraints.
- Execution: Developers, Release Engineer, SRE, and Documentation Owner collaborate on build, testing, observability, and docs.
- Release: Release Engineer + Release Coordinator + Support coordinate execution, communications, and follow-up.
- Post-release: SRE and Data Owner verify health and metrics; PM coordinates retrospective and action items; Documentation Owner publishes final notes.

---

## How to add these to the docs
- Add each persona as a subsection under Roles & Personas with Role Summary, Responsibilities, Interactions, Example Artifacts.
- Include a mapping table that shows role involvement by project stage for quick reference.
- Make sure acceptance criteria for each role (e.g., "Telemetry implemented" for Data Owner) are concrete and linked to backlog items where applicable.
