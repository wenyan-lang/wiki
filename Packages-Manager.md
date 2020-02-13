The package manager for wenyan-lang is called [wyg](https://github.com/wenyan-lang/wyg)(wenyan-get, or 文淵閣).

## Install 

```bash
npm i -g @wenyanlang/wyg
```

## Usage

```bash
wyg i ziyue
```

Chinese name is also acceptale

```bash
wyg i 子曰
```

The command above will download the package [`子曰`](https://github.com/antfu/ziyue-wy) to `藏書樓/子曰` of cwd. You can think of `藏書樓` as the wenyan version of `node_modules`. 

> 💡 You may want to include `藏書樓` into your `.gitignore` as well

Then write code and import the package as you always do

```
吾嘗觀「「子曰」」之書。方悟「子曰」之義。

子曰「「巧言令色，鮮矣仁！」」。
```

> 💬 Importing from `藏書樓` is only supported by Wenyan v0.2.2 or above.

### Publish Your Own Packages

Please following [the instruction in wyg-registry](https://github.com/wenyan-lang/wyg-registry).

### Use wyg in browser

You can fetch the package information by

```html
<script src="https://unpkg.com/@wenyanlang/wyg"></script>
```

```js
Wyg.resolve('ziyue')
  .then(({ name, entry, author, repo }) => {
    console.log(name, entry)
  })
```

Output:

```
子曰 https://raw.githubusercontent.com/antfu/ziyue-wy/master/序.wy
```

### Direct import

You can access packages with Urls this format. It will redirect to the package repo's `序.wy` file.

```
https://wyg.wy-lang.org/pkg/<package-name>
```

For example, the following two links are both acceptable.

```
https://wyg.wy-lang.org/pkg/ziyue
https://wyg.wy-lang.org/pkg/子曰
```

If you want to use packages in [Browser Runtime](https://github.com/wenyan-lang/wenyan/wiki/Browser-Runtime), you can import them by:

```html
<script src='https://unpkg.com/@wenyanlang/runtime'></script>

<script type="application/wenyan" src="https://wyg.wy-lang.org/pkg/ziyue"></script>
```
