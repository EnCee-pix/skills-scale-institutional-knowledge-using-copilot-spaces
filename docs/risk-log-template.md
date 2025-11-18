# OctoAcme Risk Log Template

## Purpose
A structured risk register to identify, assess, track, and mitigate project risks throughout the project lifecycle. The Risk Champion maintains this log and facilitates regular reviews.

**Related Documentation:**
- [Risk Management & Communication](octoacme-risks-and-communication.md)
- [Roles and Personas](octoacme-roles-and-personas.md) (Risk Champion)
- [Release Checklist](release-checklist.md)

---

## Risk Register Overview

**Project Name:** _[Enter project name]_  
**Risk Champion:** _[Name]_  
**Last Updated:** _[Date]_  
**Review Frequency:** Weekly during active development, Bi-weekly during maintenance

---

## Risk Priority Matrix

Risks are prioritized using Likelihood × Impact:

| Likelihood / Impact | Low | Medium | High |
|---------------------|-----|--------|------|
| **High** | Medium | High | Critical |
| **Medium** | Low | Medium | High |
| **Low** | Low | Low | Medium |

**Priority Definitions:**
- **Critical**: Immediate attention required, escalate to leadership
- **High**: Requires mitigation plan and active monitoring
- **Medium**: Monitor and review regularly, plan mitigation
- **Low**: Document and review periodically

---

## Risk Register

### Risk Template (YAML Format)

```yaml
risks:
  - id: RISK-001
    description: "Brief description of the risk"
    likelihood: "Low | Medium | High"
    impact: "Low | Medium | High"
    priority: "Low | Medium | High | Critical"
    category: "Technical | Resource | Schedule | External | Quality | Security"
    owner: "Name of person responsible"
    mitigation: "Actions taken to reduce likelihood or impact"
    contingency: "Backup plan if risk materializes"
    status: "Open | In Progress | Mitigated | Closed | Accepted"
    dateIdentified: "YYYY-MM-DD"
    lastReviewed: "YYYY-MM-DD"
    targetResolution: "YYYY-MM-DD"
    escalationContact: "Name or role to escalate to"
    notes: "Additional context or updates"
```

---

## Risk Register (Markdown Table Format)

| ID | Description | Likelihood | Impact | Priority | Owner | Mitigation | Status | Last Reviewed | Escalation Contact |
|----|-------------|------------|--------|----------|-------|------------|--------|---------------|-------------------|
| RISK-001 | Key developer assigned to another project mid-sprint | Medium | High | High | Project Manager | Cross-train team members; document critical knowledge | In Progress | 2024-01-15 | Engineering Manager |
| RISK-002 | Third-party API availability uncertain during launch | High | Medium | High | Tech Lead | Implement fallback mechanism; establish SLA with vendor | Open | 2024-01-15 | Product Manager |
| RISK-003 | Database migration may cause extended downtime | Low | High | Medium | DevOps Lead | Test migration on staging; prepare rollback script; schedule maintenance window | Mitigated | 2024-01-14 | Release Manager |
| RISK-004 | Scope creep from late feature requests | Medium | Medium | Medium | Product Owner | Enforce change control process; maintain prioritized backlog | Open | 2024-01-15 | Product Manager |
| RISK-005 | Insufficient test coverage for edge cases | Medium | Medium | Medium | Quality Advocate | Implement additional test cases; conduct exploratory testing | In Progress | 2024-01-15 | QA Lead |

---

## Example Risk Entries

### RISK-001: Key Developer Departure

**Description:** Senior developer with critical system knowledge may leave the team mid-project.

**Category:** Resource  
**Likelihood:** Medium  
**Impact:** High  
**Priority:** High  

**Owner:** Project Manager  
**Escalation Contact:** Engineering Manager  

**Mitigation Strategy:**
- Implement pair programming and knowledge sharing sessions
- Document critical system components and architectural decisions
- Cross-train at least two team members on critical areas
- Maintain updated technical documentation

**Contingency Plan:**
- Identify backup resources from other teams
- Prioritize features to complete critical work early
- Consider contractor support if needed

**Status:** In Progress  
**Date Identified:** 2024-01-10  
**Last Reviewed:** 2024-01-15  
**Target Resolution:** 2024-01-31  

**Notes:**
- 2024-01-15: Knowledge transfer sessions scheduled twice weekly
- 2024-01-12: Documentation sprint completed for authentication module

---

### RISK-002: External API Dependency

**Description:** Project depends on third-party API with no formal SLA; outages could block critical functionality.

**Category:** External  
**Likelihood:** High  
**Impact:** Medium  
**Priority:** High  

**Owner:** Tech Lead  
**Escalation Contact:** Product Manager  

**Mitigation Strategy:**
- Implement circuit breaker pattern for API calls
- Add caching layer for frequently accessed data
- Create fallback UI for degraded mode
- Establish monitoring and alerting for API health
- Negotiate SLA with vendor

**Contingency Plan:**
- Maintain cached data for up to 24 hours
- Display user-friendly degraded mode messaging
- Have manual workaround process documented for critical operations

**Status:** In Progress  
**Date Identified:** 2024-01-05  
**Last Reviewed:** 2024-01-15  
**Target Resolution:** 2024-01-25  

**Notes:**
- 2024-01-15: Circuit breaker implementation merged
- 2024-01-10: SLA discussion initiated with vendor
- 2024-01-08: Monitoring alerts configured

---

### RISK-003: Security Vulnerability in Dependency

**Description:** Critical security vulnerability discovered in third-party library used in production.

**Category:** Security  
**Likelihood:** Medium  
**Impact:** High  
**Priority:** Critical  

