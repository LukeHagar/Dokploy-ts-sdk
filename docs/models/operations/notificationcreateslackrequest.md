# NotificationCreateSlackRequest

## Example Usage

```typescript
import { NotificationCreateSlackRequest } from "dokploy/models/operations";

let value: NotificationCreateSlackRequest = {
  appBuildError: true,
  databaseBackup: true,
  dokployRestart: false,
  name: "<value>",
  appDeploy: false,
  dockerCleanup: false,
  webhookUrl: "https://average-scorpion.net",
  channel: "<value>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `appBuildError`    | *boolean*          | :heavy_check_mark: | N/A                |
| `databaseBackup`   | *boolean*          | :heavy_check_mark: | N/A                |
| `dokployRestart`   | *boolean*          | :heavy_check_mark: | N/A                |
| `name`             | *string*           | :heavy_check_mark: | N/A                |
| `appDeploy`        | *boolean*          | :heavy_check_mark: | N/A                |
| `dockerCleanup`    | *boolean*          | :heavy_check_mark: | N/A                |
| `webhookUrl`       | *string*           | :heavy_check_mark: | N/A                |
| `channel`          | *string*           | :heavy_check_mark: | N/A                |