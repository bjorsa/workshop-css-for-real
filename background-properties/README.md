# 23. Background properties

## The task

Remove the solid color from the #heading-section and add the pigments-min.jpg as a background image to the section instead.

Resize, style and position the header and background image so that looks nice.

## The solution

I replaced the background color with the image.

```css
#heading-section {
    background-image: url("../images/pigments-min.jpg");
    height: 400px;
    position: relative;
}
```

To make sure that we avoid sizing issues I set it to not repeat and sized it to cover the entire area.

```css
#heading-section {
    background-image: url("../images/pigments-min.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    height: 400px;
    position: relative;
}
``` 

I then played around some with positioning to get it where I wanted.

```css
#heading-section {
    background-image: url("../images/pigments-min.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: left 0 top 20%;
    height: 400px;
    position: relative;
}
```

Finally, to increase the readability, I increased the opacity of the linear gradient of the navigation bar as well as added another gradient covering the image.

```css
#heading-section {
    background-image: linear-gradient(rgba(0, 0, 0, .1), rgba(0, 0, 0, .9)), url("../images/pigments-min.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: left 0 top 20%;
    height: 400px;
    position: relative;
}

.navigation {
    background: linear-gradient(rgba(0, 0, 0, .8), rgba(0, 0, 0, .8));
    padding: 20px;
}
```

It's actually possible to express all of the background properties using the background shorthand.

```css
#heading-section {
    background: linear-gradient(rgba(0, 0, 0, .1), rgba(0, 0, 0, .9)), url("../images/pigments-min.jpg") left 0 top 20%/cover no-repeat;
    height: 400px;
    position: relative;
}
```

You can read more about that here: https://developer.mozilla.org/en-US/docs/Web/CSS/background