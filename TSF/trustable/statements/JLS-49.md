---
level: '1.1'
normative: true
references:
    - type: website
      url: "https://github.com/nlohmann/json/blob/55f93686c01528224f448c19128836e7df245f72/README.md?plain=1#L1842"
      description: "Instructions on how to run test suite without internet connectivity."
    - type: verbose_file
      path: "./cmake/download_test_data.cmake"
      description:  "File specifying that test data should be downloaded from given directory instead of external repository, if provided."
    - type: website
      url: "https://github.com/nlohmann/json_test_data"
      description: "External repository containing test data."
evidence:
        type: https_response_time
        configuration:
                target_seconds: 2
                urls:
                    - "https://github.com/nlohmann/json/blob/55f93686c01528224f448c19128836e7df245f72/README.md?plain=1#L1842"
                    - "https://github.com/nlohmann/json_test_data"
score:
    Erikhu1: 1.0
---

The eclipse-score/inc_nlohmann_json project mirrors the external nlohmann/json_test_data repository containing test data used in the unit tests executed in the CI pipeline, such that the test suite can be executed without internet connectivity.
