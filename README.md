# CoreLink Mock Server

> **Maturity: Scaffold / Planned** — there is no supported mock runtime, container, or package in this repository yet.

CoreLink Mock Server is the planned deterministic local/CI simulation boundary for versioned CoreLink public APIs, authentication/tenant failures, events/webhooks, and recovery scenarios.

## Current state

This repository currently contains documentation only. Contrary to an older scaffold description, the CoreLink contract repository is **not empty**: `api-contracts` contains a `1.0.0-draft` public OpenAPI boundary, AsyncAPI/event material, schemas, compatibility policy/matrix, runtime-parity documentation, and Postman assets.

The missing piece is the mock implementation and conformance evidence—not the existence of contract sources.

## Contract source

Normative behavior must come from [`CoreLinkPlatform/api-contracts`](https://github.com/CoreLinkPlatform/api-contracts). The mock must identify immutable contract provenance and must not hand-invent a parallel API.

## Planned responsibilities

- deterministic HTTP success/validation/auth/authorization/conflict scenarios;
- strict tenant-isolation and insufficient-scope failures;
- Device/Command scenarios aligned with accepted public contract revisions;
- telemetry/location/event/webhook scenarios only as their versioned contracts are accepted;
- duplicate, retry/replay, timeout and recovery fixtures;
- synthetic data only—no production/customer data;
- reproducible local/CI package or container;
- SDK/CLI/MCP conformance against the same scenario set.

## Non-goals

- pretending mock behavior is runtime Product Acceptance;
- exposing provider-specific APIs or identifiers as CoreLink contracts;
- claiming Stable support before packaged conformance/release gates pass;
- copying private runtime behavior that is not present in reviewed contracts.

## Backlog

- [MOCK-01](https://github.com/CoreLinkPlatform/mock-server/issues/2) — contract-driven HTTP mock baseline.
- [MOCK-02](https://github.com/CoreLinkPlatform/mock-server/issues/3) — deterministic auth/tenant/command/telemetry/webhook/failure scenarios.
- [MOCK-03](https://github.com/CoreLinkPlatform/mock-server/issues/4) — publish artifact and run consumer conformance in CI.

## Related documentation

- [CoreLink developer docs](https://github.com/CoreLinkPlatform/developer-docs)
- [Contract compatibility matrix](https://github.com/CoreLinkPlatform/api-contracts/blob/main/docs/compatibility-matrix.md)
- [Organization maturity inventory](https://github.com/CoreLinkPlatform/.github/blob/main/REPOSITORY_MATURITY.md)

Installation instructions will be added only when a real reproducible artifact exists.