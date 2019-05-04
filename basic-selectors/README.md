# 4. Basic Selectors

In this exercise we are going to add some basic selectors to our main.css file.

The selectors that you need to be aware of at this point is the following.

* The element selector, which selects all matching elements of your web page.

```css
h1 {
    background: red;
}
```

* The class selector, which selects all elements with the matching class applied.

```html
<div class="warning">Note this!</div>
```

```css
.warning {
    color: orange;
}
```

* The universal selector, selecting all of the elements of your web page. This is rarely used, but we'll see a use case in later sections.

```css
* {
    color: red;
}
```

* The ID selector, selecting a single element with matching ID on your web page.

```html
<div #id="navigation-bar">
    ...
</div>
```

Please note the use of kebab case when selecting class names. The reason being that CSS, just like HTML, is case insensitive. Using class names in camel case like _navigationBar_ would then allow the user to target this class using for instance _navigationbar_ or even _naviGationbar_ which might be undesirable.

In a later exercise, we'll also have a look at standard naming schemes for classes that might be of use for avoiding collisions as your project grows.

```css
#navigation-bar {
    width: 200px;
}
```

* The attribute selector, selecting all of the elements that has the specified attribute.

```html
<button disabled>Click</button>
```

```css
[disabled] {
    color: gray;
}
```

The above is only a very basic use of selectors, but it does give us some options for marking and selecting specific elements or classes of elements on our web page.

## The task

So far we've styled our page using exclusively element selectors, this affords us very little control. As a result of this, both of our sections have the same background color.

Please correct this so that only the header section, where our h1 element is placed has this background color.

Also our heading elements (h1, h2, ...) tags should stand stand out from the rest of the text, please apply the a darker version (darkened 60% or so) of the same color used as heading section background to all of the h-level tags.

You might want to look into some online color tool to help with this operation, for instance: https://www.hexcolortool.com

This makes the heading section title meld into the background since it is now the same color base as the background element, mark the heading section tag with a class and apply a white color to the text of the title to increase the contrast.
