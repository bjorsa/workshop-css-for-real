# 1. Inline CSS

In this very first exercise I've prepared a simple HTML file (index.html) that we are going to apply some style to. For completeness sake, this exersize shows you how to apply the style directly to the element. 

Applying CSS directly to an element is done by inserting one or more "CSS declarations" separated by semi colons into the _style_-attribute of the element opening tag.

```html
<h1 style="declaration1; declaration2; ...">
```

A CSS declaration consists of a property followed by a colon and then some value or values. An example of this is the background property which take multiple values as it's input. For now let's use a color name or value.

```html
<h1 style="background: teal;">
```
or
```html
<h1 style="background: #E57737;">
```

If you need some inspiration picking a color theme for your website, go have a look at for instance: https://coolors.co

## The task

Please add some nice background color to the _section_-element in the html document.