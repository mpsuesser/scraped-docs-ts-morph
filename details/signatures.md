---
url: https://raw.githubusercontent.com/dsherret/ts-morph/latest/docs/details/signatures.md
title: "Signatures"
description: ""
access_date: 2026-08-03T19:02:39.365Z
current_date: 2026-08-03T19:02:39.365Z
---

## Signatures

### Type Parameters

```ts
const typeParams = signature.getTypeParameters(); // returns: TypeParameter[]
```

### Parameters

```ts
const params = signature.getParameters(); // returns: Symbol[]
```

### Return Type

```ts
const returnType = signature.getReturnType();
```

### Documentation Comments

```ts
const docs = signature.getDocumentationComments();
```

### JS Doc Tags

```ts
const tags = signature.getJsDocTags();
```

### Declaration

```ts
const declaration = signature.getDeclaration();
```
