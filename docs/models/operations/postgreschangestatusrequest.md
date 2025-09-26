# PostgresChangeStatusRequest

## Example Usage

```typescript
import { PostgresChangeStatusRequest } from "dokploy/models/operations";

let value: PostgresChangeStatusRequest = {
  postgresId: "<id>",
  applicationStatus: "idle",
};
```

## Fields

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `postgresId`                                                                                                         | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `applicationStatus`                                                                                                  | [operations.PostgresChangeStatusApplicationStatus](../../models/operations/postgreschangestatusapplicationstatus.md) | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |