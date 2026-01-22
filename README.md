# OCASI – Open Consent-Aware Interface

## Overview

OCASI is a small, self-hostable reference component digital commons artefact designed to provide a clear, machine-readable interface for handling explicit user consent in decentralized and self-hosted services. Its purpose is to externalize consent management from applications, reducing duplicated logic and enabling consistent, reusable consent-derived access rules across systems.

The artefact focuses strictly on the lifecycle and evaluation of explicit consent. It does not seek to become a general authorization or identity framework. OCASI is intentionally narrow, stable in scope, and designed to operate as a standalone component.

## Scope

OCASI handles:

* Creation, update, and revocation of explicit user consent
* Evaluation of consent-derived access rules
* A neutral, language-agnostic API contract suitable for diverse environments

See **NON_GOALS.md** for explicit boundaries.

## Value as a standalone artefact

OCASI is designed for adoption by any third-party service without coupling to the authors, specific platforms, or proprietary infrastructure. It is deployable, usable, and extensible entirely without involvement from the original authors.

## Deliverables

By the end of the grant period, the project will produce:

* A self-hostable OCASI service
* An open API specification
* A documented consent model
* Minimal reference integrations

All artefacts will be released as free and open digital commons.