**Owner:** Security Lead  
**Escalation Contact:** Engineering Manager → CISO  

**Mitigation Strategy:**
- Immediate patch evaluation and testing
- Emergency release planning if patch available
- Temporary workaround or feature disablement if needed
- Communication plan for customers if data exposed

**Contingency Plan:**
- Disable affected feature temporarily
- Implement compensating controls
- Accelerate migration to alternative library

**Status:** Closed  
**Date Identified:** 2024-01-12  
**Last Reviewed:** 2024-01-14  
**Target Resolution:** 2024-01-13 (Completed)  

**Notes:**
- 2024-01-14: Patch deployed to production successfully
- 2024-01-13: Emergency patch tested and approved
- 2024-01-12: Vulnerability confirmed, patch available from vendor

---

## Risk Review Process

### Weekly Risk Review Agenda (15-30 minutes)

1. **Review Open Risks** (10 min)
   - Update status of existing risks
   - Verify mitigation actions are progressing
   - Escalate any risks increasing in priority

2. **Add New Risks** (5 min)
   - Capture newly identified risks
   - Assign initial assessment and owner

3. **Close Resolved Risks** (5 min)
   - Verify mitigation success
   - Document lessons learned
   - Archive closed risks

4. **Escalation Needs** (5 min)
   - Identify risks requiring leadership attention
   - Prepare escalation communications

### Risk Review Participants
- **Required:** Risk Champion, Project Manager, Tech Lead
- **Optional:** Product Owner, QA Lead, DevOps Lead, relevant stakeholders
- **As Needed:** Subject matter experts for specific risks

---

## Risk Escalation Criteria

Escalate risks when:
- Priority level reaches **Critical**
- Impact or Likelihood increases to **High**
- Mitigation actions are blocked or ineffective
- Risk requires resources or decisions outside team authority
- Risk threatens project delivery or business objectives
- Security or compliance risks are identified

**Escalation Path:**
1. Team-level: Risk Champion → Project Manager
2. Program-level: Project Manager → Product Manager
3. Leadership-level: Product Manager → Engineering Manager / Executive Sponsor
4. Critical/Security: Direct escalation to Security/Incident Response

---

## Risk Categories

| Category | Description | Examples |
|----------|-------------|----------|
| **Technical** | Technology, architecture, integration challenges | Performance issues, technical debt, integration complexity |
| **Resource** | People, skills, availability concerns | Key person dependency, skill gaps, competing priorities |
| **Schedule** | Timeline, dependencies, delivery risks | Missed milestones, dependencies on other teams, aggressive deadlines |
| **External** | Third-party dependencies, market factors | Vendor delays, API changes, regulatory changes |
| **Quality** | Defects, technical debt, test coverage | Insufficient testing, known bugs, quality metrics trending negative |
| **Security** | Vulnerabilities, compliance, data protection | Security vulnerabilities, compliance violations, data exposure |

---

## Risk Status Definitions

| Status | Definition |
|--------|------------|
| **Open** | Risk identified, mitigation plan needed or in progress |
| **In Progress** | Mitigation actions actively being executed |
| **Mitigated** | Mitigation successful, monitoring continues |
| **Closed** | Risk no longer applicable or fully resolved |
| **Accepted** | Risk acknowledged, decision made to accept without mitigation |

---

## Instructions for Use

### For Risk Champions:
1. **Create a copy** of this template for your project
2. **Schedule regular reviews** (weekly recommended during active development)
3. **Update the register** before each review meeting
4. **Facilitate risk discussions** with the team
5. **Ensure owners are assigned** and taking action
6. **Escalate appropriately** based on priority and urgency
7. **Archive closed risks** but keep them accessible for retrospectives

### For Team Members:
1. **Report risks early** - don't wait for them to become issues
2. **Participate in reviews** - provide updates on your mitigation actions
3. **Take ownership** when assigned risks
4. **Communicate blockers** that prevent mitigation progress

### For Stakeholders:
1. **Review risk summaries** in weekly status reports
2. **Support mitigation efforts** by unblocking resources or decisions
3. **Escalate externally** when risks require organizational support

---

## Risk Report Template (for Status Updates)

```markdown
## Risk Summary - [Date]

**Critical Risks:** [Count]
**High Priority Risks:** [Count]
**Total Active Risks:** [Count]

### New Risks This Week:
- RISK-XXX: [Brief description] - Priority: [Level]

### Risks Closed This Week:
- RISK-XXX: [Brief description] - Resolution: [How resolved]

### Top 3 Risks Requiring Attention:
1. RISK-XXX: [Description] - Owner: [Name] - Status: [Status]
2. RISK-XXX: [Description] - Owner: [Name] - Status: [Status]
3. RISK-XXX: [Description] - Owner: [Name] - Status: [Status]

### Escalations Needed:
- [List any risks requiring leadership attention]
```

---

## Tips for Effective Risk Management

✅ **Do:**
- Identify risks early and often
- Be specific and concrete in risk descriptions
- Assign clear owners for each risk
- Update status regularly and honestly
- Escalate proactively when needed
- Document lessons learned from materialized risks

❌ **Don't:**
- Ignore small risks (they can snowball)
- Blame individuals for raising risks
- Let risks go stale without review
- Over-mitigate low-priority risks
- Forget to close resolved risks
- Skip risk reviews when "everything is fine"

---

**Related Templates:**
- [Release Checklist](release-checklist.md) - includes risk review as part of release readiness
- [Role Interaction Matrix](role-interaction-matrix.md) - shows risk-related collaboration patterns
- [Retrospective Guide](octoacme-retrospective-and-continuous-improvement.md) - use closed risks in retrospectives
