# Sass everlast

### Preprocessor

Sass is a preprocessor, it compiles your SASS files into CSS.

> It greatly simplifies the process of writing complex CSS
> using Variables, Nesting, Mixins, Partials and Inheritance.

### Variables

```css
// defining variable
$primary-color: #333;

// usage example
// color: $primary-color;
```

### Nesting

<table width="100%"><tr>
<td>
<pre>
//SCSS
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
   li { display: inline-block; }
}
</pre>
</td>
<td>
<pre>
//CSS
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
nav li {
  display: inline-block;
}
</pre>
</td>
</tr></table>

### Partials

Partials are files contain little snippets of CSS, use to brake a large CSS into small manageable and relevant chunks of code.

```css
//A Partial file name starts with underscore '_',
//so that sass compiler will not compile it to its own css file.
//example _variables.scss

//how to import above file (notice no underscore and extension used).
@import "variables";
```

### Modules

...

### Mixins

`@mixin and @include`

```css
@mixin transform($property) {
  -webkit-transform: $property;
  -ms-transform: $property;
  transform: $property;
}

.box {
  @include transform(rotate(30deg));
}
```

### Extend/Inheritance

```css
/* This CSS will print because %message-shared is extended in .message class. */
%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.message {
  @extend %message-shared;
}
```

### Operators

Sass has math operators like `+,-,*,/,%`

```css
article[role="main"] {
  float: left;
  width: 600px / 960px * 100%;
}
```

### A typical top-level directory layout

```

sass
│ README.md
| main.scss
│
└───utilities/
│ │ _variables.scss
│ │ _mixins.scss
| | _functions.scss
│
└───base/
│ │ _reset.scss // Reset/normalize
│ │ _typography.scss // Typography rules
│
└───components/
│ │ _button.scss
│ │ _slider.scss
| | ...
│
└───layout/
│ │ _navigation.scss
│ │ _header.scss
| | _footer.scss
| | _sidebar.scss
| | _forms.scss
| | _grid.scss
| | ...
│
└───pages/
│ │ _home.scss
│ │ _about.scss
| | _contact.scss
│
└───themes/
│ │ _theme.scss
│ │ _admin.scss
│
└───vendors/
│ │ _bootstrap.scss
│ │ _jquery-ui.scss
|
|
```

It does not mean you have to follow everything as it is, you might not need some of them from the above structure

**Tips for VS Code**

**Useful extensions**

[SCSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-scss)

[SCSS Everywhere](https://marketplace.visualstudio.com/items?itemName=gencer.html-slim-scss-css-class-completion)

[SCSS Lint](https://marketplace.visualstudio.com/items?itemName=adamwalzer.scss-lint)
