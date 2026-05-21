# Tasks and Scenarios

## Usability Testing – CGRH Self-Service System
## UADY Benefits System

**Prepared by:** Héctor Barrera, Rodrigo Alonzo, Héctor Castro, Damián Villares

**Date:** April 2026

**Course:** Human-Computer Interaction — Faculty of Mathematics, UADY

**Semester:** January – June 2026

---

## 1. Overview

This document defines the tasks and scenarios used during the usability testing sessions for the CGRH Self-Service System. Each task is written as a realistic situation that a UADY employee would encounter in their daily or periodic work life — not as a set of navigation instructions.

This distinction is deliberate and methodologically critical. Telling a participant "click on the CFDI menu and then select the download button" would test their ability to follow instructions, not their ability to use the system. By framing each task as a real-world goal, the test reveals whether the system's structure, labels, and feedback are clear enough for users to find their own path.

Participants will receive one printed task card at a time. They will not see the next task until the current one is complete or abandoned. The moderator will not confirm whether the participant has completed a task correctly — the participant must judge this for themselves based on what the system shows them.

---

## 2. Pre-Task Setup

Before presenting any task to the participant, the moderator must verify the following:

- The prototype is open in the browser and showing the **login screen**
- A printed credential card is ready for Task 1 (test account username and password)
- The test account has sample data loaded: at least three CFDI receipts with dates, a Savings Fund balance, and a FAR balance
- The note-taker has a blank observation sheet for this participant
- Screen recording is active (if applicable)

Between tasks, the moderator or technical support member resets the prototype to the required starting state as specified in each task section below.

---

## 3. Tasks

---

### Task 1 — Login

**Starting state:** Login screen, no credentials entered.

**Credential card given to participant:**

> Usuario: `empleado.prueba@correo.uady.mx`
> Contraseña: `UADY2026`

---

**Scenario presented to the participant (read aloud and handed as printed card):**

> *"Tienes una cuenta en el sistema de la CGRH. Entra a tu cuenta usando los datos que te damos en esta tarjeta."*

---

**What we are observing:**

- Does the participant identify the username and password fields without hesitation?
- Do they enter the credentials correctly on the first attempt?
- If they make an error (e.g., wrong capitalization), does the system's error message help them understand what went wrong?
- How long does it take from reading the task to reaching the main menu?

**Related requirements:** RF03
**Related metrics:** NAV-01, NAV-02, NAV-04, APR-01, APR-03

**Task complete when:** Participant reaches the main menu screen.

---

### Task 2 — CFDI Download (Round 1)

**Starting state:** Main menu. Participant is logged in.

---

**Scenario presented to the participant (read aloud and handed as printed card):**

> *"Necesitas presentar tu recibo de nómina más reciente en una institución financiera. Encuéntralo y descárgalo."*

---

**What we are observing:**

- Does the participant recognize which section of the main menu corresponds to payroll receipts?
- Do they hesitate at the label "CFDI" — do they associate it with "recibo de nómina" without help?
- Can they identify the most recent receipt in the list?
- Do they find and use the download option without trying other buttons first?
- Do they know when the download was successful, or do they express uncertainty?

**Related requirements:** RF05, RF10
**Related metrics:** NAV-01, NAV-02, NAV-03, NAV-04, NAV-05, APR-01, APR-03

**Task complete when:** Participant has downloaded the PDF of the most recent receipt and acknowledges (verbally or by action) that the task is done.

---

### Task 3 — Savings Fund Consultation

**Starting state:** Main menu. Participant navigates back after Task 2, or moderator resets to main menu.

---

**Scenario presented to the participant (read aloud and handed as printed card):**

> *"Quieres saber cuánto tienes en tu Fondo de Ahorro antes de tomar una decisión económica. Consulta tu saldo."*

---

**What we are observing:**

- Does the participant identify the Savings Fund section from the main menu without confusion?
- Is the label "Fondo de Ahorro" immediately clear, or does the participant express doubt about whether this is the right section?
- Once inside, can they locate the balance figure without navigating further or clicking unnecessary elements?
- Do they express confidence that what they are seeing is their actual current balance?

**Related requirements:** RF05, RF30
**Related metrics:** NAV-01, NAV-02, NAV-03, NAV-04, NAV-05, APR-01

**Task complete when:** Participant reads or points to the Savings Fund balance on screen.

---

### Task 4 — Password Recovery

**Starting state:** Login screen. Moderator logs the participant out and clears any saved credentials before presenting this task.

---

**Scenario presented to the participant (read aloud and handed as printed card):**

> *"Imagina que olvidaste tu contraseña y no puedes entrar a tu cuenta. Desde esta pantalla, intenta recuperar el acceso."*

---

**What we are observing:**

- Does the participant find the password recovery option on the login screen without assistance?
- Is the recovery option visible and clearly labeled, or does the participant search for it?
- Does the participant understand each step of the recovery flow as it is presented?
- If the flow requires entering an email address, does the participant know which email to use?
- Does the system give sufficient feedback at each step so the participant knows what to do next?

**Note for the moderator:** This task evaluates the initiation and navigation of the recovery flow. Full completion (receiving and clicking an email link) may not be possible in the test environment. If the prototype simulates the confirmation screen, allow the participant to reach it. If not, end the task when the participant has successfully submitted their email and seen the confirmation message.

