---
name: qa-test-design
description: Design a risk-based set of QA test scenarios for a feature, change, bug fix, or release. Use when deciding what to test or preparing manual and automated test coverage; not for reviewing existing test code.
---

# QA Test Design

Turn the supplied requirement, design, change, or defect report into a practical test set that gives the team confidence to release. Inspect available behavior, interfaces, and relevant code or documentation before inferring scenarios. Ask focused questions when an unknown changes expected behavior, supported platforms, user permissions, or release risk.

Model the feature in terms of users, states, inputs, integrations, and observable outcomes. Cover the meaningful risks for the change, including:

- Primary user journeys and acceptance criteria.
- Boundary, empty, invalid, duplicate, and unexpected input.
- State transitions, permissions, roles, tenancy, and recovery from failures.
- API, database, third-party, asynchronous, and cross-feature integration behavior.
- Backwards compatibility, migration, browsers or devices, accessibility, localization, performance, and security when they are in scope.

Prioritize by impact and likelihood. Do not produce a generic exhaustive checklist or duplicate permutations that cannot reveal a distinct defect. Pairwise or representative coverage is appropriate when combinations are numerous; call out combinations that remain untested because they are low risk.

Present the recommendation as a compact test plan:

1. **Test scope and assumptions** — behavior considered and important unknowns.
2. **Release risks** — the failure modes that drive prioritization.
3. **Test scenarios** — grouped by area and marked P0, P1, or P2. Each includes preconditions or test data, action, and expected observable result.
4. **Execution guidance** — which scenarios belong in automated unit, integration, contract, end-to-end, or exploratory testing, and which need manual validation.
5. **Out of scope / open questions** — known gaps or decisions needed before release.

Use concrete business-language cases where possible. State expected results rather than describing only actions. Recommend test data that protects privacy and avoids production side effects. Do not write tests or change application code unless explicitly asked.
