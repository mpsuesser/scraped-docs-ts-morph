---
url: https://raw.githubusercontent.com/dsherret/ts-morph/latest/docs/details/literals.md
title: "Literals"
description: ""
access_date: 2026-08-03T17:27:45.897Z
current_date: 2026-08-03T17:27:45.897Z
---

## Literals

Literals:

- `StringLiteral` (ex. `"some string"`)
- `NumericLiteral` (ex. `5`, `10.53`)
- `TrueLiteral` / `FalseLiteral` (ex. `true` / `false`)
- `NoSubstitutionTemplateLiteral` (ex. `` `some string` ``)
- `RegularExpressionLiteral` (ex. `/pattern/gi`)

Methods:

- `.getLiteralValue()` - Returns the string, number, boolean, or RegExp value.
- `.setLiteralValue(...)` - Allows setting the literal value.
- `isTerminated()` - If the literal is terminated.
- `hasExtendedUnicodeEscape()` - If the literal has a unicode escape (ex. `\u{20bb7}`)
