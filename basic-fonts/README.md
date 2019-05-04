# 6. Basic fonts

In this exercise, we are going to apply some basic fonts to our web page.

If you open up settings in Chrome and go to the Appearance section and then click Customize fonts you'll land on a page 
where the browser default fonts are visible.

Other browsers have menus corresponding to this where you can examine how a web page using the built in browser font 
will look.

Using the example of chrome, this is what it looks like in my browser.

```text
Standard font

Times

16: The quick brown fox jumps over the lazy dog
```

The standard font corresponds to not specifying a font at all.

```text
Serif font

Times

16: The quick brown fox jumps over the lazy dog
```

The serif font corresponds to the built in _serif_ font family.

```css
p {
    font-family: serif;
}
```

```text
Sans-serif font

Helvetica

16: The quick brown fox jumps over the lazy dog
```

As you might guess, the sans-serif font corresponds to using the built in _sans-serif_ font family.

```css
p {
    font-family: serif;
}
```

```text
Fixed-width font

Courier

16: The quick brown fox jumps over the lazy dog

```

The fixed-width font corresponds to setting the _monospace_ built in font family.

```css
p {
    font-family: monospace;
}
```

There are even more built in (generic) font families that you can read about here: https://developer.mozilla.org/en-US/docs/Web/CSS/font-family

This is still however somewhat limiting, so in this exercise we are going to work with google fonts to apply a font (or even two if you feel up for the challenge) to our web page.

Google provides an online resource that you can use for quickly getting started with applying some fonts to your web page.
You can find google fonts here: https://fonts.google.com

Upon selecting a font, the site will provide you with instruction on how to include a reference to the online font resource as well as give you an CSS snippet that is needed for inclusion in your .css file.

As an example using the Open Sans would look something like this
```html
<link href="https://fonts.googleapis.com/css?family=Open+Sans" rel="stylesheet">
```

Please be advised that you need to include the google font link above the inclusion of your main.css file in the HTML document.

```css
p {
font-family: 'Open Sans', sans-serif;
}
```

The font family specified after the comma (,) sign is the fallback font, should the 'Open Sans' font not be available.

## The task

Please apply a different font to match the style of your web-site to the h-level elements of the page using google fonts. Make sure that it uses a fallback style that doesn't make the page look awful.

## The solution

I've added a link to the HTML page above the link element that I've used to include the main.css file.

```html
<link href="https://fonts.googleapis.com/css?family=Lato" rel="stylesheet">
```

In the main.css file, I've added the _font-family_ property to the h-level element selector that was already there.

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