# DestinationUpdateRequest

## Example Usage

```typescript
import { DestinationUpdateRequest } from "dokploy/models/operations";

let value: DestinationUpdateRequest = {
  name: "<value>",
  accessKey: "<value>",
  bucket: "<value>",
  region: "<value>",
  endpoint: "<value>",
  secretAccessKey: "<value>",
  destinationId: "<id>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `name`             | *string*           | :heavy_check_mark: | N/A                |
| `accessKey`        | *string*           | :heavy_check_mark: | N/A                |
| `bucket`           | *string*           | :heavy_check_mark: | N/A                |
| `region`           | *string*           | :heavy_check_mark: | N/A                |
| `endpoint`         | *string*           | :heavy_check_mark: | N/A                |
| `secretAccessKey`  | *string*           | :heavy_check_mark: | N/A                |
| `destinationId`    | *string*           | :heavy_check_mark: | N/A                |
| `serverId`         | *string*           | :heavy_minus_sign: | N/A                |