# Justification of Selected Usability Attributes
**User Research – CGRH System UADY**  
Analysis date: 03/20/2026

---

## Context

Based on the qualitative analysis of 6 interviews conducted with teaching and administrative staff at UADY, 8 groups of findings were identified in the affinity diagram. Of those 8, **4 critical attributes** were selected as they concentrate the highest risks of abandonment, error, and distrust in the system. These attributes are not the only relevant ones, but they are the ones that, if not addressed through design, could compromise the adoption of the system entirely.

---

## Attribute 1: Ease of Navigation

**Why we selected it**

This is the most frequently mentioned pain point across all interviews. Five out of six users expressed — directly or indirectly — that complex or unintuitive navigation frustrates them and leads them to abandon the task.

The target user profile engages with digital platforms occasionally and does not have consolidated experience with web conventions. When the structure of a page is unclear, the user does not look for an alternative solution within the system: they simply stop.

> *"The navigation; sometimes she can't find what she's looking for."* — E1  
> *"Too many steps; she prefers it to be simple."* — E3  
> *"Navigation changes a lot from one page to another."* — E6

Additionally, since system use will be infrequent (biweekly for payroll, every 6 months for the Savings Fund), each session may feel like the first time. If the navigation is not immediately understandable, the user will lose both time and confidence.

**Design implication:** minimize the number of steps required to access documents or complete a procedure. Maintain a predictable structure with clear labels and no deep menus.

---

## Attribute 2: Error Handling and Prevention

**Why we selected it**

The dominant response to any error or unexpected situation is to escalate to another person — a colleague, a family member, or the support team. Only two users (E3 and E4) attempt to resolve the problem on their own before escalating. E5, the youngest participant, would simply abandon the task.

This means the system cannot rely on users knowing what to do when something goes wrong. If an ambiguous error message appears, or if a flow does not respond as expected, the most likely outcome is that the user leaves the system and does not return on their own.

> *"He would leave it."* — E5, if something does not go as expected  
> *"She would ask for help."* — E1, E2, when facing any error  
> *"Call someone."* — E6

**Design implication:** prevent errors before they occur through real-time validations and confirmation prompts before irreversible actions. When an error does occur, the message must explain what happened and what the user can do next — not just display a code or a generic alert.

---

## Attribute 3: System Status Visibility

**Why we selected it**

100% of participants expect to receive an explicit confirmation after completing a procedure. No user trusts that an action worked unless there is a visible signal indicating so. The preferred confirmation channel is email, which is already part of their daily workflow.

This finding is unanimous and has no exceptions. The absence of feedback would not just cause discomfort — it would generate active distrust, potentially leading users to repeat the procedure or visit the offices in person to verify.

> *"Some notification or email saying 'procedure in progress'."* — E1  
> *"She needs a receipt confirming the action was completed."* — E4  
> *"Expects them to send a confirmation email."* — E5, E6

**Design implication:** confirm every relevant action at two moments: immediately on screen (a visible success message) and subsequently by email (a channel already familiar and trusted by the user).

---

## Attribute 4: Memorability

**Why we selected it**

Unlike a daily-use application, the CGRH system will be used infrequently: payroll receipts arrive biweekly and the Savings Fund is checked every 6 months. This makes memorability a critical attribute — users do not have the opportunity to "practice" until they become proficient.

Two users (E1 and E2) already anticipate having difficulty remembering how to use the system after a period of inactivity. E4, who uses digital platforms more regularly, explicitly mentions that she forgets how to use pages she visits infrequently.

> *"It depends; if the navigation is easy, yes — if it has too many steps, she can get lost."* — E1  
> *"She would have to write down how to use it."* — E2  
> *"She finds it difficult that she forgets how to use them."* — E4

**Design implication:** the system must be resumable without requiring users to remember specific steps from their previous session. Descriptive labels, recognizable icons, and short flows reduce cognitive load and the need to relearn the interface.

---

## Relationship Between the 4 Attributes

The four attributes are not independent — they reinforce each other. Simple navigation reduces the likelihood of errors. Well-handled errors do not interrupt the flow. A flow that users can easily remember reduces their reliance on external help. And visible confirmation at the end of each task closes the loop with confidence.

Designing these four points well does not guarantee a perfect system, but it does minimize the most likely causes of abandonment identified in the research.

---

## Attributes Deprioritized in This Iteration

The following attributes are relevant but are considered secondary at this stage, either because they affect a minority of users or because they can be addressed through more localized design decisions:

| Attribute | Reason for deprioritizing now |
|---|---|
| Visual accessibility | Important, but addressable through style guidelines (font size, contrast). Does not affect the flow architecture. |
| Perceived trust and security | Most users feel secure with a username and password. The shared-PC risk (E5) can be resolved with automatic session timeout. |
| Learnability | Largely resolved if navigation and memorability are well designed. |
| Resistance to change | Not a direct UX design problem; depends on institutional communication and the system's perceived value proposition. |
