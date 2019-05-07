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