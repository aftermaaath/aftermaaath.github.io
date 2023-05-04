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
#published: false

###########################################################
#                Projects Page Data
###########################################################
page_data:
  main:
    header: "Notes"
    info: "Your note page description."
    text_color: "white"
    # if you don't want to use background image, comment it. back_color will be activated.
    # img: ":post_pic1.jpg"
    back_color: "purple"

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
      post: |
        # Examples

        This is an example page to display markdown related styles for Mr. Green Jekyll Theme.

        ### Headings (centered)
        {:data-align="center"}

        # Heading 1

        ## Heading 2

        ### Heading 3

        #### Heading 4

        ##### Heading 5

        ###### Heading 6

        ***

        ### Paragraphs

        #### Paragraph

        **William Shakespeare**, Let me not to the marriage of true minds
        Admit impediments. Love is not love
        Which alters when it alteration finds,
        Or bends with the remover to remove.
        O no, it is an ever-fixed mark
        That looks on tempests and is never shaken;
        It is the star to every wand'ring barque,
        Whose worth's unknown, although his height be taken.
        Love's not Time's fool, though rosy lips and cheeks
        Within his bending sickle's compass come;
        Love alters not with his brief hours and weeks,
        But bears it out even to the edge of doom.
        If this be error and upon me proved,
        I never writ, nor no man ever loved.

        #### Texts

        Quoted text `Hello world`

        Bold text **Hello world**

        Italic text _Hello world_

        kbd text <kbd>Hello world</kbd>

        #### Blockquote

        > **William Shakespeare**, Let me not to the marriage of true minds
        Admit impediments. Love is not love
        Which alters when it alteration finds,
        Or bends with the remover to remove.
        O no, it is an ever-fixed mark
        That looks on tempests and is never shaken;
        It is the star to every wand'ring barque,
        Whose worth's unknown, although his height be taken.
        Love's not Time's fool, though rosy lips and cheeks
        Within his bending sickle's compass come;
        Love alters not with his brief hours and weeks,
        But bears it out even to the edge of doom.
        If this be error and upon me proved,
        I never writ, nor no man ever loved.

        ### Link

        This is [Mr. Green Jekyll Theme](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme), a simple theme built for [Jekyll](https://jekyllrb.com/).

        ### Picture

        ![such a lovely place](:projects-heading.jpg)

        ### Picture (centered)

        ![such a lovely place](:project1_thumb.jpg){:data-align="center"}

        ### Lists

        - Apple
        - Banana
        - Orange

        1. Fruits
            1. Apples
                - Granny Smith
                - Mutsu
            1. Bananas
                - Cavendish
                - Red
        1. Vegetables

        ***

        ### Tables

        #### Small Table (centered)

        | Fruits(not aligned) | Alignment (centered) | num (right align) |
        | ------------------- | :------------------: | ----------------: |
        | Apple               |       centered       |              9999 |
        | Banana              |  centered long text  |               999 |
        | Orange              |       centered       |                99 |
        | Lemon               |       centered       |                 9 |
        {:data-align="center"}

        #### Wide Table (centered)

        scroll enabled when page is narrow

        | Fruits | num (left align) | num (right align) | num  | num  | num  |
        | ------ | :--------------- | ----------------: | ---- | ---- | ---- |
        | Apple  | 1111             |              1111 | 2222 | 3333 | 4444 |
        | Banana | 111              |               111 | 222  | 333  | 444  |
        | Orange | 11               |                11 | 22   | 33   | 44   |
        | Lemon  | 1                |                 1 | 2    | 3    | 4    |
        {:data-align="center"}

        #### Wider Table

        scroll enabled when page is narrow

        | Fruits | num (left align) | num (right align) | num  | num  | num  | num  | num  | num  |
        | ------ | :--------------- | ----------------: | ---- | ---- | ---- | ---- | ---- | ---- |
        | Apple  | 1111             |              1111 | 2222 | 3333 | 4444 | 5555 | 6666 | 7777 |
        | Banana | 111              |               111 | 222  | 333  | 444  | 555  | 666  | 777  |
        | Orange | 11               |                11 | 22   | 33   | 44   | 55   | 66   | 77   |
        | Lemon  | 1                |                 1 | 2    | 3    | 4    | 5    | 6    | 7    |

        ### Code

        #### Quote

        ```python
        for i in range(5, 10):
          print(i)
        ```

    # picture
    - type: id_picture
      project_name: "Example Project"
      project_excerpt: "Picture"
      img: ":post_pic1.jpg"
      img_title: "img title2"
      date: "2021-04-23"
      post: |
        # Title
        This is project content.

        ![Image](:project2_thumb.jpg)

    # quote
    - type: id_quote
      project_name: "Example Project"
      project_excerpt: "William Shakespeare"
      #img: ":project1_thumb.jpg"
      #img_title: "img title3"
      date: "2021-05-27"
      post: |
        Let me not to the marriage of true minds
        Admit impediments. Love is not love
        Which alters when it alteration finds,
        Or bends with the remover to remove.
        O no, it is an ever-fixed mark
        That looks on tempests and is never shaken;
        It is the star to every wand'ring barque,
        Whose worth's unknown, although his height be taken.
        Love's not Time's fool, though rosy lips and cheeks
        Within his bending sickle's compass come;
        Love alters not with his brief hours and weeks,
        But bears it out even to the edge of doom.
        If this be error and upon me proved,
        I never writ, nor no man ever loved.
    - type: id_quote
      project_name: "Example Project"
      project_excerpt: "Albert Einstein"
      img: "post_pic1.jpg"
      img_title: "img title4"
      date: "2021-06-08"
      post: |
        Two things are infinite: the universe and human stupidity; and I'm not sure about the universe.
    - type: id_quote
      project_name: "Example Project"
      project_excerpt: "Mae West"
      img: "post_pic1.jpg"
      img_title: "img title5"
      date: "2021-08-20"
      post: |
        You only live once, but if you do it right, once is enough.
    - type: id_quote
      project_name: "Example Project"
      project_excerpt: "Mahatma Gandhi "
      img: "post_pic1.jpg"
      img_title: "img title6"
      date: "2021-12-20"
      post: |
        Be the change that you wish to see in the world.
---
