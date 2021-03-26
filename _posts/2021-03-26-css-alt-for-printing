---
layout: post
title: Using the alt-tag for printing links in CSS
published: true
tags: css
---

In the process of putting online my CV and trying to have a single version that's good for both printing and viewing on screen, I discovered a great way to append the value of an attribute through CSS:

```css
a::after {	
				content: " (" attr(href) ")";
```

This will read the value of the `href` attribute, and print its content after the `a` element. I've used this specifically in my case to show a 😸 emoji to link to my github profile, but instead show my username when the page is printed:

```html
<a alt="github/aequivinius" href="https://github.com/aequivinius"><span>😺</span></a>
```

```css
@media print {
a span {	/* hide the emoji */
				  display: none; }
				
a::after {
				  content: attr(alt); }
}
```

This can be expanded, for example, by defining own attributes and selecting based on their presence (`a[myattribute]`).
