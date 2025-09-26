# RedisChangeStatusRequest

## Example Usage

```typescript
import { RedisChangeStatusRequest } from "dokploy/models/operations";

let value: RedisChangeStatusRequest = {
  redisId: "<id>",
  applicationStatus: "idle",
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `redisId`                                                                                                      | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `applicationStatus`                                                                                            | [operations.RedisChangeStatusApplicationStatus](../../models/operations/redischangestatusapplicationstatus.md) | :heavy_check_mark:                                                                                             | N/A                                                                                                            |