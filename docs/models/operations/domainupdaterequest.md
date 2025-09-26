# DomainUpdateRequest

## Example Usage

```typescript
import { DomainUpdateRequest } from "dokploy/models/operations";

let value: DomainUpdateRequest = {
  host: "tinted-squid.net",
  domainId: "<id>",
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `host`                                                                                           | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `path`                                                                                           | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `port`                                                                                           | *number*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `https`                                                                                          | *boolean*                                                                                        | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `certificateType`                                                                                | [operations.DomainUpdateCertificateType](../../models/operations/domainupdatecertificatetype.md) | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `serviceName`                                                                                    | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `domainType`                                                                                     | [operations.DomainUpdateDomainType](../../models/operations/domainupdatedomaintype.md)           | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `domainId`                                                                                       | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |