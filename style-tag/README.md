# 2. The Style Tag

In this exercise we are going to migrate the inline style that we applied to a shared style tag block inside the head tag of our HTML file.

Applying CSS via a style tag is done by creating rules with associated properties that you can apply via CSS selectors.

The following is an example of a rule that specifies that content should be rendered using the color pink inside all of the main tags that appear in a page where this rule apply.

```css
main {
    color: pink;
}
```

More details on the anatomy of rules can be found here: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Basic_rule_syntax

We will also talk at great length about selectors (the tag name part in the rule above) in coming exercises.

In this exercise the rules are defined inside the style-tag element of the HTML file, inside of the head-tag.

```html
<html>
  <head>
    <title>...</title>
    .
    .
    <style>
        main {
            color: gray
        }
    </style>
    .
    .
  <head>
  <body>

  </body>
</html>
```

Technically it is not required to place the style tag under the head element of the HTML page. It is legal to place the style tag under either the head or the body element, although, most commonly it is found residing inside the head element on a page.

If you want to find out more about the style element, please have a read at: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style

Again, this is not the method of choice when applying style to web pages, since allowing inlined CSS like this might have serious security impacts.

## The task

Open up the style-tag/index.html file in your editor and have a look at it. I have added some resized and size optimized images to display where the Colorisious branch offices are located as well as their address.

We'll discuss web size optimization in more detail as well in a later exercise. The resource I used for compressing the images can be found at: https://imagecompressor.com/

When you open up the page in the browser you'll notice that the overall page style is quite awful. We'll get to correct that in some of the coming exercises, starting with this one.

Please go ahead and migrate the background color declaration that we inlined in the _style_-attribute into a shared style-tag block inside the header element of our page using the following tag rule (of course substituting with the color value of your choice).

```css
section {
    background: #EC9A29;
}
```

Also see to it that the text of our main section are all set to a nice color of your choice.

Go have a look at: https://coolors.co or some other color guide of your choice if you need some inspiration.

## The solution

The first step here was pretty straight forward I think. Simply add the style-tag as described above.

```html
<html>
    <head>
        <title>...</title>
        .
        .
        <style>
            section {
                background: #EC9A29;
            }
        </style>
        .
        .
    </head>
</html>
```

To solve the part with changing the text color I added the following rule.

```css
main {
    color: #333;
}
```

As for resizing the images I used the following.

```css
img {
    width: 25%;
}
```

Again, note that this approach is not the recommended way for several reasons.

* First of all, it is not secure, allowing styles to be specified as part of a HTML document can have adverse security implications. Exactly how to prevent this and to what degree this matters is beyond the scope of this workshop. If you want to know more, please have a read at: https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.md
* Sharing CSS rules in multiple HTML files is usually beneficial in medium to large projects, and this is not possible if you apply styles directly to the HTML page. Every time the same style needs to be applied to some different HTML page you need to rewrite the same set of CSS declarations.
* It is very hard to maintain. Changing some aspect of your web page might involve finding the relevant rules on 10s to 100s of different pages, at least when your project is starting to grow.

In the next exercise, we'll focus on how to overcome this by externalizing the CSS into a separate file.