# OctoAcme Project Management Docs

## Overview
OctoAcme organizes work around a pragmatic, lightweight project lifecycle: Initiation, Planning, Execution, Release, and Retrospective. Projects begin with a Project One-pager to capture the problem, goals, success metrics, stakeholders, and a rough timeline. Approved initiatives move into planning where the team runs a kickoff, builds a prioritized backlog with acceptance criteria and estimates, defines a Definition of Done, and records dependencies and risks.

Day-to-day execution uses practical workflows and clear ownership. A project board follows the flow Backlog → Ready → In Progress → In Review → QA → Done. Pull requests are small, CI-gated, and include acceptance criteria and issue links. Core personas include Project Managers (PM), Product Managers (PdM), Developers, QA, and Stakeholders — each with defined responsibilities for planning, delivery, and acceptance.

Communication is structured to maintain transparency and fast decision-making: short daily standups for blockers and progress, regular planning and demo/review ceremonies, weekly PM–PdM syncs, and monthly stakeholder updates. Cross-team dependencies and risks are tracked in a Risk Register and escalated through a documented path when needed.

Quality assurance and risk control are integrated into the workflow. Teams are expected to provide unit and integration tests, end-to-end smoke tests for critical flows, and automated security scanning in CI. Releases follow checklists (staging verification, rollback plans, release notes) and incidents trigger a blameless retrospective whose action items feed back into the backlog and risk register for continuous improvement.

## Quick Links to Process Documents
- Project Management Overview: ./octoacme-project-management-overview.md
- Project Initiation Guide: ./octoacme-project-initiation.md
- Project Planning: ./octoacme-project-planning.md
- Execution & Tracking: ./octoacme-execution-and-tracking.md
- Risk Management & Communication: ./octoacme-risks-and-communication.md
- Release & Deployment Guide: ./octoacme-release-and-deployment.md
- Retrospective & Continuous Improvement: ./octoacme-retrospective-and-continuous-improvement.md
- Roles & Personas: ./octoacme-roles-and-personas.md

## Acceptance checklist
- [ ] Content aligns with existing process docs
- [ ] Update improves clarity or closes a documented gap
- [ ] Proposed content has been reviewed with stakeholders (if needed)

## How to use
Add this README to the docs/ folder as the primary entry point for OctoAcme project management documentation. Link to it from onboarding materials and project READMEs to speed newcomer ramp-up.
