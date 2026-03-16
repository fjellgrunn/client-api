# Usage Guide

Comprehensive usage guidance for `@fjell/client-api`.

## Installation

```bash
npm install @fjell/client-api
```

## API Highlights

- `createPItemApi` and `createCItemApi`
- Client API type contracts (`ClientApi`, `ClientApiOptions`, `PItemApi`, `CItemApi`)
- `FjellHttpError` helpers and HTTP wrapper exports

## Quick Example

```ts
import { createPItemApi } from "@fjell/client-api";

const widgetsApi = createPItemApi({
  baseUrl: "/api/widgets",
  headers: { "content-type": "application/json" },
});

const widget = await widgetsApi.load({ pk: "widget#123", sk: "meta" });
```

## Model Consumption Rules

1. Import from the package root (`@fjell/client-api`) instead of deep-internal paths unless explicitly documented.
2. Keep usage aligned with exported public symbols listed in this guide.
3. Prefer explicit typing at package boundaries so generated code remains robust during upgrades.
4. Keep error handling deterministic and map infrastructure failures into domain-level errors.
5. Co-locate integration wrappers in your app so model-generated code has one canonical entry point.

## Best Practices

- Keep examples and abstractions consistent with existing Fjell package conventions.
- Favor composable wrappers over one-off inline integration logic.
- Add targeted tests around generated integration code paths.
