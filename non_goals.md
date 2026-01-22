# OCASI – Non‑Goals

To maintain strict scope clarity and the characteristics of a small, self‑contained commons artefact, OCASI explicitly excludes the following areas. These non‑goals are intentional design decisions and help ensure the artefact remains predictable, reusable, and independent.

## Not a General Authorization Framework

OCASI does not serve as a replacement for authorization systems, RBAC/ABAC engines, or policy decision points. It only evaluates **consent‑derived** access decisions.

## Not a Policy Engine

It does not provide rule authoring, rule composition, or complex policy evaluation features. No rule language, no multi-condition evaluation, no policy inheritance.

## Not an Identity Provider

OCASI does not manage authentication, identity resolution, user credentials, tokens, or sessions. It assumes identities are resolved externally.

## Not a Compliance, GDPR, or Legal Management Toolkit

OCASI does not generate legal text, manage terms & conditions, nor track legal provenance. It focuses solely on functional consent logic.

## Not a Permission Management Suite

It is not a roles/permissions system, does not manage hierarchical permissions, and does not orchestrate application-level authorization.

## Not a Platform or Extensible Framework

OCASI does not attempt to grow into a broader access-control ecosystem. The artefact is intentionally **small**, **complete**, and **independent**.

## Scope Boundary

OCASI’s sole responsibility is:
**Translate explicit user consent into machine-evaluable access decisions, and nothing beyond that.**
