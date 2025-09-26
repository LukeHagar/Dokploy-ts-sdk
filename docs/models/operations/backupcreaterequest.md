# BackupCreateRequest

## Example Usage

```typescript
import { BackupCreateRequest } from "dokploy/models/operations";

let value: BackupCreateRequest = {
  schedule: "<value>",
  prefix: "<value>",
  destinationId: "<id>",
  database: "<value>",
  databaseType: "mysql",
};
```

## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `schedule`                                                         | *string*                                                           | :heavy_check_mark:                                                 | N/A                                                                |
| `enabled`                                                          | *boolean*                                                          | :heavy_minus_sign:                                                 | N/A                                                                |
| `prefix`                                                           | *string*                                                           | :heavy_check_mark:                                                 | N/A                                                                |
| `destinationId`                                                    | *string*                                                           | :heavy_check_mark:                                                 | N/A                                                                |
| `database`                                                         | *string*                                                           | :heavy_check_mark:                                                 | N/A                                                                |
| `mariadbId`                                                        | *string*                                                           | :heavy_minus_sign:                                                 | N/A                                                                |
| `mysqlId`                                                          | *string*                                                           | :heavy_minus_sign:                                                 | N/A                                                                |
| `postgresId`                                                       | *string*                                                           | :heavy_minus_sign:                                                 | N/A                                                                |
| `mongoId`                                                          | *string*                                                           | :heavy_minus_sign:                                                 | N/A                                                                |
| `databaseType`                                                     | [operations.DatabaseType](../../models/operations/databasetype.md) | :heavy_check_mark:                                                 | N/A                                                                |