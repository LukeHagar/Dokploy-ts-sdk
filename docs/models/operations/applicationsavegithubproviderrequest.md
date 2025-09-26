# ApplicationSaveGithubProviderRequest

## Example Usage

```typescript
import { ApplicationSaveGithubProviderRequest } from "dokploy/models/operations";

let value: ApplicationSaveGithubProviderRequest = {
  applicationId: "<id>",
  owner: "<value>",
  githubId: "<id>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `applicationId`    | *string*           | :heavy_check_mark: | N/A                |
| `repository`       | *string*           | :heavy_minus_sign: | N/A                |
| `branch`           | *string*           | :heavy_minus_sign: | N/A                |
| `owner`            | *string*           | :heavy_check_mark: | N/A                |
| `buildPath`        | *string*           | :heavy_minus_sign: | N/A                |
| `githubId`         | *string*           | :heavy_check_mark: | N/A                |