**Related requirements:** RF02
**Related metrics:** NAV-01, NAV-02, NAV-04, NAV-06, APR-01, APR-03

**Task complete when:** Participant reaches the confirmation screen that tells them a recovery email has been sent.

---

### Task 5 — Logout

**Starting state:** Participant is logged in, on any screen inside the system.

---

**Scenario presented to the participant (read aloud and handed as printed card):**

> *"Ya terminaste de usar el sistema por hoy. Cierra tu sesión."*

---

**What we are observing:**

- Does the participant find the logout option without assistance?
- Is the logout option visible enough, or does the participant have to search for it?
- Does the participant understand that they have successfully logged out based on what the system shows them after?
- Does the participant attempt to close the browser tab instead of logging out — indicating the logout option was not found?

**Related requirements:** RF04
**Related metrics:** NAV-01, NAV-02, NAV-04, APR-03

**Task complete when:** Participant reaches the logged-out state (login screen or confirmation message) through the system's logout function — not by closing the browser.

---

### Task 6 — CFDI Download (Round 2)

**Starting state:** Login screen. Participant logs in again using the credential card from Task 1.

---

**Scenario presented to the participant (read aloud and handed as printed card):**

> *"Ahora necesitas descargar el recibo de nómina del mes anterior, no el más reciente. Encuéntralo y descárgalo."*

---

**What we are observing:**

- Does the participant navigate to the CFDI section faster than in Task 2?
- Do they make fewer navigation errors compared to the first round?
- Can they distinguish between receipts by date and select the correct one (second most recent)?
- Is there a measurable improvement in time and errors between Round 1 and Round 2?

This task directly measures **APR-02 (improvement between attempts)** — the learnability metric that requires two rounds of the same type of task to detect whether the system is learnable or requires re-learning every time.

**Related requirements:** RF03, RF05, RF10
**Related metrics:** NAV-01, NAV-02, NAV-03, APR-01, APR-02

**Task complete when:** Participant downloads the PDF of the second most recent receipt.

---

## 4. Task Summary Table

| # | Task | Starting state | RF | Primary metrics | Expected duration |
|---|---|---|---|---|---|
| 1 | Login | Login screen | RF03 | NAV-01, NAV-02, APR-01 | ≤ 3 min |
| 2 | CFDI Download (Round 1) | Main menu | RF05, RF10 | NAV-01–05, APR-01 | ≤ 5 min |
| 3 | Savings Fund Consultation | Main menu | RF05, RF30 | NAV-01–05, APR-01 | ≤ 3 min |
| 4 | Password Recovery | Login screen | RF02 | NAV-01, NAV-04, NAV-06 | ≤ 4 min |
| 5 | Logout | Inside system | RF04 | NAV-01, NAV-02, APR-03 | ≤ 1 min |
| 6 | CFDI Download (Round 2) | Login screen | RF03, RF05, RF10 | APR-01, APR-02 | ≤ 3 min |

Total estimated task time: **15–19 minutes**
Total session time including introduction, SUS, and debrief: **45–55 minutes**

---

## 5. Moderator Guidelines

### 5.1 What the moderator must never do during a task

- Tell the participant where to click or what to look for
- Confirm or deny whether the participant has completed the task correctly
- React visibly (verbally or facially) to errors or hesitations
- Suggest that the participant is taking too long

### 5.2 Neutral prompts the moderator may use

If the participant has been silent for more than 20 seconds or appears completely stuck, the moderator may use one of the following neutral prompts. These are designed to keep the think-aloud active without giving directional help:

- *"¿Qué estás pensando en este momento?"*
- *"¿Qué esperarías que pasara si hicieras clic ahí?"*
- *"¿Qué harías si esto fuera tu propia computadora?"*
- *"Sigue intentando lo que te parezca más lógico."*

### 5.3 When to end a task early

A task should be marked as **abandoned** and ended if any of the following occur:

- The participant explicitly states they do not know how to continue and do not want to keep trying
- The participant has been on the same screen for more than 5 minutes with no forward progress
- The participant becomes visibly distressed or frustrated to the point where continuing would affect the quality of subsequent tasks

When ending a task early, the moderator should say:

> *"Está bien, vamos a pasar a la siguiente tarea. Esto nos ayuda a identificar qué partes del sistema necesitan mejorar."*

### 5.4 Between tasks

After each task — whether completed or abandoned — ask the participant:

> *"Antes de continuar, ¿hay algo que quieras comentar sobre lo que acabas de hacer o sobre lo que notaste?"*

Record any comments in the qualitative section of the observation sheet before resetting the prototype for the next task.

---

## 6. Print Checklist

The following materials must be printed before each session:

- [ ] Informed consent form (1 per participant)
- [ ] Credential card with test account username and password (1 per participant)
- [ ] Task cards — one card per task, printed separately so they can be handed one at a time (6 cards per session)
- [ ] Observation sheet (1 per participant)
- [ ] SUS questionnaire (1 per participant)
- [ ] Orientation and Learnability Likert scale (1 per participant)

---

## References

- Nielsen, J. (1994). *10 Usability Heuristics for User Interface Design*. Nielsen Norman Group.
- Carroll, J. M. (2000). *Making Use: Scenario-Based Design of Human-Computer Interactions*. MIT Press.
- Rubin, J., & Chisnell, D. (2008). *Handbook of Usability Testing: How to Plan, Design, and Conduct Effective Tests* (2nd ed.). Wiley.
