# OctoAcme Role Interaction Matrix

## Purpose
Define clear responsibilities and handoff points between core project roles to reduce friction, prevent gaps, and improve coordination. Use this matrix during project planning, onboarding, and when clarifying "who does what."

**Related Documentation:**
- [Roles and Personas](octoacme-roles-and-personas.md) - detailed role descriptions
- [Project Management Overview](octoacme-project-management-overview.md)
- [Release Checklist](release-checklist.md) - shows roles in action
- [Risk Log Template](risk-log-template.md) - shows risk responsibilities

---

## How to Use This Matrix

### For Project Planning:
- Review the matrix during project kickoff to assign roles
- Identify gaps where responsibilities may be unclear
- Clarify RACI assignments for your specific project

### For Onboarding:
- Share this matrix with new team members
- Use it to explain collaboration patterns
- Reference when questions arise about "who should I talk to?"

### For Issue Resolution:
- Consult when there's confusion about ownership
- Use to identify the right escalation path
- Reference in retrospectives when handoffs fail

### RACI Legend:
- **R** = Responsible (does the work)
- **A** = Accountable (owns the outcome, decision maker)
- **C** = Consulted (provides input)
- **I** = Informed (kept updated)

---

## Core Responsibilities Matrix

| Activity / Deliverable | Program Manager | Project Lead | Product Owner | Release Manager | Risk Champion | Quality Advocate | QA | DevOps |
|------------------------|----------------|--------------|---------------|-----------------|---------------|------------------|----|---------| 
| **Strategic Planning** |
| Product vision & strategy | I | I | A/R | I | I | I | I | I |
| Project portfolio prioritization | A/R | C | C | I | C | I | I | I |
| Resource allocation across projects | A/R | C | I | I | I | I | I | I |
| **Project Initiation** |
| Project charter creation | R | A | C | I | C | I | I | I |
| Stakeholder identification | R | R | C | I | R | I | I | I |
| High-level timeline & milestones | R | A | C | C | C | I | I | C |
| **Backlog & Requirements** |
| Product backlog prioritization | I | C | A/R | I | I | C | C | I |
| User story creation | I | R | A | I | I | C | C | I |
| Acceptance criteria definition | I | C | A/R | I | I | C | C | I |
| Technical requirements | I | A/R | C | I | C | C | C | C |
| **Sprint Planning** |
| Sprint goal definition | I | C | A/R | I | I | I | I | I |
| Sprint capacity planning | C | A/R | C | I | C | I | I | C |
| Task breakdown & estimation | I | R | C | I | C | C | C | C |
| **Development & Quality** |
| Code implementation | I | A | I | I | I | C | I | C |
| Code reviews | I | R | I | I | I | C | C | C |
| Test strategy definition | I | C | C | I | I | A/R | R | C |
| Test case development | I | I | I | I | I | C | A/R | I |
| Automated testing implementation | I | R | I | I | I | C | A/R | C |
| Manual testing execution | I | I | I | C | I | C | A/R | I |
| Quality metrics tracking | I | C | I | C | C | A/R | R | C |
| Technical debt management | I | A/R | C | I | C | C | I | C |
| **Risk & Issue Management** |
| Risk identification | C | R | C | C | A/R | C | C | C |
| Risk assessment & prioritization | C | C | C | C | A/R | C | C | C |
| Risk mitigation planning | C | R | C | C | A/R | C | C | R |
| Risk register maintenance | I | C | I | C | A/R | C | I | I |
| Issue escalation | R | R | C | C | R | C | C | C |
| **Release Management** |
| Release planning & scheduling | C | C | C | A/R | C | C | C | C |
| Release readiness assessment | I | C | C | A/R | C | C | R | R |
| Deployment execution | I | I | I | A | I | I | C | R |
| Release validation | I | C | C | A/R | I | C | R | R |
| Rollback decision | I | C | C | A/R | C | C | C | R |
| Release notes | I | C | C | A/R | I | I | I | I |
| **Communication** |
| Stakeholder status updates | A/R | R | C | C | C | I | I | I |
| Team standup facilitation | I | A/R | C | I | I | I | I | I |
| Sprint reviews | C | A/R | R | I | I | C | C | I |
| Retrospectives | C | A/R | R | C | C | C | C | C |
| Incident communication | R | C | C | R | C | C | I | R |
| **Project Closure** |
| Final deliverable sign-off | C | C | A | R | I | C | C | C |
| Project retrospective | A/R | R | R | R | R | R | R | R |
| Lessons learned documentation | R | R | C | C | C | C | C | C |
| Handoff to operations/support | C | C | C | R | C | C | C | A/R |

---

## Key Handoff Points

### 1. Requirements → Development

