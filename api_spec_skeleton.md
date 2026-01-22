# OCASI API Specification – Skeleton

This document provides a minimal, language‑agnostic outline of the OCASI API. It is not a full specification; it establishes the stable boundaries of the interface and illustrates how external services interact with the consent artefact.

## Base Principles

* Stateless, predictable HTTP interface
* JSON request/response structures
* No dependency on specific frameworks or identity systems
* Minimal set of operations to maintain clarity and reusability

## Endpoints

### 1. Create Consent

```
POST /consents
```

**Request body (example):**

```json
{
  "subject": "user:1234",
  "actor": "service:analytics",
  "purpose": "activity-insights",
  "conditions": {}
}
```

**Response:**

* 201 Created
* JSON: consent identifier and stored representation

### 2. Get Consent

```
GET /consents/{id}
```

Returns stored consent entry.

### 3. Update Consent

```
PATCH /consents/{id}
```

Allows modification of purpose, conditions, or actor.

### 4. Revoke Consent

```
DELETE /consents/{id}
```

Marks consent as revoked and invalid for future evaluations.

### 5. Evaluate Access

```
POST /evaluate
```

**Request body (example):**

```json
{
  "subject": "user:1234",
  "actor": "service:analytics",
  "purpose": "activity-insights"
}
```

**Response:**

```json
{
  "allowed": true
}
```

## Notes

* OCASI does not enforce authentication/authorization; that responsibility remains external.
* Evaluation is strictly based on consent-derived rules.

This skeleton defines the stable surface of the artefact while keeping implementation freedom for adopters.
