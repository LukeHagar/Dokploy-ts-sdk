# MongoChangeStatusRequest

## Example Usage

```typescript
import { MongoChangeStatusRequest } from "dokploy/models/operations";

let value: MongoChangeStatusRequest = {
  mongoId: "<id>",
  applicationStatus: "idle",
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `mongoId`                                                                                                      | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `applicationStatus`                                                                                            | [operations.MongoChangeStatusApplicationStatus](../../models/operations/mongochangestatusapplicationstatus.md) | :heavy_check_mark:                                                                                             | N/A                                                                                                            |