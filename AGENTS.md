# CoreLink Mock Server Agent Context

This repository is part of the CoreLink product.

## Canonical context

Follow `CoreLinkPlatform/product-planning/AGENTS.md`, `PRODUCT_ARCHITECTURE.md`, `GLOSSARY.md`, `STANDARDS.md`, and `architecture/repository-map.yaml`. Public API behavior is normative in `CoreLinkPlatform/api-contracts`.

## Repository responsibility

`mock-server` owns contract-driven mock and conformance behavior for supported CoreLink developer interfaces.

## Boundaries

- Mock behavior must derive from supported contracts and examples, not from undocumented implementation details.
- Do not introduce fields, states, or semantics absent from canonical contracts.
- Keep fixtures synthetic and free of customer secrets or production data.
- Provider-specific implementation details must remain hidden unless explicitly part of an approved diagnostic contract.
- Conformance failures should identify contract mismatches, not silently normalize them away.
