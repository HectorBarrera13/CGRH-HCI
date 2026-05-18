# Benchmark — Ideal Clicks and Expert Reference Times

## Usability Testing – CGRH Self-Service System
## UADY Benefits System

**Document type:** Internal — for team use only. Not shown to participants.

**Prepared by:** Héctor Barrera, Rodrigo Alonzo, Héctor Castro, Damián Villares

**Date:** April 2026

**Course:** Human-Computer Interaction — Faculty of Mathematics, UADY

**Semester:** January – June 2026

---

## Purpose

This document defines two reference values used to calculate NAV-02 and NAV-03 during usability testing analysis:

- **Ideal click count** — the minimum number of clicks required to complete each task following the optimal path through the prototype, with no errors, no backtracking, and no exploratory detours. This value is used to calculate the ratio of unnecessary clicks per participant (NAV-03).
- **Expert reference time** — the time a team member familiar with the system takes to complete each task on the prototype, following the optimal path without hesitation. This value is used as the benchmark against which participant times (NAV-02) are compared.

Both values must be established before the first participant session. They are fixed for the duration of the testing phase — do not update them mid-study, as this would make results across sessions incomparable.

---

## How to Establish Expert Reference Times Before Sessions

One team member who is familiar with the prototype but has not been involved in its visual design must complete each task three times following the optimal path. Record the time for each attempt and take the average. This controls for interface loading time and minor interaction variability.

| Attempt | T1 | T2 | T3 | T4 | T5 | T6 |
|---|---|---|---|---|---|---|
| Run 1 (mm:ss) | | | | | | |
| Run 2 (mm:ss) | | | | | | |
| Run 3 (mm:ss) | | | | | | |
| **Average** | | | | | | |

Fill in the average times above before the first session and carry those values forward into the task benchmark tables below.

---

## How to Use This Document During Analysis

**NAV-02 — Time on task ratio:**
> Participant ratio = participant time ÷ expert reference time
> A ratio of 1.0 means the participant matched the expert. A ratio of 2.0 means they took twice as long. Ratios above 3.0 on any task indicate a significant usability problem in that flow.

**NAV-03 — Unnecessary click ratio:**
> Participant ratio = participant click count ÷ ideal click count
> A ratio of 1.0 means the participant followed the optimal path exactly. The threshold for this study is ≤ 2.0 — anything above indicates the navigation structure in that flow is not clear enough.

---

## Task Benchmarks

---

### Task 1 — Login

**Objective:** Enter credentials and reach the main menu.

#### Optimal path

| Step | Action | Click # |
|---|---|---|
| 1 | Click on the username field | 1 |
| 2 | Type username | — |
| 3 | Click on the password field | 2 |
| 4 | Type password | — |
| 5 | Click the login button | 3 |

**Ideal click count: 3**

> Typing actions are not counted as clicks. Only discrete click interactions with interface elements count toward the ideal click total. If the prototype auto-focuses the username field on load, step 1 does not count — adjust to **2 clicks** if confirmed in the pilot session.

#### Reference times

| Value | Time |
|---|---|
| Expert reference time (average of 3 runs) | \_\_\_ : \_\_\_ |
| Participant threshold (3× expert) | \_\_\_ : \_\_\_ |
| Maximum acceptable time | **3:00** |

> The maximum acceptable time (3:00) is derived from participant expectations stated in the interview phase. E4 said the system should be "as fast as email." Login is a prerequisite action — if it takes more than 3 minutes, users are likely to abandon before reaching any functional content.

---

### Task 2 — CFDI Download (Round 1)

**Objective:** Navigate from the main menu to the CFDI section, identify the most recent receipt, and download it as a PDF.

#### Optimal path

| Step | Action | Click # |
|---|---|---|
| 1 | Click on the CFDI / Recibos de Nómina option in the main menu | 1 |
| 2 | Identify the most recent receipt in the list | — |
| 3 | Click on the download button for the most recent receipt | 2 |
| 4 | Confirm download if a dialog appears | 3 |

**Ideal click count: 2–3**

> The range accounts for whether the prototype presents a download confirmation dialog. If no dialog appears and the file downloads directly on click, the ideal count is **2**. Confirm during the pilot session and fix one value before participant sessions begin.

#### Reference times

| Value | Time |
|---|---|
| Expert reference time (average of 3 runs) | \_\_\_ : \_\_\_ |
| Participant threshold (3× expert) | \_\_\_ : \_\_\_ |
| Maximum acceptable time | **5:00** |

> This task has the highest maximum acceptable time because it is the most common use case and the one with the most navigation steps. E5 stated a maximum of 5–10 minutes for payroll tasks. The 5:00 threshold is set at the conservative end of that range.

---

### Task 3 — Savings Fund Consultation

**Objective:** Navigate from the main menu to the Savings Fund section and locate the current balance.

#### Optimal path

| Step | Action | Click # |
|---|---|---|
| 1 | Click on the Fondo de Ahorro option in the main menu | 1 |
| 2 | Read the balance displayed on screen | — |

**Ideal click count: 1**

> This is the simplest task in the test. If the balance is displayed immediately upon entering the section without any additional interaction required, the optimal path is a single click. If the participant must click a secondary element to reveal the balance, add one click and update to **2**.

#### Reference times

| Value | Time |
|---|---|
| Expert reference time (average of 3 runs) | \_\_\_ : \_\_\_ |
| Participant threshold (3× expert) | \_\_\_ : \_\_\_ |
| Maximum acceptable time | **3:00** |

> The Savings Fund is consulted every six months. It should be immediately accessible once the section is entered — no further navigation should be required to see the balance figure.

