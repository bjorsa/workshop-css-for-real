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

## The solution

The rules in the style tag were simply copied and pasted into the external file _main.css_ a link element were then added to the head element of the HTML file.

```html
<link rel="stylesheet" href="main.css">
```

This does address some of the downsides that we noted with the two previous approaches of including CSS onto our web page.

* It aleviates the security concern that was present with inline CSS and embedded style elements where abusing the possibility of adding CSS to our page on the fly was possible.
* Sharing CSS rules in multiple HTML files is now only a matter of linking to the same file.
* Maintenance is made easier by having only one place to change.