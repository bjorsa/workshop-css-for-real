# 19. A new page

## The task

Create the testimonials page.

Start by copying all of the material inside the body tag of the main page.

Remove everything between the #heading-section and the #footer-section.

Fix the navigation bar links.

Now, we are going to move some of the material from the main.css file into a shared.css file that can be used from both of the pages.

Move all of the general styling as well as rules referring directly  to the header and footer into the new shared.css file.

Add a new link element to the main HTML file, above the one referring to main.css and use it to include shared.css

Check that your page looks the way it did before.

Copy the link elements, except the one referring to main.css and paste it into the head element of the testimonials page. Fix the file paths of the copied links.

Add a new style sheet directly under the testimonials directory and name it testimonials.css and link it into the page.

Check the look of the testimonials page by clicking the "Our Customers" link on the navigation bar.

Now copy the contents of the tesimonials-section.html file and paste it into the testimonials page, between the #heading section and the #footer-section.

Style the new page by adding some spacing for the new section making it look something along the lines of this.

![Testimonials Page](images/testimonials.png)

## The solution

I started by adding some spacing to the elements of the new testimonial section and also setting the width of the section to 60%. Also the font was upsized and italiziced.

```css
#testimonial-section {
    padding: 20px;
    margin: 45px auto 0;
    width: 60%;
}

.testimonial__item {
    margin-top: 30px;
    font-size: larger;
    font-style: italic;
}
```

The odd looking margin shorthand with three values sets the top to 45px, left and right to auto and bottom to 0.

The image containers were then resized and floated left. The images themselves were given a width to fill out the image containers.

```css
.testimonial__image {
    float: left;
    width: 20%;
}

.testimonial__image img {
    width: 100%;
}
```

I then added the clearfix class to the testimonial__details elements in the HTML structure to avoid the separate items bleeding into each other.

```html
<div class="testimonial__details clearfix">
```

To give the text some spacing I had to increase the margin from the left edge to match the size of the image and then some.

```css
.testimonial__text {
    margin-left: calc(20% + 20px);
}
```

The calc function can be used to add units of different types.

Finally to achieve the inverted effect of the second item, I added a new class _.testimonial__item--flipped_.

```html
<div class="testimonial__item testimonial__item--flipped">
    <h3>Chillin&apos; with my minis</h3>
    <div class="testimonial__details clearfix">
        <div class="testimonial__image">
            <img src="../../images/testimonials/sam-lenz-min.jpg" alt="The Miniature Dude"/>
        </div>
        <div class="testimonial__text">
            I do paint a lot! There is no way I'm paying premium for equipment that I can have at a bargain that still does the job!
            Colorisious has a good range of cheap stuff that I can use for my painting without worrying that I'll break it or how much color I use.
            I just wanna chill with my minis, no hastle!
        </div>
    </div>
</div>
```

And then styled the elements to reverse the look.

```css
.testimonial__item.testimonial__item--flipped > h3 {
    text-align: right;
}

.testimonial__item--flipped .testimonial__image {
    float: right;
}

.testimonial__item--flipped .testimonial__text {
    margin-left: 0;
    margin-right: calc(20% + 20px);
}
```