# Project Feasibility

## CGRH Self-Service System – UADY

---

## Arguments Supporting Project Success

The requirements are limited to authentication, session management, and data retrieval: conventional web development patterns with no real-time processing or complex external integrations. CFDI, FAR, and Savings Fund data reside in institutional databases under the CGRH's direct jurisdiction, eliminating authorization dependencies between units. The UADY provides server infrastructure without the need for external hosting.

Since the system is read-only — users view information without modifying it — the security risk surface is reduced and the scope of regression testing is contained. The restriction to desktop further simplifies the presentation layer to a single rendering environment.

---

## Team Strengths and Weaknesses

| Dimension | Strength | Weakness |
|---|---|---|
| Technical | Familiarity with web development and standard authentication patterns | Limited experience integrating with legacy institutional systems |
| Methodological | HCI approach with a defined and justified user segment | Reduced experience conducting usability testing with older adults |
| Organizational | Access to UADY's institutional context and ties with the CGRH | Dependency on the unit's availability and timeline for data validation |
| Scope | Functional requirements are well-defined and bounded | Risk of scope creep if the CGRH requests additional features |

---

## HCI Challenges and Mitigation Strategies

### Challenge 1: Recruiting Users for Usability Testing

Recruiting retirees over 60 for usability testing requires active coordination with the CGRH and logistics adapted to this profile's mobility and availability constraints, given that they no longer have regular presence at university facilities. Using younger substitute participants would invalidate the specific signal that justifies the project's user segmentation and produce misleading usability findings.

**Mitigation:** Secure a collaboration letter with the CGRH early in the semester to facilitate contact with retirees. Design short-format test sessions (30–45 min), preferably in remote format or at a location accessible to the participant, not the team.

### Challenge 2: Cognitive Load in the Registration Flow (RF01)

The registration flow requires users to provide their employee key, RFC, CURP, and institutional email in a single session — a high cognitive demand for users with limited digital experience. A poorly sequenced or insufficiently guided form at this stage leads to early abandonment before the user accesses any of the system's core value.

**Mitigation:** Apply progressive disclosure principles to break the form into clearly separated steps with explicit progress indicators. Plan at least two usability evaluation cycles with the target segment before considering RF01 stable, prioritizing first-use sessions with participants who have no prior experience with the system.

### Challenge 3: Error Communication and Recovery

Standard web error messages (e.g., "Invalid credentials", "RFC format incorrect") assume a level of technical literacy that the retiree segment may not have. Poorly written error messages at RF02 and RF03 can cause users to abandon the system entirely rather than attempt recovery.

**Mitigation:** Design all error states with plain language, specific guidance on how to correct the issue, and no technical jargon. Validate error message comprehension explicitly during usability testing by asking participants to explain what the message means and what they would do next.

### Challenge 4: Mental Model Mismatch

Retirees may have built their mental model of accessing payroll or savings information around the current email-and-request process. The shift to a self-service portal introduces a new interaction paradigm that may conflict with established habits, particularly around authentication and session management.

**Mitigation:** Conduct contextual inquiry sessions before prototyping to map existing mental models. Use onboarding cues and familiar language in the UI (e.g., referencing the types of documents they currently receive by email) to bridge the gap between the old process and the new system.

---

*Last updated: February 2026*
