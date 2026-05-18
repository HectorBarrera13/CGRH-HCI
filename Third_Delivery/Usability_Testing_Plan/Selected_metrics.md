# Selected Usability Metrics

## Usability Testing – CGRH Self-Service System
## UADY Benefits System

**Prepared by:** Héctor Barrera, Rodrigo Alonzo, Héctor Castro, Damián Villares

**Date:** April 2026

**Course:** Human-Computer Interaction — Faculty of Mathematics, UADY

**Semester:** January – June 2026

---

## 1. Selection Criteria

The original metric inventory for this project contained 12 metrics across two usability dimensions: 6 for navigability (NAV-01 to NAV-06) and 6 for learnability (APR-01 to APR-06). For the usability testing sessions, **8 metrics have been selected** — 4 per dimension — based on the following criteria:

- **Signal-to-effort ratio.** Priority was given to metrics that produce high-value findings relative to the effort required to collect them in a moderated in-person session with 5 participants.
- **Alignment with identified risks.** The research phase identified two critical failure modes: task abandonment due to navigation difficulty, and lack of system feedback leading to distrust. Selected metrics must directly address at least one of these risks.
- **Feasibility within session constraints.** Metrics that require extended longitudinal observation, specialized equipment, or a large participant sample were deprioritized. The test is designed to be completed in 45–55 minutes per session.
- **Coverage across both user groups.** Selected metrics must be meaningful for both administrative personnel and manual workers, whose behavioral profiles differ significantly in error tolerance and digital competence.

### Deprioritized metrics and rationale

| Metric | Reason for deprioritizing |
|---|---|
| NAV-03 — Number of unnecessary clicks | Requires frame-by-frame screen recording analysis. Meaningful only if click counting infrastructure is available; otherwise produces unreliable manual counts. NAV-04 (navigation errors) captures the same signal more efficiently. |
| APR-05 — Perceived consistency | Overlaps substantially with NAV-05 (perceived orientation). Both address the same underlying user need — predictability of the interface. NAV-05 is retained because it is measurable during the task; APR-05 is absorbed into the post-session debrief question. |
| APR-06 — Short-term retention | Requires a structured verbal recall protocol after all tasks are complete, which adds 10–15 minutes to an already dense session. The information it produces is partially captured by APR-02 (improvement between attempts) and the debrief questions. |

---

## 2. Selected Metrics

---

### Navigability

---

#### NAV-01 — Task Success Rate

| Field | Detail |
|---|---|
| **Dimension** | Navigability |
| **Type** | Quantitative |
| **Threshold** | ≥ 85% completion rate per task across all participants |

**What it measures:**
Whether users can complete each core task — login, CFDI download, Savings Fund consultation, password recovery initiation, and logout — without requesting help from the moderator or abandoning the task.

**Why it was selected:**
This is the most direct measure of whether the system works for its intended users. A task completion rate below 85% on any flow is an immediate signal that the design has a critical problem in that specific path. Given that the manual workers profile has a documented tendency to abandon tasks at the first sign of difficulty, this metric is especially sensitive for that group.

**How to collect it:**
The note-taker records a binary outcome (completed / not completed) for each task on the observation sheet. A task is considered completed only if the participant reaches the defined end state without moderator intervention. Requesting help from the moderator counts as incomplete.

**How to calculate it:**
> Success rate per task = (number of participants who completed the task ÷ total participants) × 100

---

#### NAV-02 — Time on Task

| Field | Detail |
|---|---|
| **Dimension** | Navigability |
| **Type** | Quantitative |
| **Threshold** | See benchmark document for reference times per task |

**What it measures:**
How long it takes each participant to complete each task, from the moment the task card is handed to them until they reach the defined end state or abandon.

**Why it was selected:**
Interview participants expressed a clear expectation: the system should be at least as fast as receiving a document by email. E4 stated it should be "immediate, like email." E5 said payroll tasks should take a maximum of 5–10 minutes. Time on task directly validates whether the system meets this expectation. It also identifies which specific flows are the slowest, informing where navigation simplification is most needed.

**How to collect it:**
The note-taker starts a stopwatch when the task card is handed to the participant and stops it when the task is complete or abandoned. Times are recorded in mm:ss format on the observation sheet.

**How to calculate it:**
> Average time per task = sum of all participant times for that task ÷ number of participants who attempted it

Compare averages against the benchmark times defined in the Benchmark document.

---

#### NAV-04 — Navigation Error Rate

| Field | Detail |
|---|---|
| **Dimension** | Navigability |
| **Type** | Quantitative |
| **Threshold** | ≤ 2 navigation errors per task per participant |

**What it measures:**
How many times a participant enters the wrong section, uses the browser's back button to recover, or visibly loses their orientation before reaching the correct destination within a task.

