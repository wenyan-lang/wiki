> 🚧 Please note this project is still under heavy development. The API might be changed frequently and this doc any not be always update to date. If you get any questions, feel free to raise an issue.


## Installation

We provide a compiler runs both in Node.js and modern browsers.

### Node.js

You can install the dependence by the following command.

```bash
npm install @wenyanlang/core
```

```js
const Wenyan = require('@wenyanlang/core')
// or
const { compile } = require('@wenyanlang/core')
// or
import { compile } from '@wenyanlang/core'
```

### Browsers

You can add the following line to the head of your html body.

```html
<script src='https://unpkg.com/@wenyanlang/core/index.min.js'></script>
```

```html
<script>
// scripts will be exposed to window.Wenyan
const compiled = Wenyan.compile('吾有一言。曰「「問天地好在。」」。書之。')
</script>
```

## Exposed Functions

- core
  - [compile](#compile)
  - [execute](#execute)

### Execute

[Source](../src/parser.js)

```ts
function execute(source: string, options?: ExecuteOptions)
```

**Parameters**

| Name | Type | Note |
| --- | --- | --- |
| source | string | The Wenyan source code |
| options | object | [Execute Options](#execute-options) |

### Compile

[Source](../src/parser.js)

```ts
function compile(source: string, options?: CompilerOptions)
```

**Parameters**

| Name | Type | Note |
| --- | --- | --- |
| source | string | The Wenyan source code |
| options | object | [Compiler Options](#compiler-options) |

#### Compiler Options

| Fields | Default Value | Type | Note |
| --- | --- | --- | --- |
| lang | `"js"` | `"js" | "py" | "rb"` | Target language, can be  |
| romanizeIdentifiers | `"none"` | `"none" | "pinyin" | "baxter" | "unicode"` | Romanize variable identifiers (e.g. `甲` to `JIA2`), can |
| strict | `false` | `boolean` | Enables static type checking |
| importPaths | [] | `string[]` | Specify the searching dirs for importing, the first match will returned. If you are using `cli`, it will automatically inject `process.cwd()` in to it. |
| allowHttp | `false` | `boolean` | Allow importing from web resources |
| logCallback | console.log | `function` | Redirect verbose debug log | 
| errorCallback | process.exit | `function` | Redirect error log |
| resetVarCnt | `true` | `boolean` | Reset temporary variable counter |


#### Execute Options

Execute Options extends all field in [Compiler Options](#compiler-options)

| Fields | Default Value | Note |
| --- | --- | --- |
| outputHanzi | true | Convert numbers and bools to Hanzi |
| output | `console.log` | Redirect the output if needed |
