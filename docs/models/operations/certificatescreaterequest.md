# CertificatesCreateRequest

## Example Usage

```typescript
import { CertificatesCreateRequest } from "dokploy/models/operations";

let value: CertificatesCreateRequest = {
  name: "<value>",
  certificateData: "<value>",
  privateKey: "<value>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `certificateId`    | *string*           | :heavy_minus_sign: | N/A                |
| `name`             | *string*           | :heavy_check_mark: | N/A                |
| `certificateData`  | *string*           | :heavy_check_mark: | N/A                |
| `privateKey`       | *string*           | :heavy_check_mark: | N/A                |
| `certificatePath`  | *string*           | :heavy_minus_sign: | N/A                |
| `autoRenew`        | *boolean*          | :heavy_minus_sign: | N/A                |
| `adminId`          | *string*           | :heavy_minus_sign: | N/A                |
| `serverId`         | *string*           | :heavy_minus_sign: | N/A                |