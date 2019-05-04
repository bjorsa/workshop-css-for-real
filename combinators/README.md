# 8. Combinators

It is possible to use multiple selectors for a single rule. This can be useful for expressing fine grained selections where it is not appropriate or possible to explicitly designate the target elements with specific classes.

The first thing that we already saw in the CSS that we wrote so far, is the selector list.

```css
h1, 
h2, 
h3, 
h4, 
h5, 
h6 {
    color: #530100;
    font-family: Lato, sans-serif;
}
```

Please note that if one of the selectors is something that the browser doesn't support, then all the selectors get completely ignored.

The selector list allows you to attach multiple selectors to one css rule. This is not the same thing however as a combinator. 
Combinators are used to express relationships between the element to be selected and other elements in the same page. 

Let me illustrate this with an example.

Imagine that we have the following HTML

```html
<div id="main-content">
    <div class="important">
        <h3>Important</h3>
        <p>Some very troubling news</p>
        <ul>
            <li>
                <p>He will probably not give up power no matter what the outcome of the next election.</p>
            </li>
            <li>
                <p>
                    Lies has become commonplace and are no longer noteworthy. 
                    Any politician can use then freely nowadays.
                </p>
            </li>
        </ul>
    </div>
    <div>
        <p>You may be interested to know that there is a new restaurant opening next weekend.</p>
    </div>
</div>
```

Selecting the text inside the paragraphs of the important section could be done using a descendant combinator like this.

```css
.important p {
    color: red;
}
```

This would color all of the text inside the paragraphs that are descendants of the div tag marked with the _important_ class.

The combinators that we can use in our CSS are the following.

* Descendant combinator - Two selectors A and B, separated with a space: A B, selecting any element B that is a _descendant_ of any element matching A.
* Child combinator - Two selectors A and B, separated with a greater than sign: A > B, selecting any element B that is a _direct child_ of any element matching A.
* Adjecent sibling combinator - Two selectors A and B separated with a plus sign: A + B, selecting any element B that is _the very next sibling_ of any element matching A.
* General sibling combinator - Two selectors A and B separated with a tilde sign: A ~ B, selecting any element B that is _any sibling following_ any element matching A.

Armed with this new knowledge we can make some adjustments to our existing web page.

## The task

The white color which we previously applied to the h1 element inside the section with id _heading-section_ is selected by using a class.

```css
.heading-section__title {
    color: white;
}
``` 

This is a bit awkward since that class will probably never get used anywhere else. Change the CSS so that the h1 element is instead selected using a combinator.

Also, the img elements inside of the section element with id _retailer-section_ is targeted using only the element selector, fix this using combinators.
