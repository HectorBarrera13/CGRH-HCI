# User Profiles

## Usability Testing – CGRH Self-Service System
## UADY Benefits System

**Prepared by:** Héctor Barrera, Rodrigo Alonzo, Héctor Castro, Damián Villares

**Date:** April 2026

**Course:** Human-Computer Interaction — Faculty of Mathematics, UADY

**Semester:** January – June 2026

---

## 1. Overview

This document defines the user profiles that will participate in the usability testing sessions for the CGRH Self-Service System. These profiles are grounded in the qualitative data collected during six semi-structured interviews conducted on March 20, 2026, and are represented by the proto-personas developed during the second delivery of this project.

The original research plan targeted retired UADY employees over 60 years of age. Due to access constraints during the field research phase, the study was redirected to **active UADY employees** from two staff groups: **administrative personnel** (Personal Administrativo) and **manual workers** (Personal de Manuales). Both groups interact with the CGRH system as primary beneficiaries of the payroll and savings fund information it provides.

Usability testing participants must be recruited from these same two groups to maintain consistency with the research findings and ensure that results are applicable to the population the system is designed to serve.

---

## 2. Staff Group 1 — Administrative Personnel (Personal Administrativo)

### 2.1 Group Description

Administrative personnel are UADY employees whose primary role involves office-based tasks: academic coordination, school control, institutional secretarial work, and similar functions. They work regular hours at university facilities and have consistent access to institutional computers and stable internet connections. Their daily work routinely involves digital tools — email, document platforms, Excel — making them the more digitally active of the two groups tested.

This group currently receives payroll receipts (CFDI) by email every two weeks and consults the Savings Fund only when the biannual email arrives. They have rarely, if ever, needed to visit the CGRH offices in person.

### 2.2 Profile Attributes

| Attribute | Description |
|---|---|
| **Employment type** | Administrative staff (secretarial, coordination, school control) |
| **Age range** | 35–55 years |
| **Primary device** | Desktop or laptop computer at the workplace |
| **Secondary device** | Android smartphone for personal use |
| **Connectivity** | Stable internet at the workplace; home internet available |
| **Digital competence** | Medium to medium-high — daily use of email, office tools, and web platforms |
| **CGRH interaction** | Receives CFDI by email; consults Savings Fund reactively when notified |
| **In-person CGRH visits** | Rare; only when a specific payroll issue requires it |
| **Password management** | Device auto-save or cell phone; rarely written down manually |
| **Institutional email** | Used daily without issues |

### 2.3 Key Behavioral Patterns from Research

- **Conformity with current flow.** Participants in this group expressed satisfaction with the current email-based process. Adoption of the new system depends on it being at least as fast and simple as receiving an email. If the system adds friction, they will revert to the known channel.
- **Moderate error tolerance.** Some participants in this group (E3, E4) attempt to resolve problems independently before asking for help. However, if a problem persists, they escalate to a colleague or look for help online. They do not formally report issues unless the problem is significant.
- **Navigation as the primary pain point.** Inconsistency between web platforms was specifically mentioned by participants in this group (E6). They expect a predictable interface where learned behavior transfers across sections.
- **Explicit confirmation required.** All participants expect an on-screen or email confirmation after completing any action. Without it, they distrust the result.
- **Infrequent use affects retention.** Even within this more digitally active group, one participant (E4) explicitly stated she forgets how to use platforms she visits infrequently. This confirms that memorability is a relevant concern even for users with medium-to-high digital competence.

### 2.4 Representative Personas

This group is represented by two proto-personas developed during the second delivery:

**Carlos Pech May — 42 years old**
Administrative assistant at the School Control Department. Uses institutional systems, email, and Excel daily. Values efficiency and consistency. Frustrated by interface changes that break established habits and by error messages that do not explain what went wrong. Primary concern: the system must work reliably and predictably every time.

**María del Carmen Uc Pool — 36 years old**
Academic secretary at UADY. Medium-high digital competence. Uses office tools and web systems daily. Relies on clear system feedback to confirm that her actions were processed. Often assists colleagues who struggle with digital platforms. Primary concern: the system must clearly confirm each completed action and minimize the number of steps required.

### 2.5 Recruitment Criteria for Testing

Participants recruited for this profile must meet all of the following:

- Active UADY employee in an administrative role (academic coordination, school control, secretarial, or equivalent)
- Regular daily use of a computer at the workplace
- Receives CFDI payroll receipts by institutional email
- No prior experience using the CGRH self-service prototype
- Willing to participate and sign the informed consent form

---

## 3. Staff Group 2 — Manual Workers (Personal de Manuales)

### 3.1 Group Description

Manual workers are UADY employees whose role involves physical or operational tasks: maintenance, janitorial services, facilities management, and related functions. They do not have a personal computer assigned at work — they may share one terminal at their installation or use their smartphones as their primary device. Their internet connectivity is more limited and inconsistent than the administrative group, and their exposure to formal institutional digital platforms is lower.

This group also receives payroll receipts by email and consults the Savings Fund reactively, but their relationship with digital platforms is more fragile. They are more likely to abandon a task at the first sign of difficulty and less likely to have someone nearby who can help them navigate a web system.

### 3.2 Profile Attributes

