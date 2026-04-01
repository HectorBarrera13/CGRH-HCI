# Justification of Selected Usability Attributes
**User Research – CGRH System UADY**  
Analysis date: 03/20/2026

---

## Context

Based on the qualitative analysis of 6 interviews conducted with teaching and administrative staff at UADY, 8 groups of findings were identified in the affinity diagram. Of those 8, **2 critical attributes** were selected as they concentrate the highest risks of abandonment and distrust in the system. Rather than treating each finding in isolation, related patterns were merged into broader attributes that address the same underlying user need. These are the two areas that, if not addressed through design, could compromise adoption of the system entirely.

---

## Attribute 1: Intuitive Navigation

**Why we selected it**

Navigation difficulty was the most frequently mentioned pain point across all interviews — five out of six users expressed that complex or inconsistent navigation leads them to abandon tasks. But the issue goes beyond a single session: the CGRH system will be used infrequently, with payroll receipts checked biweekly and the Savings Fund consulted only every 6 months. This means that every time a user returns to the system, they may feel like they are using it for the first time.

A system can be simple to learn the first time but still require re-learning after months of inactivity. For the CGRH system to succeed, it must be intuitive enough that users can pick it up again without needing to remember specific steps or ask for help.

> *"The navigation; sometimes she can't find what she's looking for."* — E1  
> *"Too many steps; she prefers it to be simple."* — E3  
> *"It depends; if the navigation is easy, yes — if it has too many steps, she can get lost."* — E1  
> *"She would have to write down how to use it."* — E2  
> *"Navigation changes a lot from one page to another."* — E6

**Design implication:** minimize the number of steps required to reach any document or complete any procedure. Use clear, descriptive labels and recognizable patterns so that a user returning after 6 months can orient themselves immediately — without a tutorial, without assistance, and without having to remember where things were last time.

---

## Attribute 2: Error Prevention

**Why we selected it**

When something goes wrong — or even when something goes right — the CGRH user does not act without a clear signal from the system. These two behaviors are two sides of the same problem: users cannot recover from errors on their own, and users do not trust that a completed action worked unless the system tells them so explicitly.

On the error side, the dominant response across participants was to stop, ask someone for help, or abandon the task entirely. Only two users (E3 and E4) attempt to resolve issues independently. E5, the youngest participant, stated he would simply leave the task unfinished. This means the system must prevent errors before they happen — it cannot rely on users troubleshooting on their own.

On the feedback side, all 6 participants expect an explicit confirmation after any completed procedure. Without it, they distrust the result and may repeat the action or go to the offices in person to verify. The preferred confirmation channel is email, which is already embedded in their daily workflow.

> *"He would leave it."* — E5, if something does not go as expected  
> *"She would ask for help."* — E1, E2, when facing any error  
> *"Some notification or email saying 'procedure in progress'."* — E1  
> *"She needs a receipt confirming the action was completed."* — E4  
> *"Expects them to send a confirmation email."* — E5, E6

**Design implication:** prevent errors proactively through real-time validation and confirmation prompts before irreversible actions. When an error does occur, the message must explain what happened and what the user should do next. Every completed action must produce a visible on-screen confirmation and a follow-up email — both signals are necessary for the user to trust the system.

---

## How the Two Attributes Connect

These two attributes are not independent. A clear, predictable navigation reduces the likelihood of errors occurring in the first place. And a system that communicates its state reliably — whether through error messages or success confirmations — makes users more willing to return and try again, reinforcing the memorability of the experience over time.

Addressing both attributes consistently across the system is the minimum threshold for the CGRH platform to be trusted and adopted by its target users.

---

## Deprioritized Attributes

The following attributes were identified in the research but are not prioritized in this design phase, either because they can be resolved through localized decisions or because they depend on factors outside the scope of interface design:

| Attribute | Reason for deprioritizing |
|---|---|
| Visual accessibility | Addressable through style guidelines (font size, contrast, touch targets). Does not affect flow architecture. |
| Perceived trust and security | Most users feel secure with a username and password. The shared-PC risk (E5) can be resolved with automatic session timeout. |
| Resistance to change | Depends on institutional communication and the system's perceived value — not a UX design problem directly. |
