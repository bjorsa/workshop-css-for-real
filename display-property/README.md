# 12. The display property

The _display_ property sets whether an element is treated as a block or an inline element and also the layout used for it's children, such as grid or flex.

We'll cover flex and grid in later exercises, for now let's look at the _block_ and _inline_ property values of the _display_ property.

* block - included in the flow as a block level element, with line breaks inserted both before and after the element.
* inline - included in the flow as an inline element without any generated line breaks. 

Let's look at these in more detail.

### Block level elements

These are the main properties of block level elements, the box model they have is the same that we've looked at during the previous lectures.

* Block level elements by default take up the entire page width.
* Block level elements can contain inline elements as well as other block level elements.
* Block level elements begin on new lines.
* A block level element acts as a new layout context (flow layout by default).

Example of block level elements are:

* \<address> - Contact information.
* \<article> - Article content.
* \<aside> - Aside content.
* \<blockquote> - Long ("block") quotation.
* \<dialog> - Dialog box.
* \<dd> - Describes a term in a description list.
* \<div> - Document division.
* \<dl> - Description list.
* \<dt> - Description list term.
* \<fieldset> - Field set label.
* \<figcaption> - Figure caption.
* \<figure> - Groups media content with a caption (see <figcaption>).
* \<footer> - Section or page footer.
* \<form> - Input form.
* \<h1>, \<h2>, \<h3>, \<h4>, \<h5>, \<h6> - Heading levels 1-6.
* \<header> - Section or page header.
* \<hgroup> - Groups header information.
* \<hr> - Horizontal rule (dividing line).
* \<li> - List item.
* \<main> - Contains the central content unique to this document.
* \<nav> - Contains navigation links.
* \<ol> - Ordered list.
* \<p> - Paragraph.
* \<pre> - Preformatted text.
* \<section> - Section of a web page.
* \<table> - Table.
* \<ul> - Unordered list.

### Inline elements

These are the main properties of an inline element.

* Inline elements take up only the space they need to fit their content, thus we may have 2 inline elements on the same line.
* Inline elements may contain only data and other inline elements. 
* Inline elements are laid out horizontally in a box called line box. 
* If there isn’t enough space to fit all content a line break is added.
* Any vertical padding or border, although still applied, do not push away neighbouring elements.
* margin-top and margin-bottom have no effect on inline elements.

Example of inline elements are.

* \<a>
* \<abbr>
* \<b>
* \<br>
* \<button>
* \<canvas>
* \<em>
* \<embed>
* \<i>
* \<img>
* \<input>
* \<label>
* \<script>
* \<select>
* \<strong>
* \<template>
* \<textarea>
* \<tt>

### Inline-block elements (inline flow-root)

In addition to the above two display value settings there is a commonly used third in-between option, previously known as _inline-block_.
In fact, this is now a combination of setting an _outer_ display behaviour of _inline_ and an _inner_ display behaviour (layout behaviour for child elements) of _flow-root_,
meaning that children are layed out according to the standard flow layout model (the one we've seen so far).

The effect of applying inline and flow-root to an element is that it will act as an inline element with an attached inner 
block level element, meaning that we can lay the contents out as we would on a block level element, but without having to span an entire line of content.

The properties of inline flow-root elements are.

* Inline block elements take up only the space they need to fit their content, thus we may have 2 inline elements on the same line.
* Inline block elements can contain inline elements as well as other block level elements.
* An inline block element acts as a new layout context (flow layout by default).

Please note that the _inline flow_root_ property value is still experimental, which means you might be better off using _inline-block_

## The task

I've added some HTML to the index.html file to start laying out a navigation bar. This is the new contents of the #heading-section.

```html
<section id="heading-section">
    <div>
        <div>
            <a href="index.html">
                <img alt="Colorisious" src="../images/logo-small-min.png"/>
            </a>
        </div>
        <nav>
            <ul>
                <li>
                    <a href="products/index.html">Products</a>
                </li>
                <li>
                    <a href="testimonials/index.html">Our Customers</a>
                </li>
                <li>
                    <a href="contact-us/index.html">Contact us</a>
                </li>
            </ul>
        </nav>
    </div>
    <h1>A Splash of Colorisious</h1>
</section>
```

If you open up the page in a browser and have a look you can see that the heading-section now looks like a mess.

Add class markers to the elements above to make a structure that you think you'll need to address the issues.

First, the image is way too big, reduce the size to about 30px.

The next order of business is fixing the nav element link list, currently the items are displayed using _li_ elements which by default are block level elements. Also with a bullet leading each one.

Fix it so that the link items are all aligned on the same line using your knowledge about the display property. Also give the individual links some spacing.

Also remove the padding and margins from the ul element.

This is starting to look decent now.

Now align both the image link, the Colorisious link and the navigation bar items on the same line. Create some spacing between the navigation bar items and the Colorisious link.

## The solution

I added some class markings to the HTML as follows.

```html
<section id="heading-section">
    <div>
        <div>
            <a href="index.html">
                <img alt="Colorisious" src="../images/logo-small-min.png"/>
            </a>
        </div>
        <nav>
            <ul>
                <li>
                    <a href="products/index.html">Products</a>
                </li>
                <li>
                    <a href="testimonials/index.html">Our Customers</a>
                </li>
                <li>
                    <a href="contact-us/index.html">Contact us</a>
                </li>
            </ul>
        </nav>
    </div>
    <h1>A Splash of Colorisious</h1>
</section>
```

First of for the CSS changes, the image was reduced in size by

```css
.navigation__start img {
    height: 30px;
}
```

The link items were aligned on the same line and some space added using the following.

```css
.navigation__items ul > li {
    display: inline-block;
    margin-left: 10px;
}
```

Then the ul element rule was created as follows to remove padding and margins.

```css
.navigation__items ul {
    padding: 0;
    margin: 0;
}
```

Finally to get it all to apprear on the same line and spaced apart I added the following.

```css
.navigation__start {
    display: inline-block;
}

.navigation__items {
    display: inline-block;
    margin-left: 45px;
}
```