# 7. Inheritance

In CSS some properties are inherited from parent elements in the HTML to child elements. In this exercise we are going to have a look at the basics of inheritance and see how it releates to Specifity.

The CSS properties that are good candidates for inheritance include for instance; color, font-family and font-size, that you typically want to be applied at great extent throughout your document.

```css
body {
    color: #333;
}
```

Makes all the content of your webpage the same dark grey color.

Whether or not a specific property is inherited is listed in the property definition.

The priority of inherited properties are low, even below the properties set by the browser default style sheet. If you were to inspect a child element of body after declaring the above rule, you would find the rule at the very bottom of applied rules for that element.

There are some keywords that let you control how inherited properties are applied.

* inherit - Can be used to reapply an inherited property that would otherwise be overridden.
* initial - Sets the property to the specification default value for the specific property. This is very uncommon to use with inherited properties.
* unset - Sets the property to the inherited value if there is one, otherwise to the initial value (se above).
* revert - Rolls back the property value as if no styles had been applied to it in the current CSS origin. This differs from initial in the sense that reverted values first checks the user agent style sheet for rules to apply.

More information about inheritance and related topics can be read here: https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance

## The task

Move the color property from the rule with the main element selector to a new rule with the body element selector, also go select a nice font family for the contents of your web-page using inheritance.

Moreover, remove the italicized style from the address tags.

Make sure that the font family that we applied to the h-level elements are not overridden, and have a look in the inspect view of Chrome to see how the inherited properties are applied.