**From:** Product Owner  
**To:** Project Lead, Developers  
**Handoff:** User stories with acceptance criteria  

**Success Criteria:**
- Stories are clear, testable, and estimated
- Dependencies and constraints are identified
- Technical feasibility has been validated

**Common Issues:**
- Unclear or incomplete acceptance criteria
- Missing non-functional requirements
- Undiscovered technical constraints

**Best Practices:**
- Backlog refinement sessions before sprint planning
- Technical spike stories for uncertain work
- Written acceptance criteria in user story format

---

### 2. Development → QA

**From:** Developers  
**To:** QA, Quality Advocate  
**Handoff:** Feature branch with tests, ready for validation  

**Success Criteria:**
- All automated tests passing
- Feature deployed to test environment
- Test data prepared and documented
- Known limitations documented

**Common Issues:**
- Environment differences not accounted for
- Incomplete test data
- Undocumented assumptions

**Best Practices:**
- Definition of Done checklist
- Test environment parity with production
- Developers participate in test case review

---

### 3. QA → Release Manager

**From:** QA, Quality Advocate  
**To:** Release Manager  
**Handoff:** Validated features ready for release  

**Success Criteria:**
- All test cases executed and passed
- Known issues documented and triaged
- Regression testing completed
- Quality gates met

**Common Issues:**
- Last-minute bugs discovered
- Test coverage gaps
- Performance issues found late

**Best Practices:**
- Continuous testing throughout sprint
- Quality gates defined early
- Release readiness dashboard

---

### 4. Release Manager → DevOps

**From:** Release Manager  
**To:** DevOps  
**Handoff:** Release package ready for deployment  

**Success Criteria:**
- Release checklist completed
- Deployment runbook reviewed
- Rollback plan tested
- Monitoring configured

**Common Issues:**
- Missing deployment steps
- Configuration drift between environments
- Insufficient monitoring

**Best Practices:**
- Infrastructure as Code
- Automated deployment pipelines
- Pre-deployment validation in staging

---

### 5. DevOps → Operations/Support

**From:** DevOps, Release Manager  
**To:** Operations, Support team  
**Handoff:** Production deployment with documentation  

**Success Criteria:**
- Release notes published
- Support documentation updated
- Known issues communicated
- Monitoring dashboards accessible

**Common Issues:**
- Support team surprised by changes
- Incomplete troubleshooting guides
- Unclear escalation paths

**Best Practices:**
- Support team involved in release planning
- Runbooks for common issues
- Post-release knowledge transfer session

---

### 6. Risk Champion → Project Lead

**From:** Risk Champion  
**To:** Project Lead, Project Manager  
**Handoff:** Updated risk register with escalations  

**Success Criteria:**
- All risks assessed and prioritized
- Mitigation owners assigned
- High-priority risks flagged for action
- Escalation needs identified

**Common Issues:**
- Risks identified too late
- Mitigation plans not acted upon
- Unclear ownership

**Best Practices:**
- Weekly risk reviews
- Risk metrics in status reports
- Clear escalation triggers

---

## Collaboration Patterns

### Pattern 1: Feature Delivery (Happy Path)

```
Product Owner → Project Lead → Developers → QA → Release Manager → DevOps → Production
         ↓                                    ↓                ↓
    Acceptance Criteria              Quality Gates      Release Validation
```

**Key Roles:** Product Owner, Project Lead, QA, Release Manager, DevOps  
**Duration:** 1-3 sprints typically  
**Critical Handoffs:** Requirements → Development, Development → QA, QA → Release

---

### Pattern 2: Risk Escalation

```
Risk Champion → Project Manager → Product Manager → Executive Sponsor
       ↓               ↓                    ↓
Risk Register    Decision Log        Strategic Pivot
```

**Key Roles:** Risk Champion, Project Manager, Product Manager  
**Duration:** Hours to days depending on severity  
**Critical Handoffs:** Risk identification → Escalation decision, Decision → Communication

---

### Pattern 3: Incident Response

```
On-call Alert → DevOps → Release Manager → Incident Commander → Stakeholders
                   ↓            ↓                    ↓
              Investigation  Rollback?          Communication
                                  ↓
                           Post-Incident Review
```

**Key Roles:** DevOps, Release Manager, Incident Commander, Project Manager  
**Duration:** Minutes to hours for resolution, days for post-incident  
**Critical Handoffs:** Detection → Response, Response → Communication, Incident → Learning

---

### Pattern 4: Quality Gate Review

```
Quality Advocate → QA → Product Owner → Release Manager
        ↓           ↓          ↓              ↓
   Test Strategy  Execute  Accept/Reject  Go/No-Go Decision
```

**Key Roles:** Quality Advocate, QA, Product Owner, Release Manager  
**Duration:** Hours to days before release  
**Critical Handoffs:** Quality assessment → Product decision, Product decision → Release decision

