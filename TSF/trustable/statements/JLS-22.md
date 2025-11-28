---
level: 1.1
normative: true
references:
  - type: verbose_file
    path: "./.github/workflows/parent-workflow.yml"
    description: "Parent GitHub workflow that is scheduled to run daily and triggers the ubuntu workflow."
  - type: verbose_file
    path: "./.github/workflows/ubuntu.yml"
    description: "Ubuntu CI workflow that executes the nlohmann/json unit and integration tests in a controlled CI environment."
score:
    Jonas-Kirchhoff: 1.0
---

A scheduled GitHub workflow in eclipse-score/inc_nlohmann_json triggers the ubuntu CI workflow daily, executing the nlohmann/json unit and integration test suites under defined conditions in a controlled environment.