**Why it was selected:**
The affinity diagram identified navigation inconsistency as the most frequently mentioned pain point across all six interviews (Groups 5 and 8). E6 specifically noted that "navigation changes a lot from one page to another," and E4 stated she forgets how to use platforms she visits infrequently. Navigation errors are the observable symptom of this problem. This metric pinpoints exactly which sections of the interface cause the most disorientation.

**How to collect it:**
The note-taker counts each instance of the following during a task: participant clicks into the wrong section and backtracks, participant uses the browser back button, participant verbalizes being lost or unsure of their location. Each instance counts as one navigation error.

**How to calculate it:**
> Average navigation errors per task = sum of all errors across participants for that task ÷ number of participants who attempted it

---

#### NAV-06 — Error Recovery

| Field | Detail |
|---|---|
| **Dimension** | Navigability |
| **Type** | Qualitative |
| **Threshold** | Participant recovers independently in ≥ 70% of observed error instances |

**What it measures:**
When a participant makes an error — wrong credentials, wrong section, misunderstood instruction — whether they are able to recover and continue the task on their own, with a neutral prompt from the moderator, or not at all.

**Why it was selected:**
The research phase established that the dominant error response among the target users is to stop and ask for help or abandon the task entirely. Only 2 out of 6 interview participants attempt independent recovery. This metric directly tests whether the system's error messages and interface cues are sufficient to support recovery without human assistance — which is the minimum requirement for a system that will be used without in-person support.

**How to collect it:**
The note-taker records each error event and its outcome using three categories: (A) recovered independently, (B) recovered after a neutral moderator prompt, (C) did not recover / abandoned. The moderator may only use neutral prompts — no directional guidance.

**How to analyze it:**
Calculate the percentage of error instances resolved at each level (A, B, C) across all participants and tasks. A high proportion of (C) outcomes in a specific flow indicates a critical design problem in that area.

---

### Learnability

---

#### APR-01 — Time to First Correct Action

| Field | Detail |
|---|---|
| **Dimension** | Learnability |
| **Type** | Quantitative |
| **Threshold** | Compare against benchmark; improvement expected in Task 6 vs Task 2 |

**What it measures:**
How long it takes a participant to execute each function correctly for the first time — first successful login, first successful CFDI download, first successful Savings Fund balance view — without any intervention from the moderator.

**Why it was selected:**
This metric captures the moment of first understanding: how quickly does the interface communicate what it is and what the user should do? For the manual workers profile in particular, a long time-to-first-action signals that the interface is not self-explanatory at first contact, which directly correlates with the risk of abandonment described in the research findings.

**How to collect it:**
The note-taker starts timing from the moment the participant first sees each new screen (login, main menu, CFDI list, Savings Fund section) and stops when the participant executes the correct first action on that screen. This is a sub-measurement within each task's overall time.

**How to calculate it:**
> Average time to first correct action per screen = sum of individual times ÷ number of participants

---

#### APR-02 — Improvement Between Attempts

| Field | Detail |
|---|---|
| **Dimension** | Learnability |
| **Type** | Quantitative |
| **Threshold** | ≥ 20% reduction in time or errors in Task 6 compared to Task 2 |

**What it measures:**
The reduction in time and navigation errors when a participant repeats the CFDI download task in a second round (Task 6) compared to the first round (Task 2). This measures how quickly the system's structure is internalized after a single use.

**Why it was selected:**
This is the most direct empirical measure of learnability available within a single test session. The affinity diagram (Group 8) established that infrequent use — biweekly for payroll, every six months for savings funds — is a defining characteristic of this system's usage pattern. If users show significant improvement between two attempts separated by only 20–30 minutes within the same session, this is a strong indicator that the system is genuinely learnable. If they do not improve, it signals that the interface requires re-learning every time — a critical adoption risk.

**How to collect it:**
Compare the time on task and navigation error count recorded for Task 2 against those recorded for Task 6 for each participant.

**How to calculate it:**
> Improvement rate (time) = ((Task 2 time − Task 6 time) ÷ Task 2 time) × 100
> Improvement rate (errors) = ((Task 2 errors − Task 6 errors) ÷ Task 2 errors) × 100

A result of ≥ 20% improvement in either measure is considered evidence of adequate learnability.

---

#### APR-03 — External Help Requests

| Field | Detail |
|---|---|
| **Dimension** | Learnability |
| **Type** | Quantitative |
| **Threshold** | ≤ 1 help request per task per participant |

**What it measures:**
How many times a participant explicitly asks the moderator for guidance, clicks on help tooltips or tutorials within the prototype, or verbalizes that they do not know how to proceed and are waiting for direction.

