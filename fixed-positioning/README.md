# 21. Fixed positioning

By setting the _position_ property to the value of _fixed_ an element is taken out of the document flow and has no 
space reserved for it in the page layout.

```css
span#one {
    position: fixed;
}
```

It will be positioned according to its _top_, _right_, _bottom_ and _left_ values relative to the _initial containing block_. 
This normally is the viewport, unless some closer ancestor has a _transform_, _perspective_ or _filter_ property set to something other than _none_, in which case that element acts as the _containing block_ for the purposes of positioning.

Positions are given as distances from the corresponding sides of the _initial containing block_.

## The task

Our footer is currently not showing. We would like it to stick to the bottom edge of the visible area.

Use a position property value of fixed to achieve this.

## The solution

I started off with setting positioning and distances that would fix our #footer-section to the bottom of the viewport like this.

```css
#footer-section {
    background: linear-gradient(rgba(0, 0, 0, .5), rgba(0, 0, 0, .5)), #EC9A29;
    padding: 30px;
    position: fixed;
    bottom: 0;
    right: 0;
    left: 0;
}
```

And it works, the entire footer is however taken out of the document flow which means that it might potentially obscure content from some of the sections above it. 
And indeed it does.

Taking the entire #footer-section out of the document flow like this would force us to go back to each of the pages where it is included and add either some html structure that can "push up" the other sections, or some styling to create an extra margin with room for the footer.

I instead opted to move the styling of the footer to the child _nav_ element, like this.

```css
#footer-section nav {
    background: linear-gradient(rgba(0, 0, 0, .5), rgba(0, 0, 0, .5)), #EC9A29;
    padding: 30px;
    position: fixed;
    bottom: 0;
    right: 0;
    left: 0;
}
```

And then using the #footer-section to create some extra space (one line of text and some padding matching the height of the footer link list) within the document flow.

```css
#footer-section::after {
    content: "... This is ugly ...";
    visibility: hidden;
    padding: 30px 0;
}
```

In later exercises we'll see a better solution, using flexbox layout options.