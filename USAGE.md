<!-- Start SDK Example Usage [usage] -->
```typescript
import { Dokploy } from "dokploy";

const dokploy = new Dokploy({
  authorization: process.env["DOKPLOY_AUTHORIZATION"] ?? "",
});

async function run() {
  const result = await dokploy.admin.getOne();

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->