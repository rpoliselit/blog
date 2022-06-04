---
layout: post
title: "How to change content alignment in posts by using Jekyll"
categories: Web
tags: [en-us, jekyllrb, html]
toc: true
---

My familiarity with markup languages ​​is almost nil. I thought that by creating the blog with [Jekyll](https://jekyllrb.com) I could completely get rid of the need to write html, and it would just copy a template. Well, I found out that it is not so. The template I chose had no justified alignment. Thought I could put some kind of markup in markdown to solve this. I was wrong again. So something will always be needed to know about html. In that case, reading and editing html are necessary at least.

Looking for the answer to my problem, I learned the necessary to solve it, and here is the ready answer. There are at least three ways to change the alignment of the blog:

- align only one paragraph,
- align only the posts as layout,
- align the whole blog by default.

## Text alignment of a paragraph

Html codes can be included in markdown's syntax, and it is also encouraged. Thus not only the alignment such as other characteristics can be changed by using html tags.

Here are three ways to do it in the markdown file:

```html
<div style="text-align: justify">
    This is your paragraph. Your text is here. This is a text block.
</div>
```

```
This is your paragraph. Your text is here. This is a text block.
{: style="text-align: justify" }
```

```
{: style="text-align: justify" }
This is your paragraph. Your text is here. This is a text block.
```

The text alignment options are `right`, `left`, `center` and `justify`.

## Text alignment of the posts as layout

When a Jekyll site is created there is not a layout directory with a post.html file which one determines the layout of all your posts in blog. Let us add it with the following commands in the terminal:

```
mkdir _layouts
touch post.html
```

Fill the post.html with the following codes:

```html
---
layout: default
---

<div class="post-content e-content" itemprop="articleBody" style="text-align: justify">
    {{'{{ content' }} }}
</div>
```

Done! All the posts now are with the same text alignment.

In the case of using a template, just look for the part of posts.html that appears `{{'{{ content' }} }}`, and add `style="text-align: justify"` to the div tag.

## Text aligment of the whole blog by default

The alignment of the entire blog can be done as described in the previous section, but instead of editing post.html, edit default.html at layout directory. If in doubt, just read the documentation [here](https://jekyllrb.com/docs/layouts/).