---
level: 1.1
normative: true
references:
    - type: file
      path: "./TSF/scripts/generate_list_of_tests.py"
      description: "Script that derives the list of test environments from the persistent test results database and compares it to the documented expectations."
    - type: file
      path: "./TSF/scripts/generate_list_of_misbehaviours.py"
      description: "Script that analyses GitHub issues labelled as bugs for nlohmann/json and produces a misbehaviours summary."
    - type: verbose_file
      path: "./TSF/docs/list_of_test_environments.md"
      description: "Documented list of test environments generated from the persistent test results database."
    - type: verbose_file
      path: "./TSF/docs/nlohmann_misbehaviours_comments.md"
      description: "Collected comments and classifications for known misbehaviours of the nlohmann/json library."
---

In eclipse-score/inc_nlohmann_json, TSF helper scripts automatically analyse collected test results and bug-labelled issues for the nlohmann/json library to derive test-environment coverage and misbehaviour summaries.
