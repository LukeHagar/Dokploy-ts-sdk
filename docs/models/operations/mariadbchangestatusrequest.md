# MariadbChangeStatusRequest

## Example Usage

```typescript
import { MariadbChangeStatusRequest } from "dokploy/models/operations";

let value: MariadbChangeStatusRequest = {
  mariadbId: "<id>",
  applicationStatus: "done",
};
```

## Fields

| Field                                                                                                              | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `mariadbId`                                                                                                        | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `applicationStatus`                                                                                                | [operations.MariadbChangeStatusApplicationStatus](../../models/operations/mariadbchangestatusapplicationstatus.md) | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |