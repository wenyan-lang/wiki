[wyg](https://github.com/wenyan-lang/wyg)(wenyan-get, or 文淵閣) is a package manager for wenyan-lang. Just like [`npm`](https://www.npmjs.com/) for Node.js or [`pip`](https://pip.pypa.io/en/stable/) for Python.

## Install 

```bash
npm i -g @wenyan/wyg
```

## Usage

```bash
wyg i ziyue
```

Chinese names are also acceptable

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