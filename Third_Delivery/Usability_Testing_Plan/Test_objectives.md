# Test Objectives

## Usability Testing – CGRH Self-Service System
## UADY Benefits System

**Prepared by:** Héctor Barrera, Rodrigo Alonzo, Héctor Castro, Damián Villares

**Date:** April 2026

**Course:** Human-Computer Interaction — Faculty of Mathematics, UADY

**Semester:** January – June 2026

---

## 1. Purpose of the Test

This usability test evaluates the CGRH Self-Service System prototype with active UADY employees — both teaching staff and administrative personnel. The test is part of the third and final phase of the User-Centered Design (UCD) process followed throughout this project, corresponding to the **Evaluate designs against requirements** phase defined in ISO 9241-210:2019.

The system is designed to allow university staff to autonomously access their payroll receipts (CFDI), Retirement Savings Fund (FAR), and Savings Fund (Fondo de Ahorro) without relying on in-person visits to the CGRH or waiting for email delivery.

The purpose of this test is not to evaluate the participants — it is to evaluate the system. Findings will be used to identify usability problems, prioritize them by severity, and iterate on the prototype before the final delivery.

---

## 2. Background

The two usability attributes selected as critical priorities for this system were identified through qualitative analysis of six semi-structured interviews conducted on March 20, 2026, with active UADY employees. The affinity diagram derived from those interviews produced eight insight groups, from which two attributes were elevated as the highest-risk areas for system adoption:

**Navigability** — Five out of six participants identified navigation difficulty as their primary pain point when using web platforms. The system will be used infrequently (biweekly for payroll, every six months for savings funds), which means users may feel like first-time users every time they return. If navigation is not intuitive enough to be re-learned without effort, users will abandon the system and revert to the current email-based process.

**Learnability** — The interview data showed that the majority of users escalate to external help or abandon tasks entirely at the first sign of confusion. Only two out of six participants attempt to resolve problems independently. This means the system cannot rely on users troubleshooting on their own — it must be simple enough to understand from the first interaction and consistent enough to require minimal re-learning after periods of inactivity.

These two attributes directly inform the structure, tasks, and metrics of this usability test.

---

## 3. Primary Objectives

### Objective 1 — Evaluate Navigability

Determine whether active UADY employees can locate and access the system's core functions — login, CFDI retrieval, Savings Fund consultation, and logout — without external assistance and within a reasonable amount of time.

**This objective addresses the following research questions:**

- Can users move through the system's main flows (RF03, RF10, RF30, RF04) without getting lost or taking unnecessary detours?
- Do users understand where they are within the system at any given point, and do they know how to go back or continue?
- When users make a navigation error — such as entering the wrong section or clicking the wrong button — does the system help them recover, or does it leave them stuck?
- Are the labels, section names, and terminology used in the interface (e.g., CFDI, Fondo de Ahorro, FAR) recognizable to users without prior explanation?

**Metrics linked to this objective:** NAV-01, NAV-02, NAV-03, NAV-04, NAV-05, NAV-06.

---

### Objective 2 — Evaluate Learnability

Determine whether active UADY employees can understand how the system works from their first interaction, and whether that understanding is retained well enough to allow them to reuse the system after a period of inactivity with minimal relearning.

**This objective addresses the following research questions:**

- How quickly do users execute each function correctly for the first time, without instructions beyond the task scenario?
- Do users improve their performance when repeating the same task in a second round, and by how much?
- How often do users request help from the moderator, and at which points in the flow does this happen most?
- Do users perceive the system as consistent — meaning that what they learn in one section transfers naturally to other sections?
- At the end of the session, can users describe how they would complete the main tasks again without being prompted?

**Metrics linked to this objective:** APR-01, APR-02, APR-03, APR-04, APR-05, APR-06.

---

## 4. Secondary Objectives

Beyond the two primary dimensions, the test will also gather evidence relevant to the following secondary concerns identified during the research phase:

**System feedback and status visibility.** All six interview participants stated they expect an explicit confirmation — on-screen or by email — after completing any action. The test will observe whether users express uncertainty about whether an action was completed, and whether they attempt to repeat actions due to lack of feedback.

**Terminology comprehension.** Participants in the interview phase had no difficulty with general navigation concepts but may not immediately associate technical labels (CFDI, FAR) with their meaning. The test will note whether users hesitate or verbalize confusion when encountering these terms.

**Session security on shared computers.** One participant (E5) raised the specific concern that sessions may remain open on shared computers. The logout task (RF04) is included in the test to verify that the logout option is findable and used without prompting.

---

## 5. What This Test Will and Will Not Measure

| In scope | Out of scope |
|---|---|
| Task completion rate per flow | Back-end performance or server response time |
| Time on task per scenario | Registration flow (RF01) — requires email verification not feasible in test environment |
| Navigation errors and detours | Password recovery full flow (RF02) — email dependency; initiation step only will be observed |
| Help requests per task | Accessibility compliance (screen reader, keyboard navigation) |
| SUS score (global usability perception) | Mobile responsiveness — test will be conducted on desktop only |
| Learnability improvement between rounds | Comparative evaluation against other systems |
| Perceived orientation and consistency | |
| Short-term retention of learned flows | |

---

## 6. Success Criteria

The test will be considered successful — meaning the prototype is ready for the final delivery — if the following thresholds are met:

| Metric | Threshold |
|---|---|
| Task completion rate (NAV-01) | ≥ 85% across all tasks and participants |
| Help requests per task (APR-03) | ≤ 1 per task per participant |
| SUS score | ≥ 68 (acceptable); target ≥ 75 given user profile |
| Perceived orientation — Likert item (NAV-05) | Average ≥ 4 out of 5 |
| Perceived learnability — SUS item (APR-04) | Average ≥ 4 out of 5 |
| Severity 4 problems (catastrophic) | 0 — none present after iteration |

If any threshold is not met, the corresponding flows must be revised and, where possible, re-tested before the final prototype is submitted.

---

## 7. Connection to Functional Requirements

| Functional Requirement | Related Objective | Tasks that exercise it |
|---|---|---|
| RF03 — Login | Navigability, Learnability | Task 1 |
| RF10 — CFDI Consultation | Navigability, Learnability | Task 2 |
| RF30 — Savings Fund Consultation | Navigability | Task 3 |
| RF02 — Password Recovery (partial) | Navigability, Learnability | Task 4 |
| RF04 — Logout | Navigability | Task 5 |
| RF05 — Main Menu | Navigability, Learnability | Tasks 2, 3, 4, 5 |

---

## References

- ISO 9241-210:2019. *Ergonomics of human-system interaction — Part 210: Human-centred design for interactive systems*. International Organization for Standardization.
- Nielsen, J. (1994). *10 Usability Heuristics for User Interface Design*. Nielsen Norman Group.
- Nielsen, J. (2000). *Why You Only Need to Test with 5 Users*. Nielsen Norman Group.
- Brooke, J. (1996). SUS: A quick and dirty usability scale. In P. W. Jordan et al. (Eds.), *Usability Evaluation in Industry*. Taylor & Francis.
- Fisk, A. D., Rogers, W. A., Charness, N., Czaja, S. J., & Sharit, J. (2018). *Designing for Older Adults: Principles and Creative Human Factors Approaches* (3rd ed.). CRC Press.
