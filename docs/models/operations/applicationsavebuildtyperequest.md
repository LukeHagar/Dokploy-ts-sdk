# ApplicationSaveBuildTypeRequest

## Example Usage

```typescript
import { ApplicationSaveBuildTypeRequest } from "dokploy/models/operations";

let value: ApplicationSaveBuildTypeRequest = {
  applicationId: "<id>",
  buildType: "nixpacks",
  dockerContextPath: "<value>",
  dockerBuildStage: "<value>",
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `applicationId`                                                                                              | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `buildType`                                                                                                  | [operations.ApplicationSaveBuildTypeBuildType](../../models/operations/applicationsavebuildtypebuildtype.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `dockerfile`                                                                                                 | *string*                                                                                                     | :heavy_minus_sign:                                                                                           | N/A                                                                                                          |
| `dockerContextPath`                                                                                          | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `dockerBuildStage`                                                                                           | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `publishDirectory`                                                                                           | *string*                                                                                                     | :heavy_minus_sign:                                                                                           | N/A                                                                                                          |