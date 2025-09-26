# MongoCreateRequest

## Example Usage

```typescript
import { MongoCreateRequest } from "dokploy/models/operations";

let value: MongoCreateRequest = {
  name: "<value>",
  appName: "<value>",
  projectId: "<id>",
  databaseUser: "<value>",
  databasePassword: "<value>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `name`             | *string*           | :heavy_check_mark: | N/A                |
| `appName`          | *string*           | :heavy_check_mark: | N/A                |
| `dockerImage`      | *string*           | :heavy_minus_sign: | N/A                |
| `projectId`        | *string*           | :heavy_check_mark: | N/A                |
| `description`      | *string*           | :heavy_minus_sign: | N/A                |
| `databaseUser`     | *string*           | :heavy_check_mark: | N/A                |
| `databasePassword` | *string*           | :heavy_check_mark: | N/A                |
| `serverId`         | *string*           | :heavy_minus_sign: | N/A                |