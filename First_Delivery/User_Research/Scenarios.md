# Use Scenarios

## CGRH System – UADY

**Prepared by:** Damián Villares, Héctor Castro  
**Date:** February 27, 2026

> **Methodological note:** The scenarios presented here are **preliminary design scenarios**, derived from the analysis of functional requirements (RF01–RF30), the defined user profile, and secondary sources on the digital behavior of older adults. Their purpose is to guide design decisions and serve as a basis for creating requirements — not as an outcome of field sessions. They will be adjusted and enriched once primary research (interviews, contextual inquiry, usability testing) provides direct evidence of user behavior.

---

## Scenario 1 — CFDI Download for a Banking Procedure

**Persona:** Armando Cetina Pech, 67 years old, retired faculty  
**Context:** Morning at home, sitting in front of his desktop computer  
**Related requirements:** RF03 (Login), RF10 (CFDI Inquiry)

---

Armando needs to present his last three payroll receipts to a financial institution to apply for a loan. His nephew mentioned that he can now download them directly from the CGRH system without going to the university.

He opens the browser on his desktop and types the address his nephew wrote down for him on paper. He reaches the login screen. He enters his username — written on a note stuck to his monitor — and types his password, trying to remember whether he used capital letters or not. The system tells him the password is incorrect. Armando tries a second time with another variation he recalls. The second attempt fails as well.

He spots a link that says **"Forgot your password?"** and clicks it. The system asks for his institutional email. Armando doesn't know it by heart; he searches his notes and finds it. He types it in, clicks continue, and the system tells him he will receive an email with instructions.

Armando opens his email client and waits. After a few minutes he finds the message in his spam folder. He follows the link, sets a new password, and returns to the login screen. This time he logs in successfully.

From the main menu, he identifies the **"My CFDIs"** option. The system displays a list of receipts sorted by date. Armando selects the three most recent ones and downloads each as a PDF by clicking the corresponding button. The files are saved in his downloads folder. He logs out.

**Identified friction points:**
- Remembering or locating access credentials
- Finding the recovery email in the spam folder
- Associating the acronym "CFDI" with "payroll receipt"

**Derived design criteria:**
- RF02 must include an explicit instruction to check the spam/junk folder
- RF10 must display receipts with the label "Payroll Receipt (CFDI)" rather than the acronym alone
- The PDF download button must be the most prominent element in each record

---

## Scenario 2 — Unassisted Password Recovery

**Persona:** Concepción Dzul Rosado, 63 years old, retired administrative employee  
**Context:** Afternoon at home, using her daughter's laptop while she is at work  
**Related requirements:** RF02 (Password Recovery), RF03 (Login)

---

Concepción wants to check her Savings Fund balance before a family gathering this weekend. Her daughter left her the laptop before heading to work. Concepción remembers she already has an account in the system but cannot recall the password; the last time she logged in was four months ago.

She accesses the platform and on the login screen types what she believes is her username. The system doesn't recognize it: she's unsure whether her username is her employee number, her name, or her email. She tries three variations she can think of and none of them work.

She finds the recovery link. The system asks for her institutional email. Concepción isn't sure which one it is, but remembers it ended in `@correo.uady.mx`. She types it and clicks. The system confirms that an email has been sent.

Concepción opens the email on her daughter's phone — where she does know how to access it — and finds the message. She follows the link from the phone, sets a new password using one she already has memorized from another account, and returns to the laptop to log in with the new credentials.

The system takes her to the main menu. She finds the **Savings Fund** section, locates her current balance, and takes a photo of the screen with her phone to keep it as a reference.

**Identified friction points:**
- Ambiguity about which field to use as "username"
- Recovery flow that crosses devices (laptop → phone → laptop)
- Doesn't know how to "save" the information; photographs the screen as a workaround

**Derived design criteria:**
- RF03 must explicitly indicate below the username field what format is expected (e.g., "Enter your employee number or institutional email")
- RF02 must display a clear and concise confirmation screen, without assuming the user knows how to check email on the same device
- RF30 must offer a PDF download option as an alternative information-capture mechanism to photographing the screen