| Attribute | Description |
|---|---|
| **Employment type** | Maintenance, janitorial, facilities, and general services staff |
| **Age range** | 29–50 years |
| **Primary device** | Android smartphone (low-to-mid range) |
| **Secondary device** | Shared computer at the workplace installation (not personal) |
| **Connectivity** | Mobile data (limited); no guaranteed home internet; inconsistent signal in some campus buildings |
| **Digital competence** | Basic — uses messaging apps and social media; limited experience with formal web platforms |
| **CGRH interaction** | Receives CFDI by email; consults Savings Fund reactively when notified |
| **In-person CGRH visits** | Rare, but more likely than the administrative group when a problem arises |
| **Password management** | Auto-save on device; does not memorize or write down passwords |
| **Institutional email** | Has access; checks it when notifications arrive, not daily |

### 3.3 Key Behavioral Patterns from Research

- **Abandonment as the default error response.** The participant from this group (E5) stated directly that if something does not go as expected, he would simply leave the task. This is the highest-risk behavior for system adoption — the system must prevent errors proactively because this user will not attempt recovery on his own.
- **Shared computer security concern.** E5 raised a concrete concern about sessions remaining open on shared computers at the installation. This is a real risk for this group and directly motivates the inclusion of the logout task (RF04) and the requirement for automatic session timeout.
- **Tutorial dependency.** E5 stated he would feel more confident using the system if a tutorial or guided walkthrough were provided for the first use. Unlike the administrative group, this profile is less likely to explore independently.
- **Mobile-first mental model.** This group's primary device is a smartphone. While the test will be conducted on desktop (consistent with the system's design scope), the moderator should note any moments where participants reference phone-based interaction patterns or seem unfamiliar with desktop conventions.
- **Connectivity limitations.** E5 noted that internet signal is unreliable in some parts of campus and that WhatsApp messages sometimes fail to arrive due to limited mobile data. This is outside the scope of the interface design but relevant to understanding the real usage environment.

### 3.4 Representative Persona

This group is represented by one proto-persona developed during the second delivery:

**José Luis Chan Ek — 29 years old**
Maintenance staff at UADY. Basic digital competence — uses social media and messaging apps but has minimal experience with formal web systems. Relies primarily on his smartphone. Wants to complete tasks quickly without needing a computer. If a task is not immediately straightforward, he prefers to ask someone rather than explore on his own. Primary concern: the system must be simple enough to complete without help, or he will not use it.

### 3.5 Recruitment Criteria for Testing

Participants recruited for this profile must meet all of the following:

- Active UADY employee in a manual or operational role (maintenance, janitorial, facilities, or equivalent)
- Primary personal device is a smartphone; limited or shared access to a computer
- Receives CFDI payroll receipts by institutional email
- No prior experience using the CGRH self-service prototype
- Willing to participate and sign the informed consent form

---

## 4. Participant Composition for Testing Sessions

A total of **5 participants** will be recruited across both groups. This number is consistent with Nielsen's (2000) finding that five users are sufficient to uncover approximately 85% of usability problems in a system.

The recommended composition is:

| Group | Number of participants |
|---|---|
| Administrative personnel (Personal Administrativo) | 3 |
| Manual workers (Personal de Manuales) | 2 |

The administrative group receives three slots because it represents a broader range of digital competence within the medium-to-medium-high spectrum and is more likely to surface nuanced navigation issues. The manual workers group receives two slots because even one participant from this profile generates high-signal observations given the gap between their digital competence and the demands of a web platform.

If access allows, a sixth participant can be added from either group, prioritizing whichever profile produced the most unresolved issues in the first five sessions.

---

## 5. Exclusion Criteria

The following participants should not be included in the testing sessions, regardless of their staff group:

- Team members or colleagues who have been involved in the design, development, or review of the CGRH prototype at any stage
- Participants who have used or previewed the prototype before the session
- Participants who work in IT, systems, or software development roles at UADY, as their technical background would not be representative of the target population
- Participants under 25 or over 60 years of age, as these fall outside the active employee profile targeted in this phase

---

## 6. Differences Between Groups Relevant to Test Moderation

The two groups present meaningfully different interaction patterns that the moderator should account for during sessions:

| Dimension | Administrative personnel | Manual workers |
|---|---|---|
| Error response | Attempts recovery; escalates if needed | Abandons or waits for help |
| Navigation exploration | Moderate — will explore before asking | Low — prefers guided steps |
| Desktop familiarity | High — daily workplace use | Low — primary device is smartphone |
| Tolerance for multi-step flows | Moderate | Low |
| Verbalization during think-aloud | More natural; used to explaining processes | May require more prompting from moderator |

The moderator should apply the same script and neutral prompts across both groups, but should be aware that participants from the manual workers group may require more frequent use of the neutral prompt *"What are you thinking right now?"* to keep the think-aloud active, as they are less likely to verbalize their process spontaneously.

---

## References

- Nielsen, J. (2000). *Why You Only Need to Test with 5 Users*. Nielsen Norman Group.
- Cooper, A., Reimann, R., & Cronin, D. (2004). *About Face 3: The Essentials of Interaction Design*. Wiley.
- INEGI. (2023). *Encuesta Nacional sobre Disponibilidad y Uso de Tecnologías de la Información en los Hogares (ENDUTIH 2023)*. Instituto Nacional de Estadística y Geografía.
- Fisk, A. D., Rogers, W. A., Charness, N., Czaja, S. J., & Sharit, J. (2018). *Designing for Older Adults: Principles and Creative Human Factors Approaches* (3rd ed.). CRC Press.
