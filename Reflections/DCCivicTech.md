## Diseña tu Ciudad: Civic Tech

During the activity of Diseña tu ciudad testing, there was one vulnerability that I considered is too dangerous. The app used OCR to read the user's INE for identity verification, but because the OCR was unreliable, the CURP field was left manually editable. The consequence was critical and was that a single user could vote multiple times by modifying the last two digits of their CURP, and since online voting was available, this manipulation would be completely undetectable.

In a commercial app, a design flaw might cost revenue or user trust. In a civic participation system, the same flaw can invalidate the democratic process it was built to support. As research on HCI and civic engagement has established, sustained use of civic technology remains low because developers focus almost exclusively on making flows completable, without considering the systemic consequences for the institutions involved. The editable CURP field is a direct example: the team solved a usability problem and created an integrity crisis. Trust in a civic system include two things: the user must trust the system works, and the institution must trust the results are legitimate. This decision broke both. 

The correct response to a failing OCR is not to make the field editable, it is to question if OCR based on INE recognition is the right mechanism for this context, and explore alternatives that preserve usability and integrity. This exercise clarified something easy to overlook: the responsibility of a designer is proportional to the consequences of a failure. For the CGRH system, a poorly designed error message causes frustration. For a civic voting system, a poorly designed identity verification flow can produce fraudulent results that misrepresent the preferences of an entire community. Civic technology operates in the public interest, and that obligation must be visible in every design decision, including the ones that seem purely technical.

---

### References

Harding, M., & Knowles, B. (2015). *HCI, civic engagement & trust*. CHI 2015, ACM.
https://dl.acm.org/doi/10.1145/2702123.2702255

Corbett, E., & Le Dantec, C. (2021). *Designing civic technology with trust*.
CHI 2021, ACM. https://dl.acm.org/doi/10.1145/3411764.3445341
