# BackupUpdateRequest

## Example Usage

```typescript
import { BackupUpdateRequest } from "dokploy/models/operations";

let value: BackupUpdateRequest = {
  schedule: "<value>",
  prefix: "<value>",
  backupId: "<id>",
  destinationId: "<id>",
  database: "<value>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `schedule`         | *string*           | :heavy_check_mark: | N/A                |
| `enabled`          | *boolean*          | :heavy_minus_sign: | N/A                |
| `prefix`           | *string*           | :heavy_check_mark: | N/A                |
| `backupId`         | *string*           | :heavy_check_mark: | N/A                |
| `destinationId`    | *string*           | :heavy_check_mark: | N/A                |
| `database`         | *string*           | :heavy_check_mark: | N/A                |