# AdminAssignPermissionsRequest

## Example Usage

```typescript
import { AdminAssignPermissionsRequest } from "dokploy/models/operations";

let value: AdminAssignPermissionsRequest = {
  userId: "<id>",
  canCreateProjects: true,
  canCreateServices: false,
  canDeleteProjects: false,
  canDeleteServices: false,
  accesedProjects: [
    "<value 1>",
  ],
  accesedServices: [],
  canAccessToTraefikFiles: true,
  canAccessToDocker: false,
  canAccessToAPI: false,
  canAccessToSSHKeys: false,
  canAccessToGitProviders: true,
};
```

## Fields

| Field                     | Type                      | Required                  | Description               |
| ------------------------- | ------------------------- | ------------------------- | ------------------------- |
| `userId`                  | *string*                  | :heavy_check_mark:        | N/A                       |
| `canCreateProjects`       | *boolean*                 | :heavy_check_mark:        | N/A                       |
| `canCreateServices`       | *boolean*                 | :heavy_check_mark:        | N/A                       |
| `canDeleteProjects`       | *boolean*                 | :heavy_check_mark:        | N/A                       |
| `canDeleteServices`       | *boolean*                 | :heavy_check_mark:        | N/A                       |
| `accesedProjects`         | *string*[]                | :heavy_check_mark:        | N/A                       |
| `accesedServices`         | *string*[]                | :heavy_check_mark:        | N/A                       |
| `canAccessToTraefikFiles` | *boolean*                 | :heavy_check_mark:        | N/A                       |
| `canAccessToDocker`       | *boolean*                 | :heavy_check_mark:        | N/A                       |
| `canAccessToAPI`          | *boolean*                 | :heavy_check_mark:        | N/A                       |
| `canAccessToSSHKeys`      | *boolean*                 | :heavy_check_mark:        | N/A                       |
| `canAccessToGitProviders` | *boolean*                 | :heavy_check_mark:        | N/A                       |