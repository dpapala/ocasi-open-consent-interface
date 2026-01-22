# OCASI Consent Model

## Purpose

The OCASI consent model defines the minimal semantics required to reliably express, store, and evaluate explicit user consent across independent services. The model is intentionally compact to ensure broad reusability without imposing assumptions on application domains.

## Core Concepts

### Consent Subject

The entity about whom the consent applies (e.g., a user account, identifier, or pseudonymous token).

### Consent Actor

The entity requesting access (e.g., a service component or external application).

### Purpose

A short, machine-readable string describing *why* access is requested. OCASI treats purpose as a first‑class dimension of consent.

### Conditions

Optional constraints attached to a consent decision (e.g., time limitation, scope restriction). Conditions remain minimal and domain‑neutral.

## Lifecycle

Consent follows a predictable and reusable lifecycle:

1. **Create** – A new consent entry is established with subject, actor, purpose, and optional conditions.
2. **Update** – Consent may be modified to expand, limit, or clarify the decision.
3. **Revoke** – Consent can be withdrawn at any time. Revocation invalidates dependent access decisions.
4. **Evaluate** – A service asks OCASI whether a specific access request is valid under the current consent state.

## Minimal Data Representation (Example)

```json
{
  "subject": "user:1234",
  "actor": "service:analytics",
  "purpose": "activity-insights",
  "conditions": {
    "expiry": "2026-12-31T00:00:00Z"
  }
}
```

This model is stable and intentionally narrow to prevent scope expansion and ensure predictable behaviour for third-party adopters.
