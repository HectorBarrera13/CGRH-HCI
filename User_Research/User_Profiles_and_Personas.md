# User Profiles and Proto-Personas

## CGRH System – UADY

**Prepared by:** Damián Villares, Héctor Castro  
**Date:** February 27, 2026

> **Methodological note:** The personas presented in this document are **assumption proto-personas**, built from secondary data (ENDUTIH 2023, INEGI), institutional domain analysis, and the functional requirements defined for the CGRH system. They are not derived from formal primary research; rather, they precede and guide it. They will be refined and validated as planned primary research activities progress (interviews, surveys, usability testing). This practice is methodologically standard when fieldwork is still in the design phase or has not yet concluded (Cooper, 2004; Gothelf & Seiden, 2016).

---

## 1. General User Profile

### 1.1 Primary Users

**Primary users** are those who interact directly with the CGRH system to consult their financial and administrative information.

| Attribute | Description |
|---|---|
| **Segment** | Retired UADY employees |
| **Age range** | 60 years and older |
| **Previous occupation** | Teaching, administrative, or support staff at UADY |
| **Digital literacy level** | Basic (43.7% of the population aged 55–64 used the internet in the past year, ENDUTIH 2023, INEGI) |
| **Primary access device** | Desktop computer (low-end specifications) |
| **Use context** | Home; no regular presence at university facilities |
| **Estimated use frequency** | Monthly or sporadic (CFDI, FAR, and Savings Fund inquiries) |
| **Dependence on in-person channel** | High — currently reliant on in-person procedures or intermediaries |

**Barriers identified in the literature and domain:**
- Difficulty remembering and managing passwords (Fisk et al., *Designing for Older Adults*, 3rd ed., 2018)
- Possible visual decline affecting the reading of small text
- Tendency to abandon digital flows when error messages are unclear
- Low exposure to institutional digital platforms

### 1.2 Secondary Users

**Secondary users** interact with the system indirectly or in specific contexts.

| Segment | Relationship with the system |
|---|---|
| CGRH administrative staff | Handles inquiries from retirees who were unable to complete the flow autonomously |
| Retiree's family members or assistants | In some cases, they support the primary user in tasks such as logging in or downloading documents |
| Active UADY staff (faculty and administrators) | Share the platform but experience a lower level of digital friction |

---

## 2. Proto-Personas

---

### Proto-Persona 1 — "Don Armando"

> *Retired faculty member who needs his CFDIs for external administrative procedures*

| Field | Detail |
|---|---|
| **Name** | Armando Cetina Pech |
| **Age** | 67 years old |
| **Previous occupation** | Full-time professor, School of Engineering, UADY (35 years of service) |
| **Place of residence** | Mérida, Yucatán |
| **Device** | Desktop computer with Windows 10; 19" monitor |
| **Connectivity** | Home internet (basic service) |
| **Digital competence** | Basic-medium — uses WhatsApp and YouTube, but has never independently downloaded a PDF |

**Goals:**
- Download his payroll receipts (CFDI) to present as proof of income at a financial institution
- Access his Retirement Savings Fund (FAR) information to plan a major expense
- Complete these procedures without having to travel to UADY facilities

**Frustrations:**
- "I never know if I'm doing the process right; when an error message appears I don't understand what it means"
- Regularly forgets his password because he doesn't write it down and has no clear recovery method
- On-screen instructions feel small and use terms he doesn't recognize (RFC, XML, CURP)

**Representative quote:**  
*"Before I used to go to the service window and in ten minutes I had my receipt. Now they tell me I can do it from the computer, but every time I try I get stuck on something different."*

**Requirements relationship:**  
Primarily RF01 (registration), RF02 (password recovery), RF03 (login), RF10 (CFDI inquiry), RF20 (FAR).

---

### Proto-Persona 2 — "Doña Concepción"

> *Retired administrative employee with minimal digital experience who depends on external support*

