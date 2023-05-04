---
layout: projects
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: id_projects

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
image_viewer_on: true
# please use the "image_lazy_loader_on" below to enable image lazy loader for individual pages or posts (_posts/ or [language]/_posts folders).
# image lazy loader can be enabled or disabled for all posts using the "image_lazy_loader_posts: true" setting in _data/conf/main.yml.
image_lazy_loader_on: true
# exclude from on site search
#on_site_search_exclude: true
# exclude from search engines
#search_engine_exclude: true
# to disable this page, simply set published: false or delete this file
published: false

###########################################################
#                Projects Page Data
###########################################################
page_data:
  main:
    header: "Notes"
    info: "Your note page description."
    text_color: "white"
    # if you don't want to use background image, comment it. back_color will be activated.
    img: ":title.jpg"
    back_color: "#003060"

  category:
    - title: "Example"
      type: id_example
      color: "gray"
    - title: "Picture"
      type: id_picture
      color: "#62b462"
    - title: "Quote"
      type: id_quote
      color: "#2FD0ED"

  list:
    # example
    - type: id_example
      project_name: "Example Project"
      project_excerpt: "Examples"
      img: ":post_pic1.jpg"
      img_title: "img title1"
      date: "2021-03-13"
      post: "projects/sample.md" 

    # picture
    - type: id_picture
      project_name: "Example Project"
      project_excerpt: "Picture"
      img: ":post_pic1.jpg"
      img_title: "img title2"
      date: "2021-04-23"
      post: "projects/sample.md"

    # quote
    - type: id_quote
      project_name: "Example Project"
      project_excerpt: "Mahatma Gandhi "
      img: ":post_pic1.jpg"
      img_title: "img title6"
      date: "2021-12-20"
      post: "projects/sample.md"
---
