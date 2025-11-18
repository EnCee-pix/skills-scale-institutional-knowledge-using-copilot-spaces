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

## Product Owner

### Role Summary
Product Owners define and prioritize product backlog items, ensuring the development team delivers maximum business value. They act as the primary interface between stakeholders and the delivery team.

### Responsibilities
- Maintain and prioritize the product backlog
- Define and communicate acceptance criteria
- Make trade-off decisions on scope, schedule, and quality
- Validate delivered features against business objectives
- Facilitate backlog refinement sessions

### Goals
- Maximize return on investment (ROI) from development efforts
- Ensure clear, actionable user stories and acceptance criteria
- Balance technical debt with new feature delivery

### Key Deliverables
- Prioritized product backlog
- User story definitions with acceptance criteria
- Sprint goals and commitments
- Stakeholder alignment on priorities

### RACI Interaction Points
- **Accountable**: backlog prioritization, acceptance decisions
- **Responsible**: defining acceptance criteria, sprint planning input
- **Consulted by**: Project Manager on scope changes, Developers on requirements clarity
- **Informs**: stakeholders on roadmap changes, Release Manager on feature readiness

### Escalation Path
Team-level blockers → Product Owner → Product Manager → Executive Sponsor

### Common Scenarios
- **Backlog Prioritization**: Works with Product Manager to understand strategic goals, then sequences backlog items based on value, dependencies, and team capacity.
- **Mid-Sprint Scope Changes**: Evaluates emergency requests against current sprint commitments, consults with Project Lead and team before accepting changes.
- **Acceptance Review**: Validates completed features against acceptance criteria, provides feedback to developers, and approves or rejects for release.

---

## Release Manager

### Role Summary
Release Managers coordinate the end-to-end release process, ensuring deployments are safe, well-communicated, and properly validated. They own release readiness and deployment execution.

### Responsibilities
- Plan and schedule release windows
- Coordinate release readiness reviews
- Manage deployment execution and validation
- Maintain release documentation and runbooks
- Facilitate go/no-go decisions
- Coordinate rollback procedures when needed

### Goals
- Zero-downtime deployments with minimal risk
- Clear communication to all affected parties
- Repeatable, reliable release processes

### Key Deliverables
- Release calendar and schedules
- Release readiness reports
- Deployment runbooks and checklists
- Post-release validation reports
- Release retrospectives

### RACI Interaction Points
- **Accountable**: release execution, deployment quality
- **Responsible**: release planning, deployment coordination, validation
- **Consulted by**: DevOps on deployment strategies, QA on test completion, Product Owner on feature readiness
- **Informs**: stakeholders on release status, support teams on new features, Project Manager on release risks

### Escalation Path
Deployment issues → Release Manager → DevOps Lead + Project Manager → Engineering Manager → Incident Commander (for critical issues)

### Common Scenarios
- **Release Coordination**: Reviews readiness checklist with QA, DevOps, and Product Owner; schedules deployment window; coordinates pre-deployment communications.
- **Deployment Issue**: Identifies problem during deployment validation, coordinates with DevOps on diagnosis, makes rollback decision if needed, triggers incident response if critical.
- **Release Communication**: Prepares stakeholder announcements, coordinates with support team on feature changes, updates release notes and documentation.

---

## Risk Champion

### Role Summary
Risk Champions proactively identify, assess, and track project risks, ensuring visibility and timely mitigation. They facilitate risk discussions and maintain the risk register.

### Responsibilities
- Identify and document project risks
- Assess risk likelihood and impact
- Facilitate risk review sessions
- Track mitigation actions to completion
- Escalate high-priority risks appropriately
- Maintain and update the risk register

### Goals
- No surprises: identify risks before they become issues
- Clear ownership and mitigation plans for all significant risks
- Regular risk visibility to stakeholders

### Key Deliverables
- Updated risk register (weekly minimum)
- Risk assessment reports
- Escalation notifications for high-priority risks
- Risk mitigation tracking
- Risk retrospective insights

### RACI Interaction Points
- **Accountable**: risk register accuracy and completeness
- **Responsible**: risk identification, assessment, tracking
- **Consulted by**: Project Manager on risk severity, team members on mitigation strategies
- **Informs**: stakeholders on significant risks, Project Manager on escalations, Quality Advocate on quality-related risks

### Escalation Path
High risks → Risk Champion → Project Manager → Product Manager + Sponsor (for strategic risks)

### Common Scenarios
- **Risk Identification**: During sprint planning, identifies dependency on external team with unclear timeline; documents in risk register with likelihood and impact assessment.
- **Risk Escalation**: Monitors risk of key developer leaving; when confirmed, escalates to Project Manager with mitigation recommendations (knowledge transfer, backup resources).
- **Risk Review**: Facilitates weekly risk review, updates status of existing risks, archives resolved risks, raises new concerns from team feedback.

---

## Quality Advocate

### Role Summary
Quality Advocates champion quality practices across the project lifecycle, ensuring testability, observability, and adherence to quality standards. They work embedded with delivery teams.

### Responsibilities
- Define and communicate quality standards
- Review features for testability and observability
- Facilitate test strategy and coverage discussions
- Monitor quality metrics and trends
- Advocate for technical quality improvements
- Support test automation initiatives

### Goals
- Build quality in from the start, not test it in at the end
- High confidence in releases through comprehensive testing
- Continuous improvement of quality practices

### Key Deliverables
- Test strategy and coverage plans
- Quality metrics dashboards
- Test automation framework recommendations
- Quality gates definition
- Quality retrospective insights

### RACI Interaction Points
- **Accountable**: quality standards definition, quality advocacy
- **Responsible**: test strategy, quality metrics, testability reviews
- **Consulted by**: Developers on test approaches, Release Manager on quality gates, Product Owner on quality trade-offs
- **Informs**: Project Manager on quality risks, stakeholders on quality status, QA team on testing priorities

### Escalation Path
Quality issues → Quality Advocate → Project Lead + Product Owner → Engineering Manager (for systemic issues)

### Common Scenarios
- **Testability Review**: Reviews feature designs early in sprint planning, identifies hard-to-test scenarios, works with developers to refactor for testability before implementation.
- **Quality Gate Discussion**: Identifies test coverage gap before release, escalates to Product Owner and Release Manager, facilitates go/no-go decision based on risk assessment.
- **Quality Metrics**: Tracks increasing defect density trend, presents findings in retrospective, facilitates team discussion on root causes and improvement actions.

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- See [Role Interaction Matrix](role-interaction-matrix.md) for detailed collaboration patterns.
- See [Risk Log Template](risk-log-template.md) for Risk Champion workflow.
- See [Release Checklist](release-checklist.md) for Release Manager workflow.
