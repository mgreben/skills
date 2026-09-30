---
name: security-review
description: Review application code, infrastructure, and designs for concrete security risks. Use for pull-request reviews, threat-focused design reviews, authentication or authorization changes, and handling of sensitive data; not for implementing offensive techniques.
---

# Security Review

Review the supplied change or design for exploitable security weaknesses in its actual trust boundaries. Do not claim a vulnerability without a plausible attack path and evidence from the artifact.

Start by identifying assets, entry points, trust boundaries, privileged actions, and sensitive data. Then examine the change for issues relevant to it, including:

- Authentication, authorization, tenancy isolation, and privilege escalation.
- Input handling at interpretation boundaries: queries, shells, templates, paths, redirects, deserialization, and outbound requests.
- Secret exposure, insecure storage or transport, unsafe logging, and data-retention mistakes.
- Dependency, configuration, cryptography, session, token, and error-handling regressions.
- Abuse controls appropriate to exposed actions, such as rate limits, replay protection, and resource limits.

Report only actionable findings, ordered by severity. For each, include the affected location, attack preconditions and path, impact, and a proportionate remediation. Distinguish confirmed findings from assumptions that need verification. Note important areas reviewed with no finding when that context helps.

Keep the review scoped to security. Do not turn a general code-quality concern into a security finding without a credible security consequence, and do not modify code unless requested.
