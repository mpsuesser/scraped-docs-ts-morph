---
url: https://raw.githubusercontent.com/dsherret/ts-morph/latest/docs/navigation/ambient-modules.md
title: "Ambient Modules"
description: ""
access_date: 2026-08-03T18:56:37.604Z
current_date: 2026-08-03T18:56:37.604Z
---

## Ambient Modules

The ambient module symbols can be retrieved by calling:

```ts
const ambientModules = project.getAmbientModules();
```

This will return the ambient modules resolved by the compiler (ex. ambient modules in `@types` or `node_modules`).

### Getting by name

Get an ambient module symbol based on its name:

```ts
const jQuerySymbol = project.getAmbientModule("jquery"); // returns: Symbol | undefined
const momentSymbol = project.getAmbientModuleOrThrow("moment"); // returns: Symbol
```
