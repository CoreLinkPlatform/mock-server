# CoreLink Mock Server

The future local and CI-compatible simulation of CoreLink public APIs and
events.

## Current status

This repository is a scaffold; it does not yet expose an HTTP server, event
emulator or packaged command. The OpenAPI and AsyncAPI source files in
`api-contracts` are also currently empty, so code generation cannot begin yet.

## Intended use

- Let SDK and integration teams develop against deterministic, versioned API
  behavior.
- Simulate authentication and strict tenant isolation without requiring a full
  platform environment.
- Provide success, validation, authorization, conflict, rate-limit and
  asynchronous command/event fixtures.
- Run in CI with no production credentials or provider dependencies.

## Compatibility rules

The mock server must implement only documented public contracts. Each release
should state the exact OpenAPI/AsyncAPI version it supports and include
fixtures for boundary and failure behavior, not just happy paths.
