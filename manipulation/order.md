---
url: https://raw.githubusercontent.com/dsherret/ts-morph/latest/docs/manipulation/order.md
title: "Order"
description: ""
access_date: 2026-08-03T19:02:39.365Z
current_date: 2026-08-03T19:02:39.365Z
---

## Order

Change the order of certain nodes using the `.setOrder(newIndex: number)` method.

```ts
const interfaceDeclaration = sourceFile.getInterfaceOrThrow("MyInterface");
interfaceDeclaration.setOrder(2);
```

Notice: Right now this is not supported on comma separated nodes. See [Issue #44](https://github.com/dsherret/ts-morph/issues/44) for more information.
