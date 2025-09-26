# NotificationUpdateDiscordRequest

## Example Usage

```typescript
import { NotificationUpdateDiscordRequest } from "dokploy/models/operations";

let value: NotificationUpdateDiscordRequest = {
  notificationId: "<id>",
  discordId: "<id>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `appBuildError`    | *boolean*          | :heavy_minus_sign: | N/A                |
| `databaseBackup`   | *boolean*          | :heavy_minus_sign: | N/A                |
| `dokployRestart`   | *boolean*          | :heavy_minus_sign: | N/A                |
| `name`             | *string*           | :heavy_minus_sign: | N/A                |
| `appDeploy`        | *boolean*          | :heavy_minus_sign: | N/A                |
| `dockerCleanup`    | *boolean*          | :heavy_minus_sign: | N/A                |
| `webhookUrl`       | *string*           | :heavy_minus_sign: | N/A                |
| `notificationId`   | *string*           | :heavy_check_mark: | N/A                |
| `discordId`        | *string*           | :heavy_check_mark: | N/A                |
| `adminId`          | *string*           | :heavy_minus_sign: | N/A                |