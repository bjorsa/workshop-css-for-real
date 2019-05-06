#14. !important

!important is a modifier that you can add to the declaration of any property to have it always applied to the target element, no matter the specificity of other rules.


 
If two separate rules affecting the same element apply !important to the same property, the normal specificity rules apply.

Use of this modifier should be avoided and only applied when necessary, and then only to very specific selections.

## The task

Apply the !important modifier to the CSS rule targeting links that are hovered over.

```css
a:hover,
a:active {
    border-bottom: 3px solid #333 !important;
}
```

Examine the effects in your browser and have a look at the ordering of rules in Chrome.

Try to get back to the previous functionality without removing the !important modifier.

## The solution

This first inclusion of !important forces us to include it in two other places to get back to the previous functionality.

The first one is in the image link, so that we can avoid the border being displayed under the image when we hover over it.

```css
a.image-link:hover,
a.image-link:active {
    border: none !important;
}
```

The second place is where we have overridden the color of the border, on the hover effect on the links inside of the #heading-section.

```css
.navigation a:hover,
.navigation a:active {
    color: white;
    border-color: white !important;
}
```

This makes it plain to see that one inclusion of !important in the wrong place (or in some third party CSS framework) quickly forces the inclusion of others.

Remove all of the !important modifiers again. 