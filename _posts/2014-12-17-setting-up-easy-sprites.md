---
title: Setting Up Easy Sprites
excerpt: 'Adding icons to the app was a bit complicated and we still have many of them scattered across the markup. But we&rsquo;re now using a long SVG sprite to consolidate the icons used in our app. We&rsquo;re going to continue adding our icons to it. Eventually we could have triple the current number of icons as the app is being prepared for new markets.'
categories:
  - css
  - icons
  - sprite
  - less css
big_image_alt: Icon Sprite Made with LESS CSS
big_image: /assets/img/blog/sprite-990x260.png
aux_images:
  - 
    aux_image: /assets/img/blog/icon-sprite-full.png
    aux_image_alt: icon-sprite-full
---
<h2>The Project</h2>

<p>Adding icons to the app was a bit complicated and we still have many of them scattered across the markup. But we&rsquo;re now using a long SVG sprite to consolidate the icons used in our app. We&rsquo;re going to continue adding our icons to it. Eventually we could have triple the current number of icons as the app is being prepared for new markets.</p>

<p><em>Note: Some of our customers are using the app in remote areas, sometimes in groups of several people sharing a single 3G hotspot, or in offshore contexts. Cutting down on image requests would make their lives easier. So, using a sprite makes sense.</em></p>

<img src="http://www.dukebranding.com/artboards/uploads/2014/12/icon-sprite-full.png" alt="icon-sprite-full" class="size-full wp-image-4785" />

<p>I&rsquo;ve made it easier than it was to add icons to the app and this new workflow is also going to be easy for anyone who has to work after me.</p>

<h2>The New Workflow</h2>

<p>In this new workflow, it only takes 3 steps to add a new icon.</p>

<ol>
<li>Add the icon to the SVG file.</li>
<li>Appropriately increment the <code>@iconTypes</code> variable.</li>
<li>Add the icons rule to the end of the icon class rules in the LESS file, and appropriately increment the argument. Example:<br /> <code>.scatter { .spriteOffset(35); }</code>
</li>
</ol>


<p>Only 1 step to use the new icon.</p>

<ol>
<li>Add the markup with any appropriate classes, <code>&lt;span class="icon16 document16"&gt;&lt;/span&gt;</code> or <code>&lt;span class="icon128 dashboard128"&gt;&lt;/span&gt;</code> (actual examples from the app).</li>
</ol>


<h2>The LESS</h2>

<p><a href="icon-sprite.less" target="_blank" title="LESS File for SVG Sprite">Download the LESS file.</a></p>

<p>The single sprite we&rsquo;re using contains 36 icons, each at 32px by 32px. Some places in the app will called a scaled version of this sprite to present the icons at 16, 24, or even 128 pixels. For calculating offsets, I use the position of the appropriate icon with a zero-based index, in which the first icon is 0 when referenced by the parametric mixins. I am also including additional states such as a hover and selected.</p>

<h3>The Variables</h3>

<p><em>Note: I&rsquo;m only going over the LESS relevant to what I am trying to highlight.</em></p>

<ul>
<li><code>@iconBase: 32px;</code> The is the base icon size, square.</li>
<li><code>@iconTypes:    36;</code> The number of icons in the sprite, which will be incremented as we add icons to the sprite. This has an effect on <code>background-position-x</code>.</li>
<li><code>@iconStates:   3;</code> The number of states (default, hover, selected). This has an effect on <code>background-position-y</code>.</li>
<li><code>@x16 = .5;</code> This is the scale multiplier that I&rsquo;m using as the multiplier to get a 16px icon out of a 32px icon.</li>
<li><code>@x24 = .75;</code> Same as above, but for a 24px icons from the 32px base.</li>
<li><code>@x32 = 1;</code> Base icon size.</li>
<li><code>@x128 = 4;</code> We have some 128px icons on the main menu screen.</li>
<li><code>@multiplier = 0;</code> Setting the initial value.</li>
<li><code>@index = 0;</code> Setting the initial value of the index for the icons in the sprite.</li>
</ul>


<h3>The First Mixin: <code>.spriteInit(@multiplier)</code></h3>

<p>This <code>.spriteInit(@multiplier)</code> mixin does two things.</p>

<ol>
<li>It derives the additional <code>background-size</code> values for the scaled versions of sprite.</li>
<li>It sets the <code>width</code> and <code>height</code> for the icon.</li>
</ol>


<p>You can see how I&rsquo;m using this mixin to define the icon size classes.</p>

<h3>The Second Mixin: <code>.spriteOffset(@index)</code></h3>

<p>When we add icons to the sprite we don&rsquo;t want to manually write offsets in the LESS. This mixin takes care of automatically doing that for us. It writes all of he necessary CSS at all of our sprite sizes.</p>

<p>Using <code>.spriteOffset(@index)</code> only requires the index(es) for the icon(s) we add to the sprite and it makes all the necessary offsets for each icon class in all of the sprite sizes, default or derived.</p>

<h2>The Benefit</h2>

<p>When I have to add a new icon to the project, for example <code>.newIcon(101)</code> I only have 3 things to do. It will also be easy for anyone to work after me.</p>

<h3>Thanks &amp; Credit</h3>

<p>While I&rsquo;m happy to share my LESS snippets with you, I am unable to share the SVG file.</p>

<p>Thanks for reading this. I hope you find it useful.</p>
