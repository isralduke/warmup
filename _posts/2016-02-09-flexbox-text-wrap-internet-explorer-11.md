---
title: FlexBox and Text Wrapping in Internet Explorer 11
excerpt: Internet Explorer 11 uses Flexbox but has a consideration to keep in mind when using long lines of text.
categories:
  - css
  - websites
image: flexbox-text-wrap-ie11.png
aux_images: ""
twitter_description: Internet Explorer 11 uses Flexbox but has a consideration to keep in mind when using long lines of text.
big_image_alt: Internet Explorer 11 uses Flexbox but has a consideration to keep in mind when using long lines of text.
---
Flexbox is a way to visually arrange portions of a website that allow designers and developers greater flexibility to meet the requirements of various screen sizes. Internet Explorer 11 uses Flexbox but has a consideration to keep in mind when using long lines of text.

Flexbox controls block level elements such as `<div>`, `<main>`, `<article>`, `<p>`, and `<section>`. When `display: flex` is applied to an element, its children automatically become flex items and inherit all of the properties and behaviors of flex items, including inline items. Any unwrapped text will also become a flex item. 

This means that Internet Explorer will present this text in a way that causes it to overflow its container (see the screenshot). While Chrome, Safari, and FireFox don't have a problem rendering this within the containing block, Internet Explorer needs that text to be wrapped in its own containing block level element such as a `<div>` or a `<p>`. 

<a title="Internet Explorer 11’s Unwrapped Text in a Flexbox Parent" href="/assets/img/blog/flexbox-long-text-ie11.png" class="image-thumb" data-lightbox="images"><img src="/assets/img/blog/flexbox-long-text-ie11.png" alt="Internet Explorer 11’s Unwrapped Text in a Flexbox Parent" /></a>

I first learned of this at <a href="http://caniuse.com/#search=flex" target="_blank" title="Can I Use Flexbox Tables">Can I Use (see Known Issue 4)</a> and while it is easily fixed, someone may have accidentally omitted a container block for their own text. The embedded CodePen below shows the easy fix.

<p data-height="268" data-theme-id="0" data-slug-hash="vLQxGy" data-default-tab="result" data-user="dukebranding" class='codepen'>See the Pen <a href='http://codepen.io/dukebranding/pen/vLQxGy/'>IE11 Text-Wrap Bug in FlexBox Workaround</a> by Duke Branding (<a href='http://codepen.io/dukebranding'>@dukebranding</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Need a [website?](/work-portfolio/projects/website%20work) [Let us help you with that!](/contact)