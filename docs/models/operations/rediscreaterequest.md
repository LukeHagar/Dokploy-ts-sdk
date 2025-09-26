# RedisCreateRequest

## Example Usage

```typescript
import { RedisCreateRequest } from "dokploy/models/operations";

let value: RedisCreateRequest = {
  name: "<value>",
  appName: "<value>",
  databasePassword: "<value>",
  projectId: "<id>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `name`             | *string*           | :heavy_check_mark: | N/A                |
| `appName`          | *string*           | :heavy_check_mark: | N/A                |
| `databasePassword` | *string*           | :heavy_check_mark: | N/A                |
| `dockerImage`      | *string*           | :heavy_minus_sign: | N/A                |
| `projectId`        | *string*           | :heavy_check_mark: | N/A                |
| `description`      | *string*           | :heavy_minus_sign: | N/A                |
| `serverId`         | *string*           | :heavy_minus_sign: | N/A                |