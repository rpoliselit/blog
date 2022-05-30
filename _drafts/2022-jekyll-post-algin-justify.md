---
layout: post
title: "How to change content align in posts by using Jekyll"
categories: Jekyll
tags: [en-us, jekill, html]
toc: true
---

não saber muito de html, querer que meus posts fiquem assim por padrão
farei por padrão, e para uma linha especifica no markdown

- [] contextualizar meu problema

## What is Jekyll?

O doutor que se torna o monstro
O framework utilizado no GithubPages

- [] apresentar
- [] colocar o link para o jekill

## Change align by default

```
mkdir _layouts
touch post.html
```


```html
---
layout: default
---

<div class="post-content e-content" itemprop="articleBody" style="text-align: justify">
    {{ content }}
</div>
```

`right`, `left`, `center`, `justify`

- [] caso não tenha a pasta _layout
- [] caso tenha a paste por ter pegado algum tema

## Change align of a paragraph

```
This is your paragraph. Your text is here. This is a text block.
{: style="text-align: justify" }
```

```
{: style="text-align: justify" }
This is your paragraph. Your text is here. This is a text block.
```

`right`, `left`, `center`, `justify`

- [] explicar q esse é no arquivo markdown
- [] pode ser em cima ou em baixo