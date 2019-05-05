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

## The solution

First of, restyling the links to get rid of the underline on the text and using the same color as the background of the #heading-section should be pretty straight forward.

```css
a {
    text-decoration: none;
    color: #EC9A29;
}
```

Next we added the border that should underline the links on hover, at the same time taking care not to target the image link.

In the HTML file I marked the image link with a class _.image-link_.

```html
<a href="index.html" class="image-link"><img alt="Colorisious" src="../images/logo-small-min.png"/></a>
```

Next we alter the a element selector rule and add some behaviour for the a:hover and a:active states.

```css
a {
    text-decoration: none;
    color: #EC9A29;
    padding: 2px;
}

a:not(.image-link):hover,
a:not(.image-link):active {
    border-bottom: 3px solid #333;
}
```

A padding of 2px was added along with the border that should appear when hovering or having a link active. 
The :not(.image-link) pseudo class was added to shield the image link.

The next task, overriding the color choices for the links in the navigation bar and making them bold was accomplished by.

```css
.navigation a {
    font-weight: 700;
}

.navigation a:hover,
.navigation a:active {
    color: white;
    border-color: white;
}
```

Note that the expression "a:not(.image-link):hover" has exactly the same specificity as ".navigation a:hover" which means that this only works when the 
".navigation a:hover" rule is specified later in the file. Try changing the order of the declarations and observe the effect.

This might be a drawback of overusing pseudo classes, they do set a rather high specifity and can be complicated to read.

There is a simpler way of stating the same thing, maybe you even ended up with the following CSS?

```css
a:hover,
a:active {
    border-bottom: 3px solid #333;
}

a.image-link:hover,
a.image-link:active {
    border: none;
}
```

This has multiple benefits. First of all it reduces the specificity of the general link state declarations to the bare minimum, making them easier to override where needed.
And secondly, makes the CSS code much easier to read. Note that we no longer have the case where ordering matters in our CSS file since the selectors now have the proper specificity for what we want to achieve. 