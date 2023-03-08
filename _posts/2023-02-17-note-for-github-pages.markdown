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
img: ":github_pages_note.jpg"
# disable comments on this page
#comments_disable: true

# publish date
date: 2023-02-23 14:47:08 +0900

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
在使用 jekyll 做 Github Pages 的過程中用到的各種東西 / 遇到的問題。
<!-- outline-end -->

#### Outline
- [挑 jekyll themes](#jekyll-themes)
- [在網頁中使用 $LaTeX$](#latex-use)
- [Code syntax highlighter](#code-highlight)
- [使用 disqus 做留言區](#disqus-comment)

<br>
<hr>

<h4 id="jekyll-themes">挑 jekyll themes</h4>

可以到這裡找主題，蠻多免費又好看的主題可以挑：[JEKYLL THEMES](https://jekyll-themes.com/)

接著就照網路上大部分的 tutorial，fork 它、把 repository name 改成 `username.github.io` 就可以了，把 `username` 換成自己的 Github username。

`_config.yml` 的 url 也要改成 `https://username.github.io`

<br>
<hr>

<h4 id="latex-use">在網頁中使用 $LaTeX$</h4>

在要使用 $LaTeX$ 的 html 的 `<head></head>` 中加入下列程式碼。在大部分 jekyll theme 中，可以找到一個叫做 `header.html` 的檔案，即為所有頁面 `head` 中的內容。因此我們在 `header.html` 裡面加上：

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
<p>$$f(x) = x^2$$</p>
```

<br>
<hr>

<h4 id="code-highlight">Code syntax highlighter</h4>

這邊是使用 rouge 作為 Markdown 的 Code syntax highlighter，首先在 `_config.yml` 中加入下列設定：
```yaml
markdown: kramdown
highlighter: rouge
```

接著在終端機輸入：
```
rougify style theme > assets/css/syntax.css
```
將上述的 theme 替換成喜歡的主題名稱，主題在[這個網頁](https://spsarolkar.github.io/rouge-theme-preview/)可以預覽。

<br>

最後在 <head></head>（`header.html`）中加入：
```html
<link href="{{ site.baseurl }}/assets/css/syntax.css" rel="stylesheet" >
```

<br>

至此就設定完成了。在使用的時候，下列兩種用法都可以：
~~~

```cpp
#include <iostream>
using namespace std;

int main(){
    return 0;
}
```

~~~

```
{% raw %}
{% highlight cpp %}
#include <iostream>
using namespace std;

int main(){
    return 0;
}
{% endhighlight %}
{% endraw %}
```

<br>
<hr>

<h4 id="disqus-comment">使用 disqus 做留言區</h4>

首先到 [disqus](https://disqus.com/) 註冊並登入，接著點擊 "Get started" 並選擇 "I want to install Disqus on my site"。照著它要求的步驟做就好了，這邊只提及要注意的地方：

1.
使用 jekyll 的話，要注意設定中要將評論開啟，並對 disqus 做設定。即 disqus 中提到的：
```html
---
layout: default
comments: true
# other options
---
```

可能不一定長這樣。像我這邊是這樣設定的：
```html
comments:
    engine: "disqus"
```

總之根據原本的檔案設定好就好。如果是 fork 下來的 theme，應該都有清楚的指示。

<br>

2.
Disqus 給的 Universal Embed Code 中有兩行需要自己更改的部分：
```javascript
this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
```
將這兩行更改為如下即可：
```javascript
this.page.url = '<%= page.permalink %>';
this.page.identifier = '<%= page.path %>';
```

<br>

3.
如果希望可以 display comment count，依照指示將<br>
`<script id="dsq-count-scr" src="//shortname.disqus.com/count.js" async></script>`<br>
加到 `body` 中（`footer.html`）。接著將 `#disqus_thread` 加到你希望它顯示的地方。

要注意部分是在 localhost 看的時候似乎不能正常顯示，以及放上去的時候要等好一陣子才會跑出來。<br>
如果一直沒跑出來，先不要跟我一樣以為自己寫錯，很可能只要
<br><br>
![](https://i.imgur.com/ydtJdpS.png)
<br><br>
就會成功了。
