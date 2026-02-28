# Video Script — CGRH HCI Project
*Spoken narration guide | ~5–7 minutes*

---

## INTRO

"We'll walk you through our Human-Computer Interaction project for the Coordination of Human Resources system — known as CGRH — at the Universidad Autónoma de Yucatán, in Mexico.

Our team is made up of four Software Engineering students: Héctor Barrera, Héctor Castro, Rodrigo Alonzo, and Damián Villares."

---

## SECTION 1 — What is the system and why does it matter?

"The project is a self-service digital platform that allows all active and retired UADY employees to access three key pieces of financial information: their payroll receipts — known as CFDIs —, their Retirement Savings Fund, and their Savings Account.

Right now, employees who need any of these documents have to go in person to the university offices, or rely on someone else to get them. That's inefficient, and for retired employees who no longer have a reason to visit campus regularly, it can be a real problem.

Our project asks: what would it take to design this system so that even the most digitally inexperienced user can use it successfully, on their own, from home?"

---

## SECTION 2 — Our user focus

"To answer that question, we made a deliberate design decision. Instead of targeting the average user, we focused our HCI analysis on the most challenging user segment: retired UADY employees over 60 years old, with basic digital literacy, using low-end desktop computers, and with possible visual and cognitive limitations.

Why this group? According to Mexico's ENDUTIH 2023 survey by INEGI, only 43.7% of people between 55 and 64 years old used the internet in the past year, compared to 82.8% of people aged 25 to 34. That's a massive gap — and it reflects the real barriers our target users face every day.

Our reasoning is simple: if we design a system that works well for the most demanding user profile, it will work well for everyone else too."

---

## SECTION 3 — User Research Plan

"To understand our users, we designed a structured research plan covering four methods.

**First, interviews** — to gather qualitative data about users' needs, past experiences with digital platforms, and their expectations for the system.

**Second, contextual inquiry** — where a researcher observes a user in their real environment, at their own computer, while they interact with a familiar platform. This lets us capture behaviors and barriers that users wouldn't necessarily mention in a conversation.

**Third, surveys** — to collect broader data from a larger group of retired employees, identifying common patterns in how they access technology and what difficulties they encounter most often.

**And fourth, usability testing** — where users attempt to complete key tasks in the system, such as logging in, recovering a password, or downloading a payroll receipt. This gives us direct evidence of friction points before they become permanent design problems.

Each method is assigned to specific team members, with clear deadlines and defined deliverables — all documented in our project repository."

---

## SECTION 4 — User Profiles and Personas

"Based on our user profile research and secondary data, we created three personas — detailed fictional representations of our target users.

It's important to note: these are assumption-based proto-personas. They were built from statistical data, domain analysis, and functional requirements — not from completed fieldwork. They will be refined as our primary research progresses. This is a methodologically valid practice when research is still ongoing.

**Our first persona is Don Armando** — a 67-year-old retired professor who needs to download his payroll receipts to present at a bank. He has basic-to-medium digital skills, uses WhatsApp and YouTube, but has never downloaded a PDF on his own. His main frustration? Forgetting his password and not understanding error messages.

**Our second persona is Doña Concepción** — a 63-year-old retired administrative employee who doesn't remember whether her username is her employee number, her name, or her email. She borrows her daughter's laptop to access the system and feels like she'll 'break something' if she clicks the wrong button.

**Our third persona is Don Feliciano** — a 69-year-old retired maintenance worker from Kanasín who has never used a computer during his working life, has no personal device, no home internet, and no email account. For him, even getting to the registration step is a significant barrier.

Together, these three personas represent a spectrum of digital exclusion — and they directly shaped the design priorities of our system."

---

## SECTION 5 — Scenarios

"To translate those personas into concrete design decisions, we developed three use scenarios.

**In the first scenario**, Armando needs to download his last three payroll receipts for a loan application. He gets his password wrong twice, finds the recovery link, checks his spam folder for the reset email, and eventually succeeds — but the process reveals three critical design problems: credential memory, spam folder awareness, and unclear labeling of the term 'CFDI.'

**In the second scenario**, Concepción tries to check her Savings Fund balance while her daughter is at work. She's unsure what her username is, recovers her password across two devices — the laptop and her daughter's phone — and ultimately photographs the screen instead of downloading a PDF because she doesn't know how to save a file.

**In the third scenario**, Feliciano visits a neighbor's house to register for the first time. He can't complete any step without full assistance — the registration form requires data he doesn't have memorized, and the email confirmation flow assumes he has independent access to his institutional email.

Each scenario directly generated design criteria that are now reflected in our functional requirements."

---

## SECTION 6 — Functional and Non-Functional Requirements

"Our system has eight functional requirements. The three highest-friction ones are **RF01 — Registration**, **RF02 — Password Recovery**, and **RF03 — Login**. These are the entry points to the entire system — a failure at any of them means the user can't access anything at all.

The three highest-frequency ones are **RF10 — CFDI inquiry**, **RF20 — Retirement Savings Fund**, and **RF30 — Savings Account**. These are the core value of the platform.

But what makes our requirements document distinctive from an HCI perspective is the non-functional requirements. We defined twelve usability-focused NFRs, each with measurable acceptance criteria.

Error messages in plain everyday language, maximum two sentences. No task should require more than three interactions from the main menu. And a human support phone number always visible on screen.

These requirements are grounded in Nielsen's ten usability heuristics and the ISO 9241-11 standard on usability definitions.

We also defined six global acceptance criteria, including a task success rate of at least 80% for the target user profile, a System Usability Scale score of 70 or above, and zero severity-4 or severity-5 usability errors in heuristic review."

---

## OUTRO

"To summarize: this project is not just about building a system — it's about building the right system for people who are often left behind by digital design.

By centering our analysis on retired employees over 60, we're making a case that accessibility and usability aren't optional features — they're the foundation.

All of our documentation, research instruments, personas, scenarios, and requirements are available in our public GitHub repository."

---

*Total estimated reading time at a calm, clear pace: ~6 minutes.*