| Field | Detail |
|---|---|
| **Name** | Concepción Dzul Rosado |
| **Age** | 63 years old |
| **Previous occupation** | Administrative assistant, General Office of School Administration, UADY (28 years of service) |
| **Place of residence** | Mérida, Yucatán |
| **Device** | Her daughter's laptop, which she borrows when needed |
| **Connectivity** | Shared family internet connection |
| **Digital competence** | Basic — uses her phone mainly for calls and text messages; computer use is sporadic |

**Goals:**
- Check her Savings Fund balance before making a payment
- Obtain her payroll receipts without needing a family member to take her to the CGRH office

**Frustrations:**
- Doesn't remember what her "username" is or whether it's her name, employee number, or institutional email
- When she tries to register, forms feel long and confusing (RFC, CURP, CAPTCHA)
- Feels like she'll "break something" if she clicks in the wrong place

**Representative quote:**  
*"I ask my daughter to help me because I can't do it on my own. But I also don't want to bother her every time I need a document."*

**Requirements relationship:**  
Primarily RF01 (registration with multiple fields — highest friction point for this profile), RF03 (login), RF04 (logout), RF30 (Savings Fund).

---

### Proto-Persona 3 — "Don Feliciano"

> *Retired facilities and maintenance staff member with no prior computer experience; first contact with a digital system*

| Field | Detail |
|---|---|
| **Name** | Feliciano Canul Tzuc |
| **Age** | 69 years old |
| **Previous occupation** | Maintenance and general services staff, Campus of Exact Sciences, UADY (30 years of service) |
| **Place of residence** | Municipality of Kanasín, Yucatán |
| **Device** | No personal computer; accesses from a neighbor's computer or at a print and copy shop |
| **Connectivity** | No home internet; uses limited mobile data on a basic phone |
| **Digital competence** | Very low — never used a computer during his working life; phone use is limited to calls and receiving photos via WhatsApp |

**Goals:**
- Obtain his payroll receipts (CFDI) to present in an IMSS pension procedure
- Avoid traveling to UADY facilities in Mérida to get a document
- Be able to complete the process with the help of a trusted person present in the same location

**Frustrations:**
- Has never created an account on any digital platform; doesn't know what a "username" or "password" is
- His RFC and CURP are written on physical documents at home; he doesn't have them memorized or digitized
- Feels the process is "for people who know about computers" and hesitates to try without in-person assistance
- Has no email account and doesn't know how to create one, which completely blocks the registration process

**Representative quote:**  
*"Passwords and emails are not my thing. If someone teaches me step by step, maybe I can do it. But on my own I won't risk doing something wrong."*

**Requirements relationship:**  
Primarily RF01 (registration — highest barrier for this profile: email account required, RFC, CURP, CAPTCHA), RF02 (password recovery — no autonomous email access), RF03 (login — first use of the system).

---

## 3. Synthesis — Primary Profile Patterns

| Pattern | Present in |
|---|---|
| Difficulty with passwords and credentials | Armando, Concepción, Feliciano |
| Dependence on external support (family or CGRH) | Concepción, Feliciano |
| Technical terminology as a barrier (RFC, CURP, CAPTCHA, XML) | Armando, Concepción, Feliciano |
| No personal access to email | Feliciano |
| No personal device or internet connection | Feliciano |
| Need for larger typography and low information density | Armando, Concepción |
| Infrequent use that increases memory load | All three profiles |
| Primary channel: desktop computer | All three profiles |

---

## References

- Fisk, A. D., Rogers, W. A., Charness, N., Czaja, S. J., & Sharit, J. (2018). *Designing for Older Adults: Principles and Creative Human Factors Approaches* (3rd ed.). CRC Press.
- INEGI. (2023). *Encuesta Nacional sobre Disponibilidad y Uso de Tecnologías de la Información en los Hogares (ENDUTIH 2023)*. Instituto Nacional de Estadística y Geografía.
- Cooper, A., Reimann, R., & Cronin, D. (2004). *About Face 3: The Essentials of Interaction Design*. Wiley.
- Gothelf, J., & Seiden, J. (2016). *Lean UX: Applying Lean Principles to Improve User Experience* (2nd ed.). O'Reilly Media.
