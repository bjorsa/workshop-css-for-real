# 18. Footer

## The solution

I added a class of _.footer__links_ to the ul element inside the _#footer-section_.

```html
<ul class="footer__links">
```

I set the background color of the _#footer-section_ to match the navigation bar at the very top of the page and also added some padding and top margin.

```css
#footer-section {
    background: linear-gradient(rgba(0, 0, 0, .5), rgba(0, 0, 0, .5)), #EC9A29;
    padding: 30px;
    margin-top: 45px;
}
```

Again, since the links are layed out in a list, it needed to loose it's bullet points and any built in padding and margins that it came with.

```css
.footer__links {
    list-style: none;
    padding: 0;
    margin: 0;
    text-align: center;
}
```

With the text-align property, I moved the link to the center of the footer.

Getting them on the same line and spacing them was done with:

```css
.footer__links li {
    display: inline-block;
    margin: 0 45px;
}

```

Finally, the _:active_ and _:hover_ states of the links were styled, this time leaving the border effect out.

```css
.footer__links a:hover,
.footer__links a:active {
    color: white;
    border: none;
}
``` 