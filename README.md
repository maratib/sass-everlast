# Sass everlast

### Preprocessor

Sass is a preprocessor, it compiles your SASS files into CSS.

> It greatly simplifies the process of writing complex CSS
> using (Variables, Nesting, Mixins, Functions, Partials and Inheritance).

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

### Functions

```css
$total: 8;
$col: 3;

@function column-width() {
  @return percentage($col/$total);
}

//width: column-width();
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

### Tips for VSCode

_*Useful extensions for sass*_

[SCSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-scss)

[SCSS Everywhere](https://marketplace.visualstudio.com/items?itemName=gencer.html-slim-scss-css-class-completion)

[Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

_*References*_

[Sass-Everlast](https://github.com/maratib/sass-everlast)
