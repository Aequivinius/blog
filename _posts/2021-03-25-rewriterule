---
layout: post
title: Apache RewriteRules recursion
published: true
tags: apache rewriterules
---

Trying to set up tidy URLs for my personal website, I stumbled upon the following problem. My goal was to have a document `complete.html`, but only use the nicer-looking `/complete`-URL to refer to it. 

```apache
RewriteEngine On
RewriteRule ^complete /complete.html
```

However, this resulted in an Internal Server Error, which checking the logs turned out to be an infinite recursion. This is because the `RewriteRule ^complete` matches all URLs starting with `complete`, including, naturally, the `complete.html` it then redirects them to. Use `RewriteRule ^complete$` to match only URLs that are precisely `complete`, with nothing else following.
