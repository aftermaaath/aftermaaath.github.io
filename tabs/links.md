---
layout: links
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: id_links

# publish date (used for seo)
# if not specified, site.time will be used.
#date: 2022-03-03 12:32:00 +0000

# for override items in _data/lang/[language].yml
#title: My title
#button_name: "My button"
# for override side_and_top_nav_buttons in _data/conf/main.yml
#icon: "fa fa-bath"

# seo
# if not specified, date will be used.
#meta_modify_date: 2022-03-03 12:32:00 +0000
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


# you can always move this content to _data/content/ folder
# just create new file at _data/content/links/[language].yml and move content below.
###########################################################
#                Links Page Data
###########################################################
page_data:
  main:
    header: "Links"
    info: "Your Links page description."

  # To change order of the Categories, simply change order. (you don't need to change list order.)
  category:
    - title: "OnlineJudge"
      type: id_oj
      color: "gray"
    - title: "C++ Programming"
      type: id_programming
      color: "#007500"
    - title: "Other references"
      type: id_others
      color: "#003D79"

  list:
    -
    # C++ Programming
    - type: id_programming
      title: "C++ reference"
      url: "http://www.cplusplus.com/reference/"
      info: "C/C++ 的語法參考、各函式庫的用法參考。"
    - type: id_programming
      title: "OI wiki"
      url: "https://oi-wiki.org/"
      info: "與競程有關的知識整合網站，包含許多競賽常用演算法的知識、用法與常見題型。"

    # OnlineJudge
    - type: id_oj
      title: "MeowMeow OJ"
      url: "http://adalab.cs.nthu.edu.tw/"
      info: "清大競程課使用的 OJ，放了很多依主題分類的課程作業，以及往年比賽題目供練習。"
    - type: id_oj
      title: "Zerojudge"
      url: "https://zerojudge.tw/"
      info: ""
    - type: id_oj
      title: "AtCoder"
      url: "https://atcoder.jp/"
      info: ""
    - type: id_oj
      title: "Codeforces"
      url: "https://codeforces.com/"
      info: ""
    - type: id_oj
      title: "CSES"
      url: "https://cses.fi/"
      info: ""
    - type: id_oj
      title: "TIOJ"
      url: "https://tioj.ck.tp.edu.tw/"
      info: "建中的 OJ，有蠻多值得練習的題目。"
    - type: id_oj
      title: "SPOJ"
      url: "https://www.spoj.com/"
      info: ""

    # Other references
    - type: id_others
      title: "EdClub"
      url: ""
      info: ""
    - type: id_others
      title: "W3Schools"
      url: ""
      info: ""
    - type: id_others
      title: "Vim Cheat Sheet"
      url: ""
      info: ""
---
