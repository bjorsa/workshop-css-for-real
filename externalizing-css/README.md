# 3. Externalizing CSS

In this short exercise we are going to examine how to move our CSS rules into an external file and still use those rules from the same HTML document. This is simply done by creating a CSS file, lets call it _main.css_, moving our rules into it and then referencing it from our HTML head element using a link tag as follows

```html
<html>
  <head>
    <title>...</title>
    .
    .
    <link rel="stylesheet" href="main.css">
    .
    .
  <head>
  <body>

  </body>
</html>
```

Strictly speaking, the link tag can go inside either the head or the body element of the html page, but is most commonly found inside the head tag.

More about the link tag: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link

## The task

Move the CSS rule declarations into an external file and reference it from the HTML page. Verify that the styles have been applied.
