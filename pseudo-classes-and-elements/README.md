# 13. Pseudo classes and elements

In CSS there is something called pseudo classes and pseudo elements.

Let's start with pseudo classes. 

### Pseudo classes

A pseudo class is something that lets you select a 
certain state of an element, as for instance the _:hover_ pseudo class which marks an element that someone hovers over with the mouse pointer.
Or something that helps us select some related element more easily like the _:first-child_ pseudo class that selects the first child element.

Examples.

```html
<body>
    <a href="#">Hover me</a>
    .
    .
    <ul>
        <li>First list item</li>
        <li>Second list item</li>
        <li>
            Sub list
            <ul>
                <li>First sub list item</li>
                <li>Second sub list item</li>
                <li>Third sub list item</li>
            </ul>
        </li>
    </ul>
</body>
```

The following CSS

```css
a:hover {
    color: fuchsia;
}

ul > li:first-child {
    font-weight: 700;    
}
```

Would color the link text pink when someone hovered the link and also make the _First list item_ and _First sub list item_ text bold.

You can read more about pseudo classes here: https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes

### Pseudo elements

Pseudo elements on the other hand represents a selector targeting a certain part of some element. Such as the _::first-letter_ pseudo class that targets the very first character of the text content of some element.

You can read more about pseudo elements here: https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements

## The task

We are going to apply some more styling to our links in the navigation bar. For this to work, we need to prepare just a little bit.

Start by removing the padding from the #heading-section rule and then applying some padding to the entire navigation bar as well as the h1 element.

```css
#heading-section {
    background: #EC9A29;
    height: 200px;
}

#heading-section h1 {
    color: white;
    padding: 20px;
}

.navigation {
    background: linear-gradient(rgba(0, 0, 0, .5), rgba(0, 0, 0, .5));
    padding: 20px;
}
```

I've also added some darker tone as a backdrop for the navigation bar using the linear-gradient() value function, we'll see this one in action again in later exercises.

The alignment on the links are also a little bit lacking. We'll fix this as well later on when we get better tools for the job.

Now, go ahead and restyle all links to have the same color as the background color of the #heading-section. Also remove the underline from the link text using the _text-decoration_ property.

Once this is done, add an underline to the links when you hover over them, selecting with the _:hover_ and _:action_ pseudo classes and applying a _bottom-border_ in a different color.

Mark the #heading-section link that surrounds the image with some class so that you can exclude that link from having the same behaviour (using the :not pseudo class selector) since we do not want an underline for the image.

Give the links some bottom padding as well to add some extra space between the link text and the border that appears.

Override the color choices for the links inside of the navigation bar using a white color for both the text and border when you hover over them, as well as making them bold.