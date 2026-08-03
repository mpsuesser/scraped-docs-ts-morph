---
url: https://raw.githubusercontent.com/dsherret/ts-morph/latest/docs/details/modifiers.md
title: "Modifiers"
description: ""
access_date: 2026-08-03T17:27:45.897Z
current_date: 2026-08-03T17:27:45.897Z
---

## Modifiers

Modifiers are nodes that modify other nodes. For example, the `private` keyword is a modifier that changes the scope of a method on a class.

Only certain nodes can have modifiers and they will have these functions.

### Getting all modifiers

```ts
functionDeclaration.getModifiers();
```

### Getting first modifier by syntax kind

Use `getFirstModifierByKind(syntaxKind: SyntaxKind);`.

```ts
functionDeclaration.getFirstModifierByKind(SyntaxKind.AsyncKeyword);
```

### Telling if has a modifier

```ts
functionDeclaration.hasModifier(SyntaxKind.AsyncKeyword); // returns: boolean
```

### Toggle modifier

Toggles a modifier on or off:

```ts
functionDeclaration.toggleModifier("async");
functionDeclaration.toggleModifier("async", false); // or explicit toggle
```
