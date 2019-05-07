# 22. Sticky positioning

In this exercise we won't work on our existing site, since we do not have a good target for sticky positioning, at least not yet. Instead I have included a list of pokemon names that I styled to try to make it apparent how the effect of applying sticky positioning behaves.

A stickily positioned element are part of the normal document flow (treated as relatively positioned) until it reaches some threshold position (relative to its nearest ancestor with a scrolling mechanism, which are created when the overflow property are set to hidden, scroll, auto or overlay) at which points it sticks at that position until it reaches the opposite end of the element to which it is stuck.

For sticky to work, you need to specify both the position property with a value of sticky, and some threshold positioning when the value should get stuck.

```css
#main ul > li:first-of-type {
    position: sticky;
    top: 5px;
}
```

With this the first list item in each list of the element with #main id, will stick when within 5px from the top of the viewport.

Sticky support is still a bit sketchy across the browsers: https://caniuse.com/#search=sticky

## The task

Add some positioning to the sample html file to make each pokemon name section letter sticky.