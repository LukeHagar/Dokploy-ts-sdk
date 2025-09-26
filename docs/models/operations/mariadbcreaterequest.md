# MariadbCreateRequest

## Example Usage

```typescript
import { MariadbCreateRequest } from "dokploy/models/operations";

let value: MariadbCreateRequest = {
  name: "<value>",
  appName: "<value>",
  databaseRootPassword: "<value>",
  projectId: "<id>",
  databaseName: "<value>",
  databaseUser: "<value>",
  databasePassword: "<value>",
};
```

## Fields

| Field                  | Type                   | Required               | Description            |
| ---------------------- | ---------------------- | ---------------------- | ---------------------- |
| `name`                 | *string*               | :heavy_check_mark:     | N/A                    |
| `appName`              | *string*               | :heavy_check_mark:     | N/A                    |
| `dockerImage`          | *string*               | :heavy_minus_sign:     | N/A                    |
| `databaseRootPassword` | *string*               | :heavy_check_mark:     | N/A                    |
| `projectId`            | *string*               | :heavy_check_mark:     | N/A                    |
| `description`          | *string*               | :heavy_minus_sign:     | N/A                    |
| `databaseName`         | *string*               | :heavy_check_mark:     | N/A                    |
| `databaseUser`         | *string*               | :heavy_check_mark:     | N/A                    |
| `databasePassword`     | *string*               | :heavy_check_mark:     | N/A                    |
| `serverId`             | *string*               | :heavy_minus_sign:     | N/A                    |