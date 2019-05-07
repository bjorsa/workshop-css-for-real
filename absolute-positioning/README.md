# 20. Absolute positioning

By setting the _position_ property to the value of _absolute_ an element is taken out of the document flow and has no 
space reserved for it in the page layout.

```css
span#one {
    position: absolute;
}
```

It will be positioned according to its _top_, _right_, _bottom_ and _left_ values relative to the _closest positioned ancestor_ element. Which is the closest parent element that has a position other than _static_.

Positions are given as distances from the corresponding sides or the _closest positioned ancestor_ element.

Consider the following HTML.

```html
<div id="outer">
    <div id="inner">
        Content    
    </div>
</div>
```

And the following CSS rules.

```css
#outer {
    position: relative;
}

#inner {
    position: absolute;
    top: 20px;
}
```

Will position the top edge of the #inner element 20px below the top edge of the content box of the #outer element.

## The task

We need to do some work on our #heading-section, it is too slim and also the heading could use some repositioning.

Increase the height of the #heading-section to 400px.

Increase the font-size of our h1 elements to 65px and remove the padding and margins from it.

By using absolute positioning for our #heading-section h1 element, position it to the left some ways into the page 
and closer to the bottom.

## The solution

I increased the height of the #heading section to 400px.

```css
#heading-section {
    background: #EC9A29;
    height: 400px;
}
```

After increasing the font-size and removing the padding and margins the CSS for our #heading-section h1 level element look like this.

```css
#heading-section h1 {
    color: white;
    font-size: 65px;
    margin: 0;
}
```

To position it closer to the bottom left of the #heading-section we give it an absolute positioning and set the left and bottom properties. 

```css
#heading-section h1 {
    color: white;
    font-size: 65px;
    margin: 0;
    position: absolute;
    left: 100px;
    bottom: 40px;
}
```

This alone will not work and will instead position the element relative to the viewport, we need to add some position property value other than static to the containing element as well.

```css
#heading-section {
    background: #EC9A29;
    height: 400px;
    position: relative;
}
```

Note that this works just as well with inline elements, such as the h1 tag as it does with block level elements.