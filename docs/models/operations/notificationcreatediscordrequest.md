# NotificationCreateDiscordRequest

## Example Usage

```typescript
import { NotificationCreateDiscordRequest } from "dokploy/models/operations";

let value: NotificationCreateDiscordRequest = {
  appBuildError: false,
  databaseBackup: true,
  dokployRestart: false,
  name: "<value>",
  appDeploy: true,
  dockerCleanup: false,
  webhookUrl: "https://weary-mom.org",
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