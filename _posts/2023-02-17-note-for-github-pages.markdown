---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: id_Examples
title: Github Pages Note

# post specific
# if not specified, .name will be used from _data/owner/[language].yml
author: aftermaaath
# multiple category is not supported
category: useful_tools
# multiple tag entries are possible
tags: [github, html]
# thumbnail image for post
img: ":post_pic1.jpg"
# disable comments on this page
comments_disable: true

# publish date
date: 2023-02-15 17:58:06 +0900

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

#### Outline
- [挑 jekyll themes](#jekyll-themes)
- [在本地瀏覽網頁](#local-preview)
- [在網頁中使用 $LaTeX$](#latex-use)
- [Code syntax highlighter](#code-highlight)
- [使用 disqus 做留言區](#disqus-comment)
- [繪圖軟體 -- Krita](#krita-use)

<br><hr>

<h4 id="jekyll-themes">挑 jekyll themes</h4>

可以到這裡找主題，蠻多免費又好看的主題可以挑：[JEKYLL THEMES](https://jekyll-themes.com/)

接著就照網路上大部分的 tutorial，fork 它、把 repository name 改成 `username.github.io` 就可以了，把 `username` 換成自己的 Github username。

\_config.yml 的 url 也要改成 `https://username.github.io`
<br><hr>

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
接著就可以用一般的方式使用了，例如寫 `$x^2 + y^2 = z^2$` 會變成 $x^2 + y^2 = z^2$；寫 `$$f(x) = x^2$$` 會變成：
<p>$$f(x) = x^2$$</p>

值得注意的是，如果在 markdown 中使用的話，`$x$` 與 `$$x$$` 皆會被視為單行，且如果內容包括含有其他意義的字元（例如 `|something|+|another thing|` 可能會被視為表格），輸出可能會跟預期不同。這時候可以用 `<p></p>` 之類的 html tag 把它包起來就不會出問題了，像是：
```html
<p>$x$</p>
```

<br><hr>
