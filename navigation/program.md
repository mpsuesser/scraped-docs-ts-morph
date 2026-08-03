---
url: https://raw.githubusercontent.com/dsherret/ts-morph/latest/docs/navigation/program.md
title: "Program"
description: ""
access_date: 2026-08-03T19:10:24.072Z
current_date: 2026-08-03T19:10:24.072Z
---

## Program

Get the program by calling:

```ts
const program = project.getProgram();
```

### Underlying compiler object

The underlying `ts.Program` can be retrieved as follows:

```ts
const tsProgram = program.compilerObject;
```

**Warning:** The underlying compiler object will be discared whenever manipulation occurs. For that reason, only hold onto the underlying compiler object between manipulations.

### Use

Generally you won't need to use the program because most of the functionality is exposed as methods on other objects.
