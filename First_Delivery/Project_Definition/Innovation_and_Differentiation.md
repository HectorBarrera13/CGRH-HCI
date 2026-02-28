# Innovation and Differentiation

## CGRH Self-Service System – UADY

---

## Current Landscape

Human resources systems at Mexican higher education institutions — such as UNAM's SIIA or self-service portals at other public universities — implicitly assume a user with medium-to-high digital competence, prioritizing functional density over navigational clarity. At the UADY specifically, information such as CFDI receipts, FAR balances, and Savings Fund reports is currently distributed via email or made available upon individual request — a fragmented process with no centralized access point. When email delivery fails or employees need clarification, they resort to in-person visits to the CGRH, generating avoidable operational load. None of the existing approaches are designed with the retiree — or any specific employee group — as the primary user.

---

## Differentiating Proposal

This project inverts that premise: the information architecture is derived from the profile with the **lowest digital competence** within the target population, which has concrete consequences from the structure of the main menu (RF05) to the granularity of authentication error messages. Rather than adapting a generic system for older adults, the design starts from the retiree and scales upward.

### 1. RF02 as a First-Level Requirement

The clearest expression of this approach is treating password recovery (RF02) as a first-level design requirement, not a secondary flow. Fisk et al. in *Designing for Older Adults* (3rd ed., 2018) document that password management is one of the most frequent barriers leading to digital channel abandonment among older adults. Designing this flow with fewer steps, explicit feedback at each state, and no technical jargon sets it apart from comparable institutional systems, where password recovery is typically a poorly documented and hard-to-reach flow.

### 2. Desktop-First Design with Visual Accessibility Criteria

The choice of desktop over mobile-first is not a limitation but a deliberate design decision: it concentrates effort on a single wide viewing surface that enables larger typography, generous spacing, and low information density per screen. These factors are directly linked to usability for users with potential visual decline — a prevalent attribute in the 60+ segment that mobile-first portals systematically sacrifice.

### 3. Centralization with a Maximum Two-Level Navigation Depth

Centralizing CFDI, FAR, and Savings Fund in a single platform with a maximum navigation depth of two levels eliminates the current dispersion of data across different channels and reduces the user's cognitive load. In comparable systems, users must navigate across multiple sections or portals to access information that this system consolidates in a single authenticated session.

---

## Summary

Together, these decisions configure a system where cognitive accessibility is not a post-hoc adjustment layer but the guiding criterion from the initial design. The difference is not technological but methodological: applying HCI centered on the lowest-competence user as a starting point, rather than as a correction at the end of the process.

---

*Last updated: February 2026*
