---
url: https://raw.githubusercontent.com/dsherret/ts-morph/latest/docs/manipulation/formatting.md
title: "Formatting"
description: ""
access_date: 2026-08-03T19:45:57.072Z
current_date: 2026-08-03T19:45:57.072Z
---

## Formatting

Sometimes you might encounter code that looks terrible. For example:

<!-- dprint-ignore -->
```ts
// BadlyFormattedFile.ts
var myVariable     :      string |    number;
function myFunction(param    : string){
return "";
}
```

Automatically format the text of this file by calling format text on it:

```ts
sourceFile.formatText();
// or provide optional formatting settings
sourceFile.formatText({
  placeOpenBraceOnNewLineForFunctions: true,
});
```

This will run the source file's text through the TypeScript compiler's formatting API, which will change the source file to contain the following text:

```ts
// BadlyFormattedFile.ts (not anymore!)
var myVariable: string | number;
function myFunction(param: string) {
  return "";
}
```

### Individual Nodes

Individual nodes can also be formatted. For example, say you have a file that looks like this:

<!-- dprint-ignore -->
```ts
// file.ts
export class MyClass {
    prop  !  : string   ;

    myMethod(    example: string    ) {
  console.log(    example    );
    }
}
```

You can select down to the specific node you want to format:

```ts
project.getSourceFileOrThrow("file.ts")
  .getClassOrThrow("MyClass")
  .getInstanceMethodOrThrow("myMethod")
  .getStatements()[0]
  .formatText();
```

Which would selectively only format the first statement in the method:

<!-- dprint-ignore -->
```ts
// file.ts
export class MyClass {
    prop  !  : string   ;

    myMethod(    example: string    ) {
        console.log(example);
    }
}
```
