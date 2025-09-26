# PortCreateRequest

## Example Usage

```typescript
import { PortCreateRequest } from "dokploy/models/operations";

let value: PortCreateRequest = {
  publishedPort: 1244.1,
  targetPort: 6872.55,
  applicationId: "<id>",
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `publishedPort`                                                                | *number*                                                                       | :heavy_check_mark:                                                             | N/A                                                                            |
| `targetPort`                                                                   | *number*                                                                       | :heavy_check_mark:                                                             | N/A                                                                            |
| `protocol`                                                                     | [operations.PortCreateProtocol](../../models/operations/portcreateprotocol.md) | :heavy_minus_sign:                                                             | N/A                                                                            |
| `applicationId`                                                                | *string*                                                                       | :heavy_check_mark:                                                             | N/A                                                                            |