---

### Task 4 — Password Recovery

**Objective:** From the login screen, initiate the password recovery flow and reach the email confirmation screen.

#### Optimal path

| Step | Action | Click # |
|---|---|---|
| 1 | Click on the "¿Olvidaste tu contraseña?" or equivalent recovery link | 1 |
| 2 | Click on the email input field | 2 |
| 3 | Type institutional email | — |
| 4 | Click the submit / send button | 3 |

**Ideal click count: 3**

> If the recovery link is placed prominently below the login form and the email field is auto-focused after clicking it, the count reduces to **2**. Confirm during the pilot session.

#### Reference times

| Value | Time |
|---|---|
| Expert reference time (average of 3 runs) | \_\_\_ : \_\_\_ |
| Participant threshold (3× expert) | \_\_\_ : \_\_\_ |
| Maximum acceptable time | **4:00** |

> Password recovery is measured only up to the confirmation screen — not through the full email link flow, which depends on email infrastructure outside the prototype. The 4:00 threshold accounts for the extra cognitive effort this task requires compared to a standard navigation task.

---

### Task 5 — Logout

**Objective:** Find and use the logout option to end the session.

#### Optimal path

| Step | Action | Click # |
|---|---|---|
| 1 | Click on the logout option (menu, avatar, or header element) | 1 |
| 2 | Confirm logout if a dialog appears | 2 |

**Ideal click count: 1–2**

> If logout is a single click with no confirmation dialog, the ideal count is **1**. If the prototype requires a confirmation step, it is **2**. Fix this value during the pilot session.

#### Reference times

| Value | Time |
|---|---|
| Expert reference time (average of 3 runs) | \_\_\_ : \_\_\_ |
| Participant threshold (3× expert) | \_\_\_ : \_\_\_ |
| Maximum acceptable time | **1:00** |

> Logout should be the fastest task in the test. A time above 1 minute almost certainly means the logout option was not findable — which is the primary usability risk for this task given the shared-computer concern identified in the research phase.

---

### Task 6 — CFDI Download (Round 2)

**Objective:** Log in and download the second most recent payroll receipt.

#### Optimal path

| Step | Action | Click # |
|---|---|---|
| 1 | Click on the username field | 1 |
| 2 | Type username | — |
| 3 | Click on the password field | 2 |
| 4 | Type password | — |
| 5 | Click the login button | 3 |
| 6 | Click on the CFDI / Recibos de Nómina option | 4 |
| 7 | Identify and click the download button for the second most recent receipt | 5 |
| 8 | Confirm download if a dialog appears | 6 |

**Ideal click count: 5–6**

> This task combines the login flow (Task 1) and the CFDI download flow (Task 2). The combined ideal count is the sum of both. The range accounts for the download confirmation dialog as in Task 2.

#### Reference times

| Value | Time |
|---|---|
| Expert reference time (average of 3 runs) | \_\_\_ : \_\_\_ |
| Participant threshold (3× expert) | \_\_\_ : \_\_\_ |
| Maximum acceptable time | **3:00** |

> The maximum acceptable time for this task is set lower than Task 2 (5:00) because it is a second attempt. By this point the participant has already completed login and CFDI download once. A time significantly higher than Task 2 is a direct signal that the system was not retained — the gap between Task 2 and Task 6 times feeds directly into the APR-02 improvement calculation.

---

## Consolidated Reference Table

| Task | Ideal clicks | Max acceptable time | Expert time (to fill) | Participant threshold (3×) |
|---|---|---|---|---|
| T1 — Login | 2–3 | 3:00 | \_\_\_ : \_\_\_ | \_\_\_ : \_\_\_ |
| T2 — CFDI Round 1 | 2–3 | 5:00 | \_\_\_ : \_\_\_ | \_\_\_ : \_\_\_ |
| T3 — Savings Fund | 1–2 | 3:00 | \_\_\_ : \_\_\_ | \_\_\_ : \_\_\_ |
| T4 — Password Recovery | 2–3 | 4:00 | \_\_\_ : \_\_\_ | \_\_\_ : \_\_\_ |
| T5 — Logout | 1–2 | 1:00 | \_\_\_ : \_\_\_ | \_\_\_ : \_\_\_ |
| T6 — CFDI Round 2 | 5–6 | 3:00 | \_\_\_ : \_\_\_ | \_\_\_ : \_\_\_ |

---

## Pilot Session Checklist

Before the first participant session, complete the following steps using this document:

- [ ] Run each task three times on the prototype following the optimal path
- [ ] Record times for all three runs per task and calculate averages
- [ ] Confirm ideal click counts — adjust any ranges to fixed values based on actual prototype behavior
- [ ] Fill in the expert reference times in the consolidated reference table above
- [ ] Calculate the 3× participant threshold for each task and fill in the table
- [ ] Keep this document open alongside the Error Register and Success Time Table during all sessions

---

## Notes on Prototype Behavior

Record any deviations from the assumed optimal paths discovered during the pilot session:

| Task | Assumed behavior | Actual behavior | Adjusted ideal clicks |
|---|---|---|---|
| | | | |
| | | | |
| | | | |
| | | | |

---

## References

- Nielsen, J. (1994). *10 Usability Heuristics for User Interface Design*. Nielsen Norman Group.
- Rubin, J., & Chisnell, D. (2008). *Handbook of Usability Testing: How to Plan, Design, and Conduct Effective Tests* (2nd ed.). Wiley.
- Tullis, T., & Albert, B. (2013). *Measuring the User Experience: Collecting, Analyzing, and Presenting Usability Metrics* (2nd ed.). Morgan Kaufmann.
