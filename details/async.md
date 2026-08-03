---
url: https://raw.githubusercontent.com/dsherret/ts-morph/latest/docs/details/async.md
title: "Async"
description: ""
access_date: 2026-08-03T19:02:39.365Z
current_date: 2026-08-03T19:02:39.365Z
---

## Async

Certain nodes in TypeScript can have an `async` keyword modifier.

### Is async

A node can be tested if it's async using the `isAsync()` method:

```ts
functionDeclaration.isAsync(); // returns: boolean
```

### `async` keyword

Get the `async` keyword if it exists:

```ts
functionDeclaration.getAsyncKeyword();
```

### Set async

Set if the declaration is async using `setIsAsync`:

```ts
functionDeclaration.setIsAsync(true);
```
