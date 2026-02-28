# Usability Testing Protocol
## Activity 4: Usability Testing — CGRH UADY

**Prepared by:** Héctor Barrera  
**Date:** February 27, 2026  
**Target profile:** Retired UADY employees, over 60 years of age

---

## 1. Evaluation Objectives

The usability tests aim to evaluate the ease of use of the CGRH system with representative users of the defined primary profile (retirees over 60 years of age with basic digital literacy). The specific objectives are:

- Identify the most frequent errors during the execution of critical tasks (registration, login, password recovery, information consultation).
- Measure the average time required to complete each task without assistance.
- Detect comprehension problems in labels, error messages, and navigation flows.
- Obtain empirical evidence to justify design decisions for requirements RF01–RF30.
- Validate or refute assumptions established in the proto-personas (Armando, Concepción, Feliciano).

| Field | Detail |
|---|---|
| **Duration per session** | 20 – 35 minutes |
| **Modality** | In-person (at participant's home or an enabled room) |
| **Participant profile** | Retired UADY employee, 60+ years, basic digital literacy |
| **Number of participants** | 5 participants (minimum viable to detect 85% of usability problems, Nielsen 1993) |
| **Roles** | 1 facilitator + 1 observer/note-taker |
| **Required materials** | Prototype on desktop computer, task cards, log sheet, pencil |
| **Success criterion per task** | Completed without assistance within the established time limit |

---

## 2. Evaluation Tasks

Each task is presented to the participant on a printed card with simple language and no technical terminology. The facilitator **does not give instructions** on how to perform the task; they only describe the objective.

| # | Task | Scenario presented to the user *(in Spanish)* | Time limit | RF |
|---|---|---|:---:|---|
| T1 | System registration | *"Imagine que va a entrar al sistema de la CGRH por primera vez. Por favor, cree una cuenta nueva."* | 8 min | RF01 |
| T2 | Login | *"Ya tiene una cuenta. Por favor, entre al sistema con su usuario y contraseña."* | 3 min | RF03 |
| T3 | Password recovery | *"Olvidó su contraseña. Por favor, intente recuperarla para poder entrar."* | 5 min | RF02 |
| T4 | CFDI consultation | *"Necesita su recibo de nómina del mes pasado para entregarlo en el banco. Búsquelo y descárguelo."* | 5 min | RF10 |
| T5 | FAR consultation | *"Quiere saber cuánto tiene en su Fondo de Ahorro para el Retiro. Búsquelo."* | 4 min | RF20 |
| T6 | Savings Fund consultation | *"Quiere ver el saldo de su Caja de Ahorro. Encuéntrelo en el sistema."* | 4 min | RF30 |
| T7 | Logout | *"Ya terminó lo que necesitaba. Por favor, salga del sistema."* | 2 min | RF04 |

---

## 3. Facilitator Script

### 3.1 Introduction (5 min)

**Suggested opening** *(in Spanish — for participant):*

> *"Buenos días/tardes. Gracias por venir. Hoy vamos a probar una página de internet que está en desarrollo. Quiero aclarar que no estamos evaluando cómo usa usted la computadora: estamos evaluando si la página está bien diseñada. Si algo no le queda claro o no sabe qué hacer, eso nos dice que hay algo que mejorar en el diseño. Le pediré que piense en voz alta mientras trabaja: que me diga qué ve, qué espera que pase, y qué le confunde. ¿Tiene alguna pregunta antes de comenzar?"*

### 3.2 Rules during the session

- Do not give hints, suggestions, or confirm whether the user is doing the right thing.
- If the user asks "Am I doing this right?", respond *(in Spanish)*: *"Haga lo que le parezca natural."*
- If the user is stuck for more than 2 minutes, log the task abandonment and move to the next one.
- If the user expresses intense frustration, briefly acknowledge it *(in Spanish)*: *"Entiendo, está bien, eso es justo lo que queremos identificar."*
- Maintain a neutral and calm tone throughout the session.

### 3.3 Closing (10 min)

After all tasks are completed, ask the following questions *(in Spanish)*:

1. *En general, ¿cómo describiría su experiencia con el sistema?*
2. *¿Hubo alguna parte que le resultara muy confusa o frustrante?*
3. *¿Hay algo que el sistema haga especialmente bien?*
4. *Si pudiera cambiar una sola cosa, ¿qué sería?*
5. *¿Usaría este sistema de manera regular si estuviera disponible?*

---

## 4. Usability Metrics

| Metric | Definition | Recording method |
|---|---|---|
| **Completion rate** | % of participants who complete the task without assistance | Log sheet: Completed / Not completed / Abandoned |
| **Time on task** | Time elapsed from when the task is presented until the user considers it done | Stopwatch; record in seconds |
| **Number of errors** | Incorrect clicks, backward navigation, repetition of steps | Observer records in real time |
| **Help requests** | Number of times the user asks the facilitator how to proceed | Count per task |
| **SUS score** | System Usability Scale: 10 items on a 1–5 Likert scale | Post-session questionnaire (see Section 6) |
| **Qualitative issues** | Verbalizations of confusion, comprehension errors, emotional reactions | Observer's text notes |

---

## 5. Task Log Sheet

*Complete one row per task. Use one sheet per participant.*

| Task | Status | Time (sec) | # Errors | # Help requests | Observations |
|:---:|---|:---:|:---:|:---:|---|
| T1 | ☐ Completed ☐ Not completed ☐ Abandoned | | | | |
| T2 | ☐ Completed ☐ Not completed ☐ Abandoned | | | | |
| T3 | ☐ Completed ☐ Not completed ☐ Abandoned | | | | |
| T4 | ☐ Completed ☐ Not completed ☐ Abandoned | | | | |
| T5 | ☐ Completed ☐ Not completed ☐ Abandoned | | | | |
| T6 | ☐ Completed ☐ Not completed ☐ Abandoned | | | | |
| T7 | ☐ Completed ☐ Not completed ☐ Abandoned | | | | |

---

## 6. SUS Questionnaire (System Usability Scale)

**Instructions for participant** *(in Spanish)*:

> *"A continuación hay 10 afirmaciones sobre el sistema. Por favor indique qué tan de acuerdo está con cada una."*
>
> *1 = Totalmente en desacuerdo — 5 = Totalmente de acuerdo*

| # | Afirmación | 1 | 2 | 3 | 4 | 5 |
|:---:|---|:---:|:---:|:---:|:---:|:---:|
| 1 | Creo que me gustaría usar este sistema con frecuencia | ☐ | ☐ | ☐ | ☐ | ☐ |
| 2 | Encontré el sistema innecesariamente complejo | ☐ | ☐ | ☐ | ☐ | ☐ |
| 3 | Pensé que el sistema era fácil de usar | ☐ | ☐ | ☐ | ☐ | ☐ |
| 4 | Creo que necesitaría el apoyo de alguien para poder usar este sistema | ☐ | ☐ | ☐ | ☐ | ☐ |
| 5 | Las diferentes partes del sistema estaban bien integradas | ☐ | ☐ | ☐ | ☐ | ☐ |
| 6 | Había demasiadas inconsistencias en el sistema | ☐ | ☐ | ☐ | ☐ | ☐ |
| 7 | Imagino que la mayoría de personas aprendería a usar este sistema muy rápidamente | ☐ | ☐ | ☐ | ☐ | ☐ |
| 8 | El sistema fue muy difícil de manejar | ☐ | ☐ | ☐ | ☐ | ☐ |
| 9 | Me sentí muy seguro/a usando el sistema | ☐ | ☐ | ☐ | ☐ | ☐ |
| 10 | Necesité aprender muchas cosas antes de poder empezar a usar el sistema | ☐ | ☐ | ☐ | ☐ | ☐ |

---

## 7. Finding Prioritization Criteria

Problems identified during testing will be classified according to Nielsen's (1993) severity scale:

| Level | Severity | Criterion |
|---|---|---|
| **4 – Critical** | Catastrophic | The user cannot complete the task; causes immediate system abandonment |
| **3 – High** | Major | The user completes the task with significant difficulty or requires assistance |
| **2 – Medium** | Minor | Causes notable confusion or delay but the user reaches the goal |
| **1 – Low** | Cosmetic | Minor annoyance; does not prevent task completion |
| **0 – No impact** | Not a problem | Observed but with no effect on the user experience |
