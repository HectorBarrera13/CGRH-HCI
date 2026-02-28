# Product Requirements

**Universidad Autónoma de Yucatán — Facultad de Matemáticas | Software Engineering**  
**HCI Deliverable — CGRH System (General Coordination of Human Resources)**  
*Mérida, Yucatán, 2026*

---

## Table of Contents

1. [Introduction and System Context](#1-introduction-and-system-context)
2. [Functional Requirements Summary](#2-functional-requirements-summary)
3. [Functional Requirements — Detailed Description](#3-functional-requirements--detailed-description)
   - [RF01 — Employee Registration](#31-rf01--employee-registration--high-friction)
   - [RF02 — Password Recovery](#32-rf02--password-recovery--high-friction)
   - [RF03 — Login](#33-rf03--login--high-friction)
   - [RF04 — Logout](#34-rf04--logout)
   - [RF05 — Main Menu](#35-rf05--main-menu)
   - [RF10 — CFDI Consultation](#36-rf10--cfdi-consultation--high-frequency)
   - [RF20 — Retirement Savings Fund](#37-rf20--retirement-savings-fund--high-frequency)
   - [RF30 — Savings Fund](#38-rf30--savings-fund--high-frequency)
4. [Non-Functional Usability Requirements](#4-non-functional-usability-requirements)
5. [RF — RNF Relationship Matrix](#5-rf--rnf-relationship-matrix)
6. [Global HCI Acceptance Criteria](#6-global-hci-acceptance-criteria)
7. [References](#7-references)

---

## 1. Introduction and System Context

The CGRH System (General Coordination of Human Resources) of the Universidad Autónoma de Yucatán is a digital self-service platform that allows **all active and retired UADY employees** to consult their financial information: payroll receipts (CFDI), Retirement Savings Fund (FAR), and Savings Fund.

For the purposes of this HCI analysis — framed as an academic subproject — the usage context of greatest interest involves **retired employees over 60 years of age** with basic digital literacy, predominantly accessing from low-end desktop computers with possible visual and cognitive limitations. This profile defines the design priorities of all requirements described here, under the premise that criteria derived from the highest-friction segment benefit the system as a whole.

> **System users:** All active and retired UADY employees.  
> **HCI analysis segment (academic subproject):** Retired UADY employees, 60+ years, basic digital literacy, low-end desktop computers.

---

## 2. Functional Requirements Summary

The system contemplates 8 functional requirements grouped into two categories from the HCI perspective:

- **Authentication and access (RF01–RF05):** Highest friction points for the target user.
- **Benefits consultation (RF10, RF20, RF30):** Higher use frequency and direct value for the retiree.

| ID | Name | HCI Priority | Data Involved | Friction Level (60+ user) |
|---|---|---|---|---|
| RF01 | Employee Registration | High | Employee ID, RFC, CURP, institutional email, password, phone | **High** — multiple fields, CAPTCHA, 2-step flow |
| RF02 | Password Recovery | High | Institutional email → temporary link → new password | **High** — credential memory, email management |
| RF03 | Login | High | Username + password → system access | **High** — entry point; blockage = no access to anything |
| RF04 | Logout | Medium | Logout button in menu | **Low** — clear and visible action |
| RF05 | Main Menu | High | Options view after login | **Medium** — user navigation and orientation |
| RF10 | CFDI Consultation | Very High | Receipt list with filters, PDF/XML download | **Medium** — financial data reading, download |
| RF20 | Retirement Savings Fund | Very High | Card with balances, contributions, returns, PDF download | **Medium** — critical financial information |
| RF30 | Savings Fund | Very High | Savings fund account summary, PDF download | **Medium** — critical financial information |

> **Note:** Requirements RF01, RF02, and RF03 represent the **highest friction points** for the 60+ user. A failure in any of these blocks access to the entire platform.

---

## 3. Functional Requirements — Detailed Description

---

### 3.1 RF01 — Employee Registration — High Friction

| Field | Detail |
|---|---|
| **Actor** | UADY Employee / Retiree |
| **Description** | The employee can register on the platform to consult their payroll documents, funds, and manage their benefits. |
| **Precondition** | The user has internet access and knows their UADY institutional email, RFC, and CURP. |

**Main Flow:**
1. User accesses the registration option.
2. System displays form — Step 1: Employee ID, RFC, CURP, institutional email, email confirmation, CAPTCHA.
3. User completes data and clicks **"Continue"**.
4. System validates and displays Step 2: name (non-editable, retrieved from payroll system), username (auto-assigned), password, confirmation, phone number.
5. User completes and clicks **"Register"**.
6. System sends confirmation email with link.
7. User confirms and can log in.

**Alternative Flows:**
- **Alt. 1:** Invalid email format → error message on the field.
- **Alt. 2:** Expired confirmation link → message and re-registration option.
- **Alt. 3:** Emails don't match → field highlighted in red with descriptive message.
- **Alt. 4:** User already registered → informational message with link to login.

> **HCI/Usability Considerations:** Two-step flow is necessary but complex for older adults. Recommendations: clear instructions before each field, visible progress indicator ("Step 1 of 2"), error messages in plain language without technical jargon, accessible CAPTCHA, minimum font size 16pt, buttons with minimum clickable area of 44×44 px and sufficient spacing to avoid accidental clicks with a mouse. Consider a visual guide or tutorial for first-time access.

---

### 3.2 RF02 — Password Recovery — High Friction

| Field | Detail |
|---|---|
| **Actor** | Registered UADY Employee / Retiree |
| **Description** | A registered employee who forgot their password can recover access through their institutional email. |
| **Precondition** | The user is registered in the system and has access to their institutional email (@correo.uady.mx). |

**Main Flow:**
1. User selects "Forgot your password?" on the login screen.
2. System requests institutional email.
3. User enters email and confirms.
4. System sends a temporary link to the email.
5. User opens the link.
6. System presents new password form.
7. User creates and confirms new password.
8. System confirms the change and redirects to login.

**Alternative Flows:**
- **Alt. 1:** Email not registered → message "Email not found".
- **Alt. 2:** Expired link → message and resend option.
- **Alt. 3:** New password does not meet requirements → visual indication of rules.

> **HCI/Usability Considerations:** This is the most critical flow in the system for older adults: it involves remembering a password, accessing email, and creating a new complex password. Recommendations: show password requirements in real time with a visual indicator (weak/medium/strong), allow viewing the entered password (eye icon), extremely clear error messages, link expiration time no less than 30 minutes, and always show the HR phone number as a support alternative.

---

### 3.3 RF03 — Login — High Friction

| Field | Detail |
|---|---|
| **Actor** | Registered UADY Employee / Retiree |
| **Description** | The registered employee logs in with their username and password to access the system. |
| **Precondition** | The user is registered in the system. |

**Main Flow:**
1. User accesses the login screen.
2. System displays: institutional logo, username and password fields, "Log In" button, and "Forgot your password?" link.
3. User enters username and password.
4. System validates credentials.
5. System displays main menu (RF05).

**Alternative Flows:**
- **Alt. 1:** Incorrect username or password → message "Username or password is incorrect", fields are cleared.
- **Ext. 1:** User selects "Forgot password" → RF02 flow.

> **HCI/Usability Considerations:** Login is the system's entry point. Recommendations: pre-filled username field if the device allows it, show/hide password button, descriptive error message without revealing which field is incorrect (security), highly visible recovery link, do not automatically lock the account without prior warning. Consider a "Remember me" option for trusted devices.

---

### 3.4 RF04 — Logout

| Field | Detail |
|---|---|
| **Actor** | UADY Employee / Retiree with active session |
| **Description** | The employee can close their session explicitly and securely. |
| **Precondition** | The user has an active session in the system. |

**Main Flow:**
1. User locates and selects the "Log out" option in the menu.
2. System invalidates the user's session.
3. System redirects to the login screen.

**Alternative Flows:** No significant alternative flows. The session can also expire due to inactivity timeout.

> **HCI/Usability Considerations:** Logout element must always be visible and clearly labeled as "Log out" (no ambiguous icons). Consider a confirmation prompt before logging out to prevent accidental closures. Inactivity timeout before automatic logout must be generous (minimum 15 minutes) given the user profile.

---

### 3.5 RF05 — Main Menu

| Field | Detail |
|---|---|
| **Actor** | Authenticated UADY Employee / Retiree |
| **Description** | After login, the user sees the main menu that gives access to all available functions. |
| **Precondition** | The user has successfully logged in (RF03). |

**Main Flow:**
1. System displays main screen with available options: CFDI, Retirement Savings Fund, Savings Fund.
2. User selects desired option.
3. System navigates to the corresponding section.

**Alternative Flows:** No alternative flows. The menu is the main distribution point.

> **HCI/Usability Considerations:** Key orientation point. Recommendations: maximum 4–5 visible options to avoid cognitive overload, representative icons **always** accompanied by descriptive text, clear visual hierarchy, personalized welcome with the user's name, and HR support number always visible on this screen.

---

### 3.6 RF10 — CFDI Consultation — High Frequency

| Field | Detail |
|---|---|
| **Actor** | Authenticated UADY Employee / Retiree |
| **Description** | The employee can view and download their Digital Tax Receipts (payroll receipts). |
| **Precondition** | The user has logged in. The system has the employee's CFDIs. |

**Main Flow:**
1. User selects "CFDI" from the main menu.
2. System displays table with CFDIs for the current month/year: folio, department, pay period, payment dates, days paid, download buttons (PDF/XML).
3. Available filters: year and month of payment date.
4. User can download individual PDF, individual XML, or select multiple/all for bulk download (.zip).
5. System generates and downloads the requested file.

**Alternative Flows:**
- **Alt. 1:** No filters applied → shows all CFDIs for the current year.
- **Alt. 2:** User cancels .zip download → system closes the save dialog.

> **HCI/Usability Considerations:** Most frequently used function in the system. Recommendations: display the most recent CFDI first, use familiar terms ("Payroll Receipt" alongside "CFDI"), large and visible PDF download buttons (PDF is more familiar than XML for older adults), simple filters with dropdown lists, clear pagination with visible page numbers, pay period labels in a comprehensible format ("1st period January" not just "01/01/2026").

---

### 3.7 RF20 — Retirement Savings Fund — High Frequency

| Field | Detail |
|---|---|
| **Actor** | Authenticated UADY Employee / Retiree |
| **Description** | The employee can view a summary of their Retirement Savings Fund (FAR) account administered by Banco Santander. |
| **Precondition** | The user has logged in. The system has the employee's FAR data (loaded by HR). |

**Main Flow:**
1. User selects "Retirement Savings Fund".
2. System displays card with:
   - General data: employee ID and name, date of last report.
   - Financial summary: Opening Balance, Contributions, Withdrawals, Returns, Closing Balance, Vested Rights.
   - Banco Santander note.
   - "Download" PDF report button.
3. User can download the complete report in PDF.

**Alternative Flows:** No alternative flows (data is read-only).

> **HCI/Usability Considerations:** Financially high-value and emotionally significant information for the retiree. Recommendations: display the Closing Balance prominently in large typography, use a visually well-delimited card, briefly explain each concept ("Returns: interest generated by your savings"), clearly indicate the data date to avoid confusion about validity, large and clearly labeled PDF download button.

---

### 3.8 RF30 — Savings Fund — High Frequency

| Field | Detail |
|---|---|
| **Actor** | Authenticated UADY Employee / Retiree |
| **Description** | The employee can view a summary of their Savings Fund account. |
| **Precondition** | The user has logged in. The system has the employee's savings fund data. |

**Main Flow:**
1. User selects "Savings Fund".
2. System displays card with account summary: employee data, balances, period movements.
3. User can download report in PDF.

**Alternative Flows:** No alternative flows (data is read-only).

> **HCI/Usability Considerations:** Same considerations as RF20. Clear visual presentation with emphasis on current balance and report download. **Visual consistency with RF20** is important to reduce the user's learning curve.

---

## 4. Non-Functional Usability Requirements

The following NFRs are derived from the target user profile and grounded in Nielsen's heuristic principles (1994) and ISO 9241-11:2018. Four dimensions are prioritized: **visual accessibility, legibility, cognitive load, and trust/support**.

| ID | Usability Attribute | Description / Acceptance Criterion | Related RFs | Nielsen Heuristic |
|---|---|---|---|---|
| RNF-01 | Legibility — Font size | Minimum font size of **16pt** throughout the interface. Headings ≥ 20pt. No text smaller than 14pt in any element. | All RFs | H8 — Aesthetic and minimalist design |
| RNF-02 | Minimum clickable area | Minimum clickable area of **44×44 px** for all buttons and interactive items. Sufficient spacing between adjacent elements to prevent accidental clicks with a mouse. | All RFs | H7 — Flexibility and efficiency |
| RNF-03 | Visual contrast | Minimum contrast ratio of **4.5:1 (WCAG AA)** between text and background. Never use light gray on white. | All RFs | H8 — Aesthetic and minimalist design |
| RNF-04 | Clear error messages | Messages in everyday language, no error codes, with a clear indication of what to do. Maximum 2 sentences. | RF01, RF02, RF03 | H9 — Help users recognize, diagnose, and recover from errors |
| RNF-05 | Recognition over recall | All options visible; never rely on the user remembering routes. Visible breadcrumbs in navigation. | RF05, RF10, RF20, RF30 | H6 — Recognition rather than recall |
| RNF-06 | Response time | Load ≤ **3 seconds** on desktop connections with basic bandwidth (≥ 5 Mbps). Visible loading indicator if operation takes more than 1 second. | RF10, RF20, RF30 | H1 — Visibility of system status |
| RNF-07 | Short flows | The number of steps to complete any consultation task must not exceed **3 interactions** from the main menu. | RF10, RF20, RF30 | H7 — Flexibility and efficiency |
| RNF-08 | Error prevention | Destructive buttons must include explicit confirmation. Forms validate in real time before submission. | RF01, RF02, RF04 | H5 — Error prevention |
| RNF-09 | Visible human support | HR contact number **always visible** in the main menu and on error screens. Analog alternative always present. | RF05, error screens RF01–RF03 | H10 — Help and documentation |
| RNF-10 | Visual consistency | Same color scheme, typography, iconography, and interaction patterns throughout the application. Same terms for the same concepts. | All RFs | H4 — Consistency and standards |
| RNF-11 | Browser and desktop compatibility | Works correctly on modern desktop browsers (**Chrome 90+, Firefox 90+, Edge 90+**) with screen resolutions from **1280×720 px**. Desktop-first design; mobile device support is not contemplated. | All RFs | H7 — Flexibility and efficiency |
| RNF-12 | Task success rate | ≥ **80%** of users from the target profile complete each task without assistance. Time on consultation tasks ≤ **90 seconds**. | RF10, RF20, RF30 | ISO 9241-11 — Effectiveness |

---

## 5. RF — RNF Relationship Matrix

Criticality matrix: **✓✓** = Critical for this RF | **✓** = Relevant for this RF

| RF | Legibility | Clickable Area | Contrast | Error Messages | Recognition | Short Flows | Visible Support | Error Prevention |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| RF01 | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓ | ✓✓ | ✓ | ✓✓ |
| RF02 | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓ | ✓✓ | ✓✓ | ✓✓ |
| RF03 | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓ | ✓ | ✓✓ | ✓ |
| RF04 | ✓ | ✓✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓✓ |
| RF05 | ✓✓ | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓ | ✓✓ | ✓ |
| RF10 | ✓✓ | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓✓ | ✓ | ✓ |
| RF20 | ✓✓ | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓✓ | ✓ | ✓ |
| RF30 | ✓✓ | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓✓ | ✓ | ✓ |

---

## 6. Global HCI Acceptance Criteria

The following criteria define the minimum usability quality that the system must achieve before being considered suitable for the target users:

| # | Criterion | Metric | Target RF |
|---|---|---|---|
| T1 | **Task success rate** | ≥ 80% of users from the target profile complete each task without external assistance. | All |
| T2 | **Time on consultation tasks** | ≤ 90 seconds from the main menu to displaying the key data. | RF10, RF20, RF30 |
| T3 | **Abandonment rate** | ≤ 10% on critical tasks during usability testing. | RF01, RF02, RF03 |
| T4 | **SUS score** | ≥ 70 on the SUS scale adapted with simplified language for the target profile. | All |
| T5 | **Severe usability errors** | 0 level 4–5 errors (Nielsen scale) in heuristic review by ≥ 3 evaluators. | All |
| T6 | **WCAG AA compliance** | Minimum contrast of 4.5:1 in all text elements. Verified with an automated tool. | All |

---

## 7. References

- Nielsen, J. (1994). *10 Usability Heuristics for User Interface Design*. Nielsen Norman Group.
- ISO 9241-11:2018. *Ergonomics of human-system interaction — Part 11: Usability: Definitions and concepts*.
- WCAG 2.1 — *Web Content Accessibility Guidelines*. W3C, 2018.
- Brooke, J. (1996). *SUS: A 'quick and dirty' usability scale*. Usability Evaluation in Industry.
- UADY CGRH — Functional requirements documents RF01–RF30, UADY Benefits System, 2025–2026.

---

*Human-Computer Interaction — Software Engineering, UADY | 2026*
