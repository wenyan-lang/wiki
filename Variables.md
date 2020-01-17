## Type

| Keyword | Explanation | Examples |
| --- | --- | --- |
| `數` |` number` type, which can be a floating point or an integer type|`三千二百零一`，`二〇二〇`|
| `言` | `string` type, which can be an empty string|`「「君子好逑」」`,`『予观夫巴陵胜状』`|
| `爻` | `boolean` type is a boolean type with only two values |` 陰`, `陽` |
| `列` |` array` type is an array type | `...` |
| `物` | `object` type, defines the object |` ... `|
| `元` | `auto type`, you can reverse the type |` ... `|

### Expressions that declare variables

```wenyan
吾有[N][type]。曰[value1]。曰[value2]...曰[valueN]。名之曰[name1]曰[name2]....[nameN]
```

### Common Example

1. 數 言 爻
    * 今/吾有一數/言/爻，曰三/「「问天地好在」」/陰，名之曰「甲」
    * 吾有三數。曰一。曰三。曰五。名之曰「甲」曰「乙」曰「丙」。
2. 元
    * 今/吾有一元，曰三/「「问天地好在」」/陰，名之曰「甲」
3. 列
    * 今/吾有一列，曰「甲」。充「甲」以四。以二。
4. 物
    * 今/吾有一物。名之曰「甲」。其物如是。物之「「乙」」者。數曰三。物之「「丙」」者。言曰「「丁」」。是謂「甲」之物也

> 💡 `今` is compiled to `var name = this.name = value` in Javascript

### Simplified writing

```wenyan
有[type][value]。名之曰[name]

有數五十。名之曰「大衍」。
```

### Reassign

```wenyan
昔之[before]，今[after]是也/矣
```

Output:

```js
before = after
```

> 💡 `也` is generally used as the end mark of` 若非` and `若...者'`, if you do not end the code block, use `矣`

## Others

You can use other variables during initialization, such as

```wenyan
吾有一數，曰「甲」，名之曰「乙」
```
Output:

```js
var 乙 = 甲;
```
