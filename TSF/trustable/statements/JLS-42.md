---
level: 1.1
normative: true
references:
  - type: project_website
    url: "https://github.com/nlohmann/json/blob/develop/.github/CONTRIBUTING.md#describe-your-changes"
    description: "Contribution guidelines requiring manual pull requests to describe the rationale behind non-trivial changes"
  - type: project_website
    url: "https://github.com/nlohmann/json/blob/develop/.github/CONTRIBUTING.md#reference-an-existing-issue"
    description: "Contribution guidelines requiring manual pull requests to link to an existing issue"
evidence:
  type: https_response_time
  configuration:
    target_seconds: 2
    urls:
      - "https://github.com/nlohmann/json/blob/develop/.github/CONTRIBUTING.md"
---

All manual pull requests to the nlohmann/json repository that introduce changes are expected to describe the rationale for the proposed change and to link to an existing issue, in accordance with the project’s contribution guidelines.
