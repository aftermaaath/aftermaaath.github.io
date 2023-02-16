---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: id_Examples
title: Github Pages Note

# post specific
# if not specified, .name will be used from _data/owner/[language].yml
author: aftermath
# multiple category is not supported
category: useful_tools
# multiple tag entries are possible
tags: [github, html]
# thumbnail image for post
img: ":post_pic1.jpg"
# disable comments on this page
comments_disable: true

# publish date
date: 2023-02-17 17:58:06 +0900

# seo
# if not specified, date will be used.
#meta_modify_date: 2022-02-10 08:11:06 +0900
# check the meta_common_description in _data/owner/[language].yml
#meta_description: ""

# optional
# please use the "image_viewer_on" below to enable image viewer for individual pages or posts (_posts/ or [language]/_posts folders).
# image viewer can be enabled or disabled for all posts using the "image_viewer_posts: true" setting in _data/conf/main.yml.
#image_viewer_on: true
# please use the "image_lazy_loader_on" below to enable image lazy loader for individual pages or posts (_posts/ or [language]/_posts folders).
# image lazy loader can be enabled or disabled for all posts using the "image_lazy_loader_posts: true" setting in _data/conf/main.yml.
#image_lazy_loader_on: true
# exclude from on site search
#on_site_search_exclude: true
# exclude from search engines
#search_engine_exclude: true
# to disable this page, simply set published: false or delete this file
#published: false
---

<!-- outline-start -->
在做 Github Pages 的過程中用到的各種東西 / 遇到的問題。
<!-- outline-end -->

Outline:
- [挑 jekyll themes](#jekyll-themes)
- [在本地瀏覽網頁](#local-preview)
- [在網頁中使用 $LaTex$](#latex-use)
- [Code syntax highlighter](#code-highlight)
- [使用 disqus 做留言區](#disqus-comment)
- [繪圖軟體 -- Krita](#krita-use)

<hr>

<h4 id="jekyll-themes">挑 jekyll themes</h4>
可以到這裡找主題，蠻多免費又好看的主題可以挑：<br>
https://jekyll-themes.com/

接著就照網路上大部分的 tutorial，fork 它、把 repository name 改成 `username.github.io` 就可以了。

\_config.yml 的 url 也要改成 `https://username.github.io`
<hr>

<h4 id="latex-use">在網頁中使用 $LaTeX$</h4>
在 `header.html` 裡面加上：
```html
<script id="MathJax-script" defer src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
<script>
    MathJax = {
      tex: {
        inlineMath: [['$', '$'], ['\\(', '\\)']]
      }
    };
</script>
```
接著就可以用一般的方式使用了，
<p>$$f(x) = x^2$$</p>

<hr>
