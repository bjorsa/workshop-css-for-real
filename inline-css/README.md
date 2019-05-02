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

Please add some nice background color to the _section_-element in the html document. If you feel up to it, experimenting with adding some additional style declarations.

## The solution

As described above I added a _style_-attribute to the _section_ opening tag as follows:

```html
<section style="background: #EC9A29;"/>
```

Note that this approach is not the recommended way for several reasons.

* First of all, it is not secure, allowing styles to be specified inline on elements can have adverse security implications. Exactly how to prevent this and to what degree this matters is beyond the scope of this workshop. If you want to know more, please have a read at: https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.md
* No reuse is possible if you apply styles directly to the elements of your HTML page. Every time the same style needs to be applied you need to rewrite the same set of CSS declarations.
* It is verbose, often multiple CSS declarations are needed to get the desired effect, applying these every time directly in the HTML file obscures the structure of the document.
* It is very hard to maintain. Changing some aspect of your web page might involve finding the relevant styles on 100s of separate elements, at least when your project is starting to grow.

In the next exercise we will explore another way of including the CSS into the HTML page.