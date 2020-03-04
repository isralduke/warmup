---
title: Make the Color Contrast Pop (enough)
date: 2020-03-04 00:00:00 Z
excerpt: Color is important because it can signal statuses, evoke emotion, and cause a purchase. But what if some people have trouble seeing your color?
images:
- image:
    alt: Color Contrast example image. 
    url: https://isralduke-site-files.s3.amazonaws.com/images/color-contrast-banner.png
---

<p class="lead">{{page.excerpt}}</p>

#### What is Color Contrast

For our purposes in this article, Color Contrast refers to the amount of visual separation between two colors. For this article, I’ll be talking about the amount of Color Contrast between text and the background to the text. The amount of separation between those two colors can be measured with math.

Don’t worry, I won’t ask you to do any homework.

Each color you see on a screen, like a monitor or mobile phone screen, is encoded into the website or app using a numeric value which computers turn into the colors you see. White is encoded using the number `#FFFFFF` (called a hexadecimal value) and Black is encoded using the number `#000000`. 

_Now, there are more number types we could use, such as `rgb(255,255,255,1)` for White and `rgb(0,0,0,1)` for Black (called RGB values), and there are more ways to encode color. But for this article we’ll only talk about the color numbers using <a href="https://htmlcolorcodes.com" target="_blank" title="Make your own colors!">hexadecimal values</a>._

#### Calculating Color Contrast

Now that I have those colors’ numbers, special tools called Contrast Calculators (here’s <a href="https://colorific.darrellhanley.com" target="_blank" title="Color Contrast Calculator by Darrel Hanley">my favorite Contrast Calculator</a> because it can also simulate color blindness) can perform calculations on those numbers to determine the amount of contrast (visual separation) between them. The resulting calculated number is called a Contrast Ratio.

Going back to White and Black, their Contrast Ratio is **21:1**. That’s the highest possible Contrast Ratio using current monitors and color technology. This is the best possible _color_ combination to make easily readable text on a screen. _(I’ll talk about text sizes in a later article.)_ 

#### How Much Color Contrast is Needed?

There’s a few different authorities we look to for guidance on how much Color Contrast we need to accommodate people with vision difficulties. One authority is <a href="https://accessibility.digital.gov/visual-design/color-and-contrast/" target="_blank" title="Color Contrast Article on Digital dot gov">Digital.gov’s Web Development and Design Standards</a>. Saying the simplest way, we need Color Contrast of **4.5:1** for the bare minimum. But, if we can design the website or app so that text gets Color Contrast of **7:1**, then we’re doing an exceptional job.

#### A Simple Breakdown

Again, talking only about color, the Color Contrast in text we want is:

- **4.5:1**. This is the minimum amount.
- **7:1**. This is the awesome amount.
- **3:1**. This is for a link in text to the surrounding text.
- **3:1** This is the amount we want for the edges of user interface elements to the surrounding color.

#### The Takeway

**More Color Contrast is better.** Stay away from those light greys on whites! It may look cool to your graphic designer friends, it’s hard for some people to read. Older people, people with dimming vision, or people with other vision difficulties can more easily see text with higher Color Contrast. It follows that if people with difficulties can easily read your text, then people without vision difficulties will also be able to easily read your text.