---

## Scenario 3 — First-Time Assisted Registration

**Persona:** Feliciano Canul Tzuc, 69 years old, retired facilities staff  
**Context:** Afternoon at a neighbor's house, using his computer; the neighbor acts as guide throughout the process  
**Related requirements:** RF01 (Registration), RF03 (Login), RF10 (CFDI Inquiry)

---

Feliciano needs to present a payroll receipt to the IMSS for a supplementary pension procedure. A relative explained that he can download it from the CGRH system without going to the university, but that he first needs to register.

He goes to his neighbor Ernesto's house, who has a computer and internet access. Ernesto opens the system in the browser. The home screen shows options to log in or register. Feliciano doesn't have an account, so Ernesto helps him find the registration button.

The registration form displays several fields: employee ID, RFC, CURP, institutional email, and email confirmation. Feliciano takes out his former-employee ID card from his wallet, where his employee number is written. His RFC and CURP are written on a folded piece of paper he carries with him. He reads them aloud and Ernesto types them in.

When they reach the institutional email field, Feliciano doesn't remember what it is. Ernesto suggests calling the CGRH to ask. After a brief phone call, they get the email and type it in. The system prompts them to create a password; Ernesto suggests a simple combination based on Feliciano's date of birth and writes it down on paper for Feliciano to keep.

The system displays a message saying a confirmation link has been sent to the email. Ernesto opens the institutional email from the same computer, finds the message, and clicks the link. Feliciano's account is now active.

They log in with the newly created credentials. The main menu appears with three options. Ernesto reads aloud: "My CFDIs, Retirement Savings Fund, Savings Fund." Feliciano recognizes the first option. Ernesto clicks it, the list of most recent receipts appears, and he downloads the PDF for the month required by the IMSS. They print it at the copy shop on the way home.

**Identified friction points:**
- The entire process required full third-party assistance; Feliciano was unable to operate the computer on his own
- Multiple data fields the user doesn't have memorized or digitized (RFC, CURP, email)
- The email confirmation flow assumes the user has access to and knows how to operate their institutional email
- Without paper and pen to write down the password, the next login attempt would be impossible

**Derived design criteria:**
- RF01 must minimize the number of fields in the initial step and provide help text for each field (e.g., "Your employee ID is printed on your UADY credential")
- The RF01 confirmation flow must account for the email account being accessed by the same user; messages must be clear and step-by-step
- RF03 must tolerate infrequent access without penalizing users with quick lockouts after failed attempts
- RF10 must label receipts in plain language ("Payroll Receipt — January 2026") in addition to the technical folio number

---

## Scenario Summary

| Scenario | Persona | Flows involved | Critical design points |
|---|---|---|---|
| 1 — CFDI Download | Armando | RF02, RF03, RF10 | Recovery email in spam, CFDI labeling, prominent PDF button |
| 2 — Password Recovery | Concepción | RF02, RF03, RF30 | Username ambiguity, cross-device flow, PDF download as screen-photo alternative |
| 3 — Assisted Registration | Feliciano | RF01, RF03, RF10 | Number of registration fields, institutional email dependency, plain-language receipt labels |

---

## Relationship with Functional Requirements

All three scenarios confirm that **RF01, RF02, and RF03** concentrate the greatest friction for the primary user, consistent with what is established in the product requirements. Additionally, the scenarios provide concrete design criteria for RF05, RF10, RF20, and RF30 that complement the functional specifications already documented.

---

## References

- Fisk, A. D., Rogers, W. A., Charness, N., Czaja, S. J., & Sharit, J. (2018). *Designing for Older Adults: Principles and Creative Human Factors Approaches* (3rd ed.). CRC Press.
- Carroll, J. M. (2000). *Making Use: Scenario-Based Design of Human-Computer Interactions*. MIT Press.
- INEGI. (2023). *Encuesta Nacional sobre Disponibilidad y Uso de Tecnologías de la Información en los Hogares (ENDUTIH 2023)*. Instituto Nacional de Estadística y Geografía.
