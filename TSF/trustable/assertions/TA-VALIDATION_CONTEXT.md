---
level: 1.1
normative: false
---

(Note: The guidance, evidence, confidence scoring and checklist sections below are copied from [CodeThink's documentation of TSF](https://codethinklabs.gitlab.io/trustable/trustable/trustable/TA.html). However, the answers to each point in the evidence list and checklist are specific to this project.)

**Guidance**

This assertion is satisfied when tests demonstrate that the features specified to meet project Expectations (TT-EXPECTATIONS) are present and function as intended.
These tests run repeatedly in a controlled environment (TA-TESTs) on a defined schedule (e.g., daily, per change, or per candidate release of nlohmann/json).

Confidence grows when tests not only verify Expectations but also validate (continuously) that they meet stakeholder and user needs.
Robust validation depends on three aspects:

- TA-VALIDATION – a strategy that produces representative and stressing data.
- TA-DATA – appropriate handling of collected data.
- TA-ANALYSIS – analysis methods that remain dependable as the project evolves.

This structure enables iterative convergence toward required behaviours, even when early validation results are unsatisfactory.

A strategy to generate appropriate data addresses quantity, quality, and selection:

- Selection: Testing remains exploratory, combining monitoring with verified and new indicators (supporting TA-INDICATORS). 
  Coverage spans input, design, and output analysis with traceable specifications and results (considering TA-BEHAVIOURS).
  Tests also support calibration of capacity, scalability, response time, latency, and throughput, executed in targetted conditions and under stress (e.g., equivalence class and boundary-value testing).
- Quantity: Automation scheduling provides sufficient repetition and covers diverse environments (e.g., multiple hardware platforms).
  Failures block merge requests, with pre- and post-merge tests giving fast feedback.
  Adequacy of data is assessed through TA-ANALYSIS.
- Quality: Test suites include fault induction (considering TA-MISBEHAVIOURS) and checks that good data yields good results while bad data yields bad results.

**Evidence**

- Test results from per-change tests
  - **Answer**: CI runs the tests on each change (JLS-01), and their results are stored in the persistent test results database (JLS-18, JLS-45).
- Test results from scheduled tests as time series
  - **Answer**: Provided in JLS-22.

**Confidence scoring**

Confidence scoring for TA-VALIDATION is based on verification that we have
results for all expected tests (both pass / fail and performance).

**Checklist**

- Is the selection of tests correct?
  - **Answer**: The upstream nlohmann/json test suite plus the additional TSF-related tests cover the behaviours captured in the Expectations (JLEX-01, JLEX-02). However, they cannot cover all conceivable misbehaviours.
- Are the tests executed enough times?
  - **Answer**: Yes, tests run on each pull request and push via the CI workflows (JLS-01) and additionally on a daily schedule in inc_nlohmann_json (JLS-22).
- How confident are we that all test results are being captured?
  - **Answer**: 
- Can we look at any individual test result, and establish what it relates to?
  - **Answer**: For CI runs, yes. Each stored test result is linked to a specific CI workflow run (repo, run_id, run_attempt) and timestamp in workflow_info, so we can relate it back to the corresponding GitHub workflow execution, code revision and CI configuration (see JLS-18).
- Can we trace from any test result to the expectation it relates to?
  - **Answer**: 
- Can we identify precisely which environment (software and hardware) were used?
  - **Answer**: 
- How many pass/fail results would be expected, based on the scheduled tests?
  - **Answer**: 
- Do we have all of the expected results?
  - **Answer**: Yes, for the selected workflows we typically have results for each run potential gaps arise when CI runs are skipped or cancelled, or due to storge limitation 
- Do we have time-series data for all of those results?
  - **Answer**: Stored test results are timestamped and can be queried as a time series (JLS-18, JLS-45), but due to storage limits we only keep a truncated history rather than a complete time series over the whole project lifetime.
- If there are any gaps, do we understand why?
  - **Answer**: Yes, gaps arise by design from the memory sensitive storage strategy (only initial snapshots and relevant changes are kept, see TSF/scripts/README.md and JLS-45), from the fixed size limits on the persistent database, and from the fact that we do not collect runtime monitoring data for deployed instances yet (see AOU-09, AOU-18 and AOU-19).
- Are the test validation strategies credible and appropriate?
  - **Answer**: Yes, the upstream nlohmann/json test suite is extensive and is complemented by additional TSF-related tests. These tests are executed on each change and on a daily schedule via CI (JLS-01, JLS-22), and their results are stored and analysed through TA-DATA and TA-ANALYSIS.
- What proportion of the implemented tests are validated?
  - **Answer**: 
- Have the tests been verified using known good and bad data?
  - **Answer**: 
