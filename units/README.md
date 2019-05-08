# 24. Units

## The task

Go through the pages and CSS that we have so far and redo the selection of units now that we know a little bit more 
about what options are available.

## The solution

There are of course very many ways in which to solve this. This is what I ended up with.

shared.css
```css
* {
    box-sizing: border-box;
}

body {
    font-family: 'Open Sans', sans-serif;
    color: #333;
    margin: 0;
}

h1,
h2,
h3,
h4,
h5,
h6 {
    color: #530100;
    font-family: Lato, sans-serif;
}

h2 {
    text-align: center;
}

h2::after {
    display: block;
    height: 2px;
    background-color: #EC9A29;
    content: " ";
    width: 100px;
    margin: 30px auto 0;
}

a {
    text-decoration: none;
    color: #EC9A29;
    padding-bottom: .2rem;
}

a:hover,
a:active {
    border-bottom: 3px solid #333;
}

a.image-link:hover,
a.image-link:active {
    border: none;
}

address {
    font-style: normal;
}

.clearfix {
    overflow: auto;
}
.clearfix::after {
    content: "";
    clear: both;
    display: table;
}

#heading-section {
    background: linear-gradient(rgba(0, 0, 0, .1), rgba(0, 0, 0, .9)), url("../images/pigments-min.jpg") left 0 top 20%/cover no-repeat;
    height: 33vh;
    position: relative;
}

#heading-section h1 {
    color: white;
    font-size: 4em;
    margin: 0;
    position: absolute;
    left: 5%;
    bottom: 10%;
}

.navigation {
    background: linear-gradient(rgba(0, 0, 0, .8), rgba(0, 0, 0, .8));
    padding: 1.3rem;
}

.navigation a {
    font-weight: 700;
}

.navigation a:hover,
.navigation a:active {
    color: white;
    border-color: white;
}

.navigation__start {
    display: inline-block;
}

.navigation__start img {
    height: 2rem;
}

.navigation__items {
    display: inline-block;
    margin-left: 3rem;
}

.navigation__items ul {
    padding: 0;
    margin: 0;
}

.navigation__items ul > li {
    display: inline-block;
    margin-left: .7rem;
}

#footer-section::after {
   content: "... This is ugly ...";
   visibility: hidden;
   padding: 2rem 0;
}

#footer-section nav {
    background: linear-gradient(rgba(0, 0, 0, .5), rgba(0, 0, 0, .5)), #EC9A29;
    padding: 2rem;
    position: fixed;
    bottom: 0;
    right: 0;
    left: 0;
}

.footer__links {
    list-style: none;
    padding: 0;
    margin: 0;
    text-align: center;
}

.footer__links li {
    display: inline-block;
    margin: 0 3rem;
}

.footer__links a:hover,
.footer__links a:active {
    color: white;
    border: none;
}

```

main.css
```css
#favourites-section {
    margin-top: 3rem;
}

.product__images {
    list-style: none;
    margin: 2rem 0 0 0;
    padding: 0;
}

.product__image-item {
    float: left;
    width: 25%;
    background: black;
}

.product__image-item img {
    opacity: 0.7;
    vertical-align: middle;
    width: 100%;
}

#retailer-section {
    margin: 45px 0;
    padding: 1.3rem;
}

.retailer__list {
    margin-top: 2rem;
    margin-left: auto;
    margin-right: auto;
    width: 90%;
    text-align: center;
}

.retailer__item {
    display: inline-block;
    text-align: center;
    width: 30%;
}

.retailer__item img {
    width: 80%;
    border-radius: 50%;
    border: 2px solid #EC9A29;
}

.retailer__item address {
    text-align: left;
    margin-top: 1.3rem;
    padding-left: 5rem;
}
```

```css
#testimonial-section {
    padding: 20px;
    margin: 3rem auto 0;
    width: 60%;
}

.testimonial__item {
    margin-top: 2rem;
    font-size: larger;
    font-style: italic;
}

.testimonial__item.testimonial__item--flipped > h3 {
    text-align: right;
}

.testimonial__image {
    float: left;
    width: 20%;
}

.testimonial__item--flipped .testimonial__image {
    float: right;
}

.testimonial__image img {
    width: 100%;
}

.testimonial__text {
    margin-left: calc(20% + 20px);
}

.testimonial__item--flipped .testimonial__text {
    margin-left: 0;
    margin-right: calc(20% + 20px);
}
```
