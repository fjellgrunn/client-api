# @fjell/client-api - Agentic Guide

## Purpose

Client-side API abstractions for contained and primary item operations in Fjell.

This guide is optimized for AI-assisted code generation and integration workflows.

## Documentation

- **[Usage Guide](./usage.md)** - API-oriented usage patterns and model-safe examples
- **[Integration Guide](./integration.md)** - Architecture placement, composition rules, and implementation guidance

## Key Capabilities

- Creates typed client APIs for primary and contained item workflows
- Re-exports standardized HTTP error handling from @fjell/http-api
- Provides registry/instance helpers for client integration patterns

## Installation

```bash
npm install @fjell/client-api
```

## Public API Highlights

- `createPItemApi` and `createCItemApi`
- Client API type contracts (`ClientApi`, `ClientApiOptions`, `PItemApi`, `CItemApi`)
- `FjellHttpError` helpers and HTTP wrapper exports
