---
title: Arguments for Real-Time Validation
date: 2019-05-06 00:00:00 Z
excerpt: Should you check a user’s input entry as they type it? A look at the arguments for real-time input validation.
images:
- image:
    alt: Graphic illustrating success and failure in form entry interactions.
    url: "https://isralduke-site-files.s3.amazonaws.com/images/real-time-form-validation.svg"
---
<p class="lead">{{page.excerpt}}</p>
#### The Scenario

A user or a website visitor is filling out a form. When they finish, they press “Submit” expecting to be finished with the form. But then, to their dismay, the browser kidnaps them and brings them to a page listing problems with the information they entered. 

Wouldn’t it be great if the user saw the potential problems before submitting the form? Yes, it would be great and a lot of thought has gone into this problem.

#### Give the User Instant Feedback

Some fields may require some extra thought from the user. Let’s use the password field as an example. It has all sorts of anxiety-producing requirements such as a mixture of uppercase and lowercase letters, a certain amount of numbers, and maybe certain special characters, but not other special characters. To start, tell them about these special requriements up front. Maybe this can be a help tip, or even better, a list of those requirements. 

Now, the extra step for a great user experience would be to check what they entered in the password as soon as they move to the next field. In the industry, we call the event “on blur” when the user moves their entry actions away from a field. Checking the user’s inputted information when they move away from a field is called “On Blur Validation.” Say that at a party sometime soon for strange looks. Well, a party with normal humans.

#### How On Blur Validation is Done

We can show them what needs to be entered. I have already said this, but it nevers hurts to repeat this: show them what you need. Again, we’ll use the password field as an example. Look at the image below. It explains, in simple language, what makes a great and acceptable password.

<figure>
	<img class="shadow-small mb-2" src="https://isralduke-site-files.s3.amazonaws.com/images/on-blur-validation-exhibit-image-1.png" alt="An example of a password field.">
	<figcaption>An example of a password field with requirements explained in simple language.</figcaption>
</figure>

Sorry I don’t have a GIF _(say it with a hard “G” sound)_ here, but imagine the user had to wait to see this error message after they tried to submit this. Their work is multipled because they have to come back to a screen they already tried to move on from in their workflow. But, if this message is displayed as soon as they move to a new field, they still have a chance to fix the error with a minimal impact on their attention, workload, and cognitive load.

<figure>
	<img class="shadow-small mb-2" src="https://isralduke-site-files.s3.amazonaws.com/images/on-blur-validation-exhibit-image-2.png" alt="An example of the error message.">
	<figcaption>An example of the error message.</figcaption>
</figure>

This approach to validation for the user will esepcially show its return on investment in long, complicated forms. Long forms where backend validation isn’t required can give an easy entry experience to the user because errors show up immediately, they can fix them immediately, and there won’t be any agonizing browser redirects listing painful bullet points of errors to track down.


#### Further Reading

- <a href="https://www.smashingmagazine.com/2012/06/form-field-validation-errors-only-approach/" title="Errors Only Approach to Form Fields Validations" target="_blank">Errors Only Approach to Form Fields Validations</a>
- <a href="https://www.smashingmagazine.com/2009/07/web-form-validation-best-practices-and-tutorials/" title="" target="_blank">Validate Before They Press Submit</a>
- <a href="https://blog.prototypr.io/ux-best-practices-of-form-validation-ddb8a0df14fd" title="Best Practices for Form Validation" target="_blank">Best Practices for Form Validation</a>