---

## Escalation Paths by Issue Type

| Issue Type | First Contact | Escalates To | Final Escalation |
|------------|---------------|--------------|------------------|
| **Technical blockers** | Project Lead | Engineering Manager | CTO |
| **Resource conflicts** | Project Manager | Program Manager | VP Engineering |
| **Scope/requirements** | Product Owner | Product Manager | VP Product |
| **Quality concerns** | Quality Advocate | QA Lead + Project Lead | Engineering Manager |
| **Release issues** | Release Manager | DevOps Lead + Project Manager | Engineering Manager |
| **Security incidents** | DevOps | Security Lead | CISO |
| **Customer escalations** | Support Manager | Product Manager | VP Customer Success |
| **Vendor/external** | Project Manager | Procurement + Product Manager | VP Operations |

---

## Role Interaction Anti-Patterns (Avoid These)

❌ **Skipping QA:** Developer → Release Manager (bypassing QA)
- **Risk:** Quality issues in production
- **Fix:** Enforce quality gates and Definition of Done

❌ **Shadow backlog:** Project Manager creates tasks without Product Owner
- **Risk:** Misaligned priorities, scope creep
- **Fix:** All work flows through prioritized backlog

❌ **Last-minute heroics:** Developer deploys directly to production
- **Risk:** Undocumented changes, incidents
- **Fix:** Enforce release process, even for hotfixes

❌ **Risk hoarding:** Team member doesn't report risks to Risk Champion
- **Risk:** Surprises, missed mitigation opportunities
- **Fix:** Psychological safety, regular risk discussions

❌ **Communication silos:** Release happens without support team notification
- **Risk:** Poor customer experience, repeat escalations
- **Fix:** Release checklist includes communication steps

---

## Decision Rights Matrix

| Decision | Primary Decision Maker | Must Consult | Must Inform |
|----------|----------------------|--------------|-------------|
| **Feature prioritization** | Product Owner | Product Manager, Project Lead | Team |
| **Technical approach** | Project Lead | Developers, Quality Advocate | Product Owner |
| **Release timing** | Release Manager | Product Owner, DevOps | Stakeholders |
| **Go/No-Go for release** | Release Manager | Product Owner, QA Lead, DevOps Lead | Stakeholders, Support |
| **Rollback decision** | Release Manager | DevOps, Incident Commander | All teams |
| **Risk escalation** | Risk Champion | Project Manager | Leadership |
| **Sprint scope changes** | Product Owner | Project Lead, Team | Stakeholders |
| **Resource allocation** | Program Manager | Project Manager, Engineering Manager | Team |

---

## Quick Reference: "Who Do I Contact For...?"

| Need | Contact | Alternative |
|------|---------|-------------|
| Prioritizing new work | Product Owner | Product Manager |
| Understanding requirements | Product Owner | Business Analyst |
| Technical architecture questions | Project Lead | Tech Lead/Architect |
| Quality concerns | Quality Advocate | QA Lead |
| Release planning | Release Manager | DevOps Lead |
| Risk reporting | Risk Champion | Project Manager |
| Status updates | Project Manager | Project Lead |
| Resource needs | Project Manager | Program Manager |
| Deployment issues | DevOps | Release Manager |
| Production incidents | DevOps On-call | Incident Commander |
| Test environment issues | QA | DevOps |

---

## Onboarding Checklist for New Team Members

Use this matrix to understand your role interactions:

- [ ] Review your role description in [Roles and Personas](octoacme-roles-and-personas.md)
- [ ] Identify your RACI assignments in the matrix above
- [ ] Note your key collaboration partners
- [ ] Understand your escalation paths
- [ ] Review relevant handoff patterns for your role
- [ ] Schedule intro meetings with your key partners
- [ ] Clarify decision rights for your responsibilities
- [ ] Bookmark relevant templates and checklists

---

## Tips for Effective Collaboration

✅ **Do:**
- Communicate early and often, especially at handoff points
- Document decisions and share with relevant stakeholders
- Respect role boundaries while maintaining team spirit
- Escalate proactively when blocked
- Ask for clarification when RACI is unclear

❌ **Don't:**
- Bypass defined processes without good reason
- Make unilateral decisions that affect others
- Assume someone else is handling a handoff
- Wait until the last minute to involve dependent roles
- Hoard information or work in silos

---

**Related Resources:**
- [Roles and Personas](octoacme-roles-and-personas.md) - detailed role descriptions and scenarios
- [Release Checklist](release-checklist.md) - roles in action during releases
- [Risk Log Template](risk-log-template.md) - Risk Champion workflow
- [Project Management Overview](octoacme-project-management-overview.md) - high-level process context
