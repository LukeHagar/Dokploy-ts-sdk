# MysqlChangeStatusRequest

## Example Usage

```typescript
import { MysqlChangeStatusRequest } from "dokploy/models/operations";

let value: MysqlChangeStatusRequest = {
  mysqlId: "<id>",
  applicationStatus: "done",
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `mysqlId`                                                                                                      | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `applicationStatus`                                                                                            | [operations.MysqlChangeStatusApplicationStatus](../../models/operations/mysqlchangestatusapplicationstatus.md) | :heavy_check_mark:                                                                                             | N/A                                                                                                            |