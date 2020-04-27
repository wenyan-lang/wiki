You can now run wenyan-lang as normal Javscript scripts right in your html.

[**Check out the demo**](https://jsfiddle.net/antfu/u532ny49/)

## Installation

Add the following script in the `<head>` of your html file.

```html
<script src='https://unpkg.com/@wenyan/runtime'></script>
```

That's all, you are good to go!

## Usage

To use wenyan in script, you **HAVE TO** specify `type="application/wenyan"` for the `<script>` tag. For example:

```html
<script type="application/wenyan">
吾有一數。曰三。名之曰「甲」。
為是「甲」遍。
  吾有一言。曰「「問天地好在。」」。書之。
云云。
</script>
```

### Scoped script

By default, all the variables in wenyan will be exposed globally. For the previous example, `甲` is accessible by `window.甲`. If you do not want to mess up your globals, you can specify the `scoped` attr.

```html
<script type="application/wenyan" scoped>
吾有一數。曰三。名之曰「甲」。
</script>
```

### Remote scripts

You can import remote scripts as you will do for Javascript.

```html
<script type="application/wenyan" src="https://raw.githubusercontent.com/LingDong-/wenyan-lang/master/examples/fizzbuzz.wy"></script>
```

### Outputting Hanzi

By default, it will convert numbers and bools to hanzi. If you want to output raw numbers, you can specify `outputHanzi="false"` in attr of the script tag.

```html
<script type="application/wenyan" outputHanzi="false">
吾有一數。曰三。書之。
</script>
```

### DOM Hacks

There are some hacks examples you can do to access the DOM and browser APIs.

```html
<script type="application/wenyan">
施「((title)=>document.title=title)」於「「文言」」。
施「((text)=>document.body.innerText=text)」於「「問天地好在。」」。
</script>
```

### Import [wyg Packages](https://github.com/wenyan-lang/wenyan/wiki/Packages-Manager)

You can import packages from [wyg](https://github.com/wenyan-lang/wenyan/wiki/Packages-Manager) by following [this instruction](https://github.com/wenyan-lang/wenyan/wiki/Packages-Manager#direct-import).
