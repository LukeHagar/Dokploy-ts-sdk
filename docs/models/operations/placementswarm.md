# PlacementSwarm

## Example Usage

```typescript
import { PlacementSwarm } from "dokploy/models/operations";

let value: PlacementSwarm = {};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `constraints`                                                    | *string*[]                                                       | :heavy_minus_sign:                                               | N/A                                                              |
| `preferences`                                                    | [operations.Preference](../../models/operations/preference.md)[] | :heavy_minus_sign:                                               | N/A                                                              |
| `maxReplicas`                                                    | *number*                                                         | :heavy_minus_sign:                                               | N/A                                                              |
| `platforms`                                                      | [operations.Platform](../../models/operations/platform.md)[]     | :heavy_minus_sign:                                               | N/A                                                              |