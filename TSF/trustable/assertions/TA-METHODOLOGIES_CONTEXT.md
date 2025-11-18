---
level: 1.1
normative: false
---

**Guidance**

To satisfy this assertion, all manual processes used in the verification of XYZ must be documented, including the methodologies applied, the results for specific aspects and iterations, and evidence that these processes were reviewed against documented criteria.

Most analysis (e.g., data analysis for TA-ANALYSIS) should be automated to enable continuous feedback.
However, the quality of any remaining manual processes (whether from first parties or external third parties) must be considered and how they are documented and reviewed.
Considerations should be made about how manual processes may impact identifying and addressing Misbehaviours (TA-MISBEHAVIOURS).

Assignment of responsibilities for any manual work must follow a documented process that verifies competence and grants appropriate access, with automation applied where possible.
Resulting assigned responsibilities must ensure organisational robustness (e.g., avoidance of conflicts of interest) together with appropriate independent verification and validation.
Manual reviews involving source inspections must follow documented guidelines, with exceptions recorded and illustrated through examples.
These guidelines should evolve over time and cover:

- coding patterns (e.g., good patterns, anti-patterns, defensive coding)
- structured design practices (e.g., control flow constraints)
- complexity management (e.g., limiting feature creep)
- documentation (e.g., clear, formal figures and diagrams)
- feature subset restrictions (e.g., programming language subsets)
- code of conduct guidelines (e.g., review etiquette, handling disagreements)

Nevertheless, specific coding rules (e.g., memory allocation, typing, concurrency) should be integrated into automatic linting and static analysis tools where appropriate.

All processes and checks must themselves be reviewed to drive continuous improvement following specified guidelines.
Any resulting changes from reviews must follow change control, regardless of who initiates them or under what circumstances.

**Evidence**

- Manual process documentation
- References to methodologies applied as part of these processes
- Results of applying the processes
- Criteria used to confirm that the processes were applied correctly
- Review records for results

**Confidence scoring**

Confidence scoring for TA-METHODOLOGIES is based on identifying areas of need for
manual processes, assessing the clarity of proposed processes, analysing the
results of their implementation, and evaluating the evidence of effectiveness
in comparison to the analysed results

**Checklist**

- Are the identified gaps documented clearly to justify using a manual process?
- Are the goals for each process clearly defined?
- Is the sequence of procedures documented in an unambiguous manner?
- Can improvements to the processes be suggested and implemented?
- How frequently are processes changed?
- How are changes to manual processes communicated?
- Are there any exceptions to the processes?
- How is evidence of process adherence recorded?
- How is the effectiveness of the process evaluated?
- Is ongoing training required to follow these processes?
