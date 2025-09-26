# NotificationCreateEmailRequest

## Example Usage

```typescript
import { NotificationCreateEmailRequest } from "dokploy/models/operations";

let value: NotificationCreateEmailRequest = {
  appBuildError: false,
  databaseBackup: true,
  dokployRestart: true,
  name: "<value>",
  appDeploy: false,
  dockerCleanup: true,
  smtpServer: "<value>",
  smtpPort: 5296.17,
  username: "Warren_Bode30",
  password: "_Zxu4oWSujorkpz",
  fromAddress: "<value>",
  toAddresses: [],
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
| `smtpServer`       | *string*           | :heavy_check_mark: | N/A                |
| `smtpPort`         | *number*           | :heavy_check_mark: | N/A                |
| `username`         | *string*           | :heavy_check_mark: | N/A                |
| `password`         | *string*           | :heavy_check_mark: | N/A                |
| `fromAddress`      | *string*           | :heavy_check_mark: | N/A                |
| `toAddresses`      | *string*[]         | :heavy_check_mark: | N/A                |