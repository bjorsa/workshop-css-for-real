# 5. Cascading and Specificity

CSS is read from the top of a .css file and downwards. Also files are included into the HTML document in the order you specified the links in your head element.

Cascading is a term that refers to the way that rules and properties of rules are selectively applied to elements.

Properties defined in rules that appear later in your CSS will override properties that was previously defined, provided that the rule in which they reappear has at least the same Specificity.

What does this mean? Consider the following HTML-snippet.

```html
<section>
    <h1 class="main-title">My main title</h1>
</section>
..
<section>
    <h1>Some other title</h1>
</section>
```

And the following CSS.

```css
h1 {
    color: magenta;
    font-weight: 700;
}

.main-title {
    color: green;
}

h1 {
    color: red;
}
```

The resulting web page will have bold text in all of the h1 elements, the h1 element marked with the main-title class will be green and the others will be red.

What happened? Properties will be applied from top to bottom in the order the rules appear, meaning that we first make all of the h1 elements magenta colored and bold. 

When we process the rule with the .main-title selector, the h1 element marked with that class will have it's color reassigned to green, it will not however clear the font-weight property since that was not reassigned to another value.

When the last rule is applied it will reassign the colors of all of the h1, except for the one marked with the main-title class, since class selectors have higher Specifity.

What are the rules for Specifity then?

We've already noticed this: different types of selectors have different specifity.

The order from lowest to highest is

0. universal selector (*) has no effect on specifity
1. element and ::pseudo-element selectors
2. .class, :pseudo-class and [attribute] selectors
3. #id selectors
4. inline styles

This might seem simple enough, but will get a little bit more tricky when we start using combined selectors and introduce inheritance into the mix. More on that later.

For a complete set of rules, please have a look at: https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity

There is a nice Specifity calculator that gives you visual cues about how the specifity is calculated and also let you compare specifity from multiple selectors at: https://specificity.keegan.st/

## The task

Please introduce a rule structure similar to the above in your CSS file and then examine your web page using the inspector in Chrome. Document what you see.

Clean up and restore your CSS.