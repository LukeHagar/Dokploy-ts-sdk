# AuthUpdateRequest

## Example Usage

```typescript
import { AuthUpdateRequest } from "dokploy/models/operations";

let value: AuthUpdateRequest = {
  email: "Sam56@yahoo.com",
  password: "J5mRzNG9iBEmeW3",
};
```

## Fields

| Field                                            | Type                                             | Required                                         | Description                                      |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| `id`                                             | *string*                                         | :heavy_minus_sign:                               | N/A                                              |
| `email`                                          | *string*                                         | :heavy_check_mark:                               | N/A                                              |
| `password`                                       | *string*                                         | :heavy_check_mark:                               | N/A                                              |
| `rol`                                            | [operations.Rol](../../models/operations/rol.md) | :heavy_minus_sign:                               | N/A                                              |
| `image`                                          | *string*                                         | :heavy_minus_sign:                               | N/A                                              |
| `secret`                                         | *string*                                         | :heavy_minus_sign:                               | N/A                                              |
| `token`                                          | *string*                                         | :heavy_minus_sign:                               | N/A                                              |
| `is2FAEnabled`                                   | *boolean*                                        | :heavy_minus_sign:                               | N/A                                              |
| `createdAt`                                      | *string*                                         | :heavy_minus_sign:                               | N/A                                              |
| `resetPasswordToken`                             | *string*                                         | :heavy_minus_sign:                               | N/A                                              |
| `resetPasswordExpiresAt`                         | *string*                                         | :heavy_minus_sign:                               | N/A                                              |
| `confirmationToken`                              | *string*                                         | :heavy_minus_sign:                               | N/A                                              |
| `confirmationExpiresAt`                          | *string*                                         | :heavy_minus_sign:                               | N/A                                              |