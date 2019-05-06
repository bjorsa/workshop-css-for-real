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