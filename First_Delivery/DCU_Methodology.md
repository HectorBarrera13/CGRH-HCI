# User-Centered Design (UCD) Methodology

## CGRH System – UADY

**Course:** Human-Computer Interaction — Faculty of Mathematics, UADY  
**Semester:** January – June 2026

---

## 1. Methodology Overview

This project adopts **User-Centered Design (UCD)** as its guiding methodology, following the iterative process defined in **ISO 9241-210:2019** (*Human-centred design for interactive systems*). UCD places the target user at the center of every design and evaluation decision, ensuring that the system is built around real needs, behaviors, and limitations rather than technical assumptions.

The UCD process is structured in four iterative phases:

```
1. Understand and specify the context of use
        ↓
2. Specify user and organizational requirements
        ↓
3. Produce design solutions
        ↓
4. Evaluate designs against requirements
        ↑_______________(iterate)_______________↑
```

Each phase informs the next, and evaluation findings feed back into earlier phases as needed.

---

## 2. How We Are Implementing UCD

Given that this is an academic project carried out by a student team without access to professional UX infrastructure, our implementation of UCD is adapted to our context and resources:

- **No expert evaluators** — heuristic evaluations are conducted by team members following established frameworks (Nielsen, 1994).
- **Limited participant access** — user sessions are coordinated through the CGRH and adapted to participants' availability and mobility.
- **Iterative across deliveries** — each course delivery corresponds to a UCD phase, building progressively on the previous one.
- **Evidence-based decisions** — all design choices must be traceable to a research finding, requirement, or established HCI principle.

---

## 3. UCD Phase Mapping by Delivery

| UCD Phase | Activities | Project Delivery |
|---|---|---|
| **1. Understand context of use** | User research (interviews, surveys, contextual inquiry), user profiles, personas, scenarios | **1st Delivery** |
| **2. Specify requirements** | Functional and non-functional requirements derived from research findings | **1st Delivery** |
| **3. Produce design solutions** | Wireframes, prototypes (low and medium fidelity), interaction flows | **2nd Delivery** |
| **4. Evaluate designs** | Usability testing with target users, heuristic evaluation, SUS scoring, iteration | **3rd Delivery** |

---

## 4. Current Status — 1st Delivery

In this first delivery, the UCD process has **not yet been fully executed**. The work completed corresponds to the **foundation phases** of the methodology:

- The **context of use** has been defined through secondary research (ENDUTIH 2023, domain analysis, functional requirements review) and documented in the user profiles and proto-personas.
- The **requirements** have been specified based on the defined user profile and mapped to HCI usability attributes.
- The **research instruments** (interview guide, contextual inquiry protocol, survey, usability testing protocol) have been designed and are ready for execution.

What has **not yet happened** in this delivery:

- Field sessions with real users have not been conducted.
- Personas are proto-personas based on secondary data, not validated with primary research.
- No design solutions or prototypes have been produced yet.

> The field research phase — interviews, contextual inquiry, surveys, and usability testing with real retired UADY employees — is planned for the next sprint and will produce the primary data needed to validate and refine the proto-personas, scenarios, and requirements documented here.

---

## 5. Planned Implementation — 2nd and 3rd Delivery

### 2nd Delivery — Design Solutions

With field research data collected, the team will:

1. Refine personas and scenarios based on real user evidence (`Personas_Final.md`).
2. Identify the highest-priority design problems from research results.
3. Produce **low-fidelity wireframes** for the critical flows: RF01 (registration), RF02 (password recovery), RF03 (login), and RF05 (main menu).
4. Iterate wireframes based on team review and alignment with the defined NFRs.
5. Produce **medium-fidelity prototypes** for user validation.

### 3rd Delivery — Evaluation and Iteration

With prototypes ready, the team will:

1. Conduct **usability testing sessions** with retired UADY employees using the protocol defined in `04_Usability_Testing_Protocol.md`.
2. Apply the **SUS questionnaire** and score results.
3. Classify findings using Nielsen's severity scale.
4. Iterate on the prototype to address critical and high-severity issues.
5. Document a final heuristic evaluation against Nielsen's 10 heuristics.

---

## 6. Artifact Traceability

Every artifact in this repository is linked to a specific UCD phase:

| Artifact | UCD Phase |
|---|---|
| `User_Research_Plan.md` | Phase 1 — Context of use |
| `01_Interview_Guide.md` | Phase 1 — Context of use |
| `02_Contextual_Inquiry_Protocol.md` | Phase 1 — Context of use |
| `03_User_Survey.md` | Phase 1 — Context of use |
| `User_Profiles_and_Personas.md` | Phase 1 — Context of use |
| `Scenarios.md` | Phase 1 — Context of use |
| `ProductRequirements.md` | Phase 2 — Requirements |
| `04_Usability_Testing_Protocol.md` | Phase 4 — Evaluation *(planned)* |
| Wireframes *(pending)* | Phase 3 — Design solutions |
| `Personas_Final.md` *(pending)* | Phase 1 — Context of use *(post-field research)* |

---

## References

- ISO 9241-210:2019. *Ergonomics of human-system interaction — Part 210: Human-centred design for interactive systems*. International Organization for Standardization.
- Nielsen, J. (1994). *10 Usability Heuristics for User Interface Design*. Nielsen Norman Group.
- Courage, C., & Baxter, K. (2005). *Understanding Your Users: A Practical Guide to User Requirements Methods, Tools, and Techniques*. Morgan Kaufmann.
