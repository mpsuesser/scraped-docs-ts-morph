---
url: https://raw.githubusercontent.com/dsherret/ts-morph/latest/docs/details/initializers.md
title: "Initializers"
description: ""
access_date: 2026-08-03T18:56:37.604Z
current_date: 2026-08-03T18:56:37.604Z
---

## Initializers

### Getting

For example, given the following code:

```ts
const add = function(a: number, b: number) {
  return a + b;
};
```

The initializer can be retrieved in any of these ways:

```ts
variableDeclaration.getInitializer(); // returns: Expression | undefined
variableDeclaration.getInitializerOrThrow(); // returns: Expression
variableDeclaration.getInitializerIfKind(SyntaxKind.FunctionExpression); // returns: Expression | undefined
variableDeclaration.getInitializerIfKindOrThrow(SyntaxKind.FunctionExpression); // returns: Expression
```

### Removing

Use `.removeInitializer()` on the parent node. For example:

```ts
variableDeclaration.removeInitializer();
```

### Setting

Use `.setInitializer(...)`:

```ts
variableDeclaration.setInitializer("2 + 2");
```
