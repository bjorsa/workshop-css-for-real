# 11. Margin collapsing

In CSS, there is an effect known as margin collapsing, which we'll examine in this exercise. This apply only to 
top and bottom margins, NOT to left and right margins.

What does collapse mean, it means that 2 margins that would otherwise be added to each other instead are overlayed, 
using the larger margin as a result.

There are three basic cases when margins collapse.

1. Adjacent siblings with margins.
2. Parent and first/last child. As we saw in the box model exercise. Parents that doesn't have content that interfere with a margin has their own margin collapsed with that of the child. The margin then appear outside of the parent extent.
3. Empty blocks. Blocks with no content, border, padding or sizing property set, then it's own top and bottom margin collapse.

Combinations of these rules may occur. 

Margins of blocks that are absolutely positioned or floating never collapse. We will talk more about positioning in a later exercise.

To find out more about margin collapsing, please have a look at: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing

## The task

Add a bottom margin of 20px to our #heading-section for demonstration purposes and examine the #heading-section as well as the h2 element inside our #retailer-section in the Chrome Inspector.

There should be no visible effect on the page.

What did you find?

Remove the margin of the #heading-section element once more.

Also, as we are on the subject of margins, you might have noticed that we have some margin around all of the content in our main element of our web page.
This is what the browser default style sheet sets for the body element, go ahead and override that so that we can get rid of the default margin.