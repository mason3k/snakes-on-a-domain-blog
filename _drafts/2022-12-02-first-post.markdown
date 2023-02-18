---
layout: single
title: "Write a Post"
date: 2022-12-02
categories: jekyll blogging
---

The goal of this article is to add some extra info
about blog writing with _Jekyll_.


## Display code snippets

You can display a block of code like the following using triple backticks.
You can also specify the language after the first triple backticks.

```python
def hello(name):
    return f"hello {name}"
```

## Add images

Create an `assets` folder where you can put all your images,
then display them with a link starting with an exclamative mark like this:
`![my inspiring image]({{ "assets/Snake_Undies.webp" | relative_url }})`.

![my inspiring image]({{ "/assets/Snake_Undies.png" | relative_url }})
_Photo by [Adventure Time](https://adventuretime.fandom.com/wiki/Snakes)_

Source: [Jekyll and Github Pages Tutorial](https://simondosda.github.io/posts/2021-09-16-blog-github-pages-4-custom.html)
