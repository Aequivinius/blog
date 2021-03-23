---
layout: post
title: Teaching Programming Using git
published: true
tags: git teaching python pytest
---

In 2021, I designed and taught an introductory course in `python` programming for linguists at the University of Innsbruck. I wanted to try out something different, so I decided to run the whole course over `git`, using `fork` and `pull request` as means to distribute and let students hand in exercises, and `actions` to grade them automatically.

## Course Structure

For every exercise, I created a directory that contains usually a `.md` explaining some of the concepts used in the exercise, a `example.py` that demonstrates those concepts and the actual exercise, provided as a scaffold `.py` with a corresponding `_test.py`. The tests are written for `pytest`, which is very straight forward and runs tests automatically when invoked with `pytest`.

The `action` is configured in such a way that everytime a `pull request` is issued, `pytest` is run. Like this, submissions can be easily checked.
