# 10. Box sizing

As we saw in the exercise about the box model, sizing on elements targets the content part of the element box 
making it really hard to use features such as padding and borders and at the same time specifying element extent.

Luckily there is a way around this, we can tell the browser to use another model for sizing the box, by setting the 
_box-sizing_ property.

There are 3 values that we can use for the _box-sizing_ property.

* content-box - this is the default behaviour, sizing targets the content part of the box and padding and borders are then added to calculate thet element extent.
* padding-box - with this setting, sizing includes any amount of space set for the padding, adding only borders to calculate the element extent.
* border-box - sizing includes any amount of space set for both the padding and border, not adding anything for size calculations of the element extent.

As you might have figured out already, setting the _box-sizing_ property to _border-box_ is what we need. In fact this is so common that
many web projects do across all the elements of the page.

## The task

Set the _box-sizing_ property to get rid of the horizontal scroll bar at the bottom of the web-page.

First try it out by setting the property only for the #heading-section and then reexamine how size is calculated for the section box by looking at the box model in the Chrome Inspector as well as hovering over the element in the browser using the selection tool.

Now revert the change you just did and set the _box-sizing_ property so that it affects all the elements of the page, current and future.

The scroll bar should again disappear.

Finally, delete the _border_ property from the #heading section and once again check the sizing of your element in the browser.

As a last step, remove the width property of the #heading-section, which was only there for demonstration purposes. Block level elements like the are sized at 100% of the available width 
anyways (but without forcing overflow when adding padding and borders).