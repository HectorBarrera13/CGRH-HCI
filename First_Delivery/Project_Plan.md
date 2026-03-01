# Project Plan

## UADY Benefits System CGRH

**General Coordination of Human Resources (CGRH) – Universidad Autónoma de Yucatán**

**Course:** Human-Computer Interaction — Faculty of Mathematics, UADY  
**Semester:** January – June 2026

---

## 1. Research Plan

### 1.1 Required Information

The research process aims to collect the following types of information from the primary user segment (retired UADY employees, 60+):

| Information needed                                        | Purpose                                                                                |
| --------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Level of digital competence and technology usage habits   | Establish baseline for design decisions (typography, navigation depth, error handling) |
| Current process for accessing CFDI, FAR, and Savings Fund | Understand pain points of the existing email/in-person model                           |
| Barriers and frustrations with digital systems            | Identify the highest-friction points in the defined RFs                                |
| Password and credential management behaviors              | Inform the design of RF01, RF02, and RF03                                              |
| Expectations and trust factors regarding online systems   | Guide onboarding and security communication design                                     |
| Task performance data (time, errors, completion rate)     | Provide empirical evidence for usability problem prioritization                        |

---

### 1.2 Research Instruments

| Instrument                  | Type                                    | Target participants   | Document                            |
| --------------------------- | --------------------------------------- | --------------------- | ----------------------------------- |
| Interview Guide             | Qualitative — semi-structured           | 5–8 retired employees | `01_Interview_Guide.md`             |
| Contextual Inquiry Protocol | Qualitative — observation               | 3–5 retired employees | `02_Contextual_Inquiry_Protocol.md` |
| User Survey                 | Quantitative — structured questionnaire | 10+ retired employees | `03_User_Survey.md`                 |
| Usability Testing Protocol  | Mixed — task performance + SUS          | 5 retired employees   | `04_Usability_Testing_Protocol.md`  |

---

### 1.3 Analysis Method per Instrument

| Instrument         | Analysis type                                                                          | Output                                        |
| ------------------ | -------------------------------------------------------------------------------------- | --------------------------------------------- |
| Interviews         | Thematic coding — identify recurring patterns across responses                         | Affinity map, barrier list per RF             |
| Contextual Inquiry | Behavioral observation log — note errors, workarounds, and external support dependency | Friction point inventory                      |
| Survey             | Descriptive statistics — frequency, distribution, Likert scale averages                | Usage profile, feature prioritization ranking |
| Usability Testing  | Task metrics (completion rate, time, error count) + SUS score + Nielsen severity scale | Prioritized usability problem list            |

---

## 2. Activity Calendar

### 1st Delivery — Research Foundation and Requirements

| Activity                | Description                                                                                 | Responsible                                     | Resulting Artifacts                                                                                                   |
| ----------------------- | ------------------------------------------------------------------------------------------- | ----------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Research planning       | Define research objectives, select methods, and establish user profile                      | Héctor Barrera, Héctor Castro                   | `User_Research_Plan.md`, `User_Research_Activities.md`                                                                |
| Instrument design       | Create interview guide, contextual inquiry protocol, survey, and usability testing protocol | Rodrigo Alonzo, Damián Villares, Héctor Barrera | `01_Interview_Guide.md`, `02_Contextual_Inquiry_Protocol.md`, `03_User_Survey.md`, `04_Usability_Testing_Protocol.md` |
| User profiling          | Define primary and secondary user profiles; build proto-personas and scenarios              | Damián Villares, Héctor Castro                  | `User_Profiles_and_Personas.md`, `Scenarios.md`                                                                       |
| Requirements definition | Specify functional and non-functional requirements based on user profile and HCI principles | Héctor Barrera, Rodrigo Alonzo                  | `ProductRequirements.md`                                                                                              |
| Project definition      | Document social relevance, innovation, and feasibility                                      | Full team                                       | `Social_Relevance.md`, `Innovation_and_Differentiation.md`, `Feasibility.md`                                          |

---

### 2nd Delivery — Field Research and Design Solutions

| Activity            | Description                                                                                                 | Responsible                    | Resulting Artifacts                                 |
| ------------------- | ----------------------------------------------------------------------------------------------------------- | ------------------------------ | --------------------------------------------------- |
| Interviews          | Semi-structured interviews with retired employees; qualitative data collection on barriers and expectations | Héctor Castro                  | Interview notes per participant                     |
| Contextual Inquiry  | In-person observation of users interacting with the system or similar platforms in their real environment   | Rodrigo Alonzo                 | Observation log sheets                              |
| Surveys             | Application and consolidation of structured questionnaires with a broader participant group                 | Damián Villares, Héctor Castro | Completed survey forms, raw data                    |
| Results analysis    | Cross-method pattern identification; problem prioritization using Nielsen severity scale                    | Full team                      | Prioritized usability problem list, insights per RF |
| Personas refinement | Update proto-personas and scenarios based on field evidence                                                 | Damián Villares, Héctor Castro | `Personas_Final.md`                                 |
| Wireframes          | Low and medium fidelity wireframes for critical flows (RF01, RF02, RF03, RF05)                              | Rodrigo Alonzo, Héctor Barrera | Wireframe files                                     |

---

### 3rd Delivery — Evaluation and Iteration

| Activity             | Description                                                                        | Responsible                    | Resulting Artifacts                 |
| -------------------- | ---------------------------------------------------------------------------------- | ------------------------------ | ----------------------------------- |
| Usability testing    | Task-based sessions with retired employees using defined protocol; SUS application | Héctor Barrera, Rodrigo Alonzo | Task log sheets, SUS questionnaires |
| Findings analysis    | Classify problems by Nielsen severity scale; identify critical issues              | Full team                      | Severity-ranked problem list        |
| Heuristic evaluation | Team evaluation against Nielsen's 10 heuristics                                    | Full team                      | Heuristic evaluation report         |
| Prototype iteration  | Address critical and high-severity findings in the prototype                       | Rodrigo Alonzo, Héctor Barrera | Updated prototype                   |
| Final documentation  | Repository organization, traceability review, and final report                     | Héctor Barrera, Rodrigo Alonzo | Final report, organized repository  |

---

## 3. Team Roles and Responsibilities

| Member          | Primary Role             | Responsibilities                                                             |
| --------------- | ------------------------ | ---------------------------------------------------------------------------- |
| Héctor Barrera  | HCI Lead & Documentation | Research planning, instrument design, usability testing, final documentation |
| Héctor Castro   | User Researcher          | Interview execution, survey application, results analysis, user modeling     |
| Rodrigo Alonzo  | UX Designer              | Instrument design, contextual inquiry, usability testing, documentation      |
| Damián Villares | UX Researcher & Modeler  | Contextual inquiry, survey application, personas and scenarios               |

> All members participate in analysis sessions and repository documentation. Role assignments reflect primary ownership, not exclusive contribution.

---

## 4. Contribution Metrics

Quantifiable individual contribution evidence is tracked through:

- **GitHub commits:** Each member commits their own deliverables under their name
- **Document authorship:** Every file includes a `Prepared by` field
- **Individual reflections:** Each member writes a reflection per activity they led
- **Peer feedback:** Team members provide feedback on each other's contributions in bi-weekly review sessions
