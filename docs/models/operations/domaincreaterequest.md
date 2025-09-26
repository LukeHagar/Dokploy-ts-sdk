# DomainCreateRequest

## Example Usage

```typescript
import { DomainCreateRequest } from "dokploy/models/operations";

let value: DomainCreateRequest = {
  host: "dim-tinderbox.name",
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `host`                                                                                           | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `path`                                                                                           | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `port`                                                                                           | *number*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `https`                                                                                          | *boolean*                                                                                        | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `applicationId`                                                                                  | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `certificateType`                                                                                | [operations.DomainCreateCertificateType](../../models/operations/domaincreatecertificatetype.md) | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `composeId`                                                                                      | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `serviceName`                                                                                    | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `domainType`                                                                                     | [operations.DomainCreateDomainType](../../models/operations/domaincreatedomaintype.md)           | :heavy_minus_sign:                                                                               | N/A                                                                                              |