**Why it was selected:**
The research phase showed that asking for help is the default response to any difficulty for the majority of participants. In the real usage context, no moderator will be present — users will either solve the problem themselves or abandon the system. Help requests during the test are a direct proxy for the situations where real users would abandon. A high number of help requests in a specific task is a reliable indicator that that task's flow needs redesign.

**How to collect it:**
The note-taker counts each explicit help request per task. Verbalizing confusion ("I don't know where to go") counts only if the participant stops attempting and directs the statement at the moderator. Thinking aloud while continuing to explore does not count.

**How to calculate it:**
> Average help requests per task = total help requests for that task across all participants ÷ number of participants

---

#### APR-04 — Perceived Ease of Learning

| Field | Detail |
|---|---|
| **Dimension** | Learnability |
| **Type** | Qualitative |
| **Threshold** | Average score ≥ 4 out of 5 |

**What it measures:**
The participant's subjective perception of how easy it was to understand the system from scratch, without prior experience or training. This is collected through a dedicated Likert scale item administered after all tasks are complete.

**Why it was selected:**
Quantitative metrics capture what users do; this metric captures how they feel about it. A participant might complete all tasks successfully but still perceive the experience as unnecessarily difficult — a signal that the system demands more cognitive effort than it should. Conversely, a participant who required help might still rate the system as easy to learn if the help was sufficient and the recovery was smooth. Both patterns are informative. This metric also maps directly to the SUS questionnaire item "I learned to use this system very quickly," allowing cross-validation between the Likert item and the global SUS score.

**How to collect it:**
Administered on the Orientation and Learnability Likert Scale post-test instrument, using the item: *"Me resultó fácil entender cómo usar el sistema desde la primera vez."* Scale: 1 (strongly disagree) to 5 (strongly agree).

**How to calculate it:**
> Average perceived ease of learning = sum of all participant scores for this item ÷ number of participants

---

## 3. Metrics Summary Table

| ID | Name | Dimension | Type | Threshold | Collection method |
|---|---|---|---|---|---|
| NAV-01 | Task Success Rate | Navigability | Quantitative | ≥ 85% per task | Binary outcome per task on observation sheet |
| NAV-02 | Time on Task | Navigability | Quantitative | See benchmark | Stopwatch, mm:ss on observation sheet |
| NAV-04 | Navigation Error Rate | Navigability | Quantitative | ≤ 2 per task | Error count on observation sheet |
| NAV-06 | Error Recovery | Navigability | Qualitative | ≥ 70% independent recovery | Outcome category (A/B/C) on observation sheet |
| APR-01 | Time to First Correct Action | Learnability | Quantitative | See benchmark | Sub-timing within each task |
| APR-02 | Improvement Between Attempts | Learnability | Quantitative | ≥ 20% reduction Task 2→6 | Comparison of Task 2 and Task 6 records |
| APR-03 | External Help Requests | Learnability | Quantitative | ≤ 1 per task | Help request count on observation sheet |
| APR-04 | Perceived Ease of Learning | Learnability | Qualitative | Average ≥ 4/5 | Likert scale post-test instrument |

---

## 4. Relationship Between Metrics and Tasks

| Task | NAV-01 | NAV-02 | NAV-04 | NAV-06 | APR-01 | APR-02 | APR-03 | APR-04 |
|---|---|---|---|---|---|---|---|---|
| T1 — Login | ✓ | ✓ | ✓ | ✓ | ✓ | — | ✓ | — |
| T2 — CFDI Round 1 | ✓ | ✓ | ✓ | ✓ | ✓ | baseline | ✓ | — |
| T3 — Savings Fund | ✓ | ✓ | ✓ | ✓ | ✓ | — | ✓ | — |
| T4 — Password Recovery | ✓ | ✓ | ✓ | ✓ | ✓ | — | ✓ | — |
| T5 — Logout | ✓ | ✓ | ✓ | — | — | — | ✓ | — |
| T6 — CFDI Round 2 | ✓ | ✓ | ✓ | — | ✓ | comparison | — | — |
| Post-test | — | — | — | — | — | — | — | ✓ |

---

## References

- Brooke, J. (1996). SUS: A quick and dirty usability scale. In P. W. Jordan et al. (Eds.), *Usability Evaluation in Industry*. Taylor & Francis.
- Nielsen, J. (1994). *10 Usability Heuristics for User Interface Design*. Nielsen Norman Group.
- Rubin, J., & Chisnell, D. (2008). *Handbook of Usability Testing: How to Plan, Design, and Conduct Effective Tests* (2nd ed.). Wiley.
- Tullis, T., & Albert, B. (2013). *Measuring the User Experience: Collecting, Analyzing, and Presenting Usability Metrics* (2nd ed.). Morgan Kaufmann.
