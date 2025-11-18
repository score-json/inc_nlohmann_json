---
level: 1.1
normative: true
references:
  - type: project_website
    url: "https://github.com/nlohmann/json/security/advisories/new"
    description: "Well-defined process for issuing a vulnerability or bug report for the nlohmann/json library"
evidence:
  type: https_response_time
  configuration:
    target_seconds: 2
    urls:
      - "https://github.com/nlohmann/json/security/advisories/new"
---

The manual activity of issuing a vulnerability or bug report for the nlohmann/json library follows a well-defined process documented in the project’s security advisory workflow.
