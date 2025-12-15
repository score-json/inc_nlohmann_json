---
level: 1.1
normative: true
references: 
    - type: verbose_file
      path: "./.github/workflows/coverage_gate.yml"
      description: "GitHub Actions workflow enforcing a limit on open PRs."
    - type: verbose_file
      path: "./.github/workflows/parent-workflow.yml"
      description: "Parent CI workflow that calls the pr_count_gate workflow."
---

In eclipse-score/inc_nlohmann_json, a GitHub workflow checks the number of open pull requests in the main repository. If the number exceeds a defined threshold, the workflow fails and blocks further merges until the number of open pull requests is reduced below that threshold.