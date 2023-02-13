a page just for fun.

subpage
link: tabs/link.md<br>
about: tabs/about.md<br>
post: \_post<br>
home: 
archive: \_layouts/archives.md<br>

## Structure of the files and directories
### \_data
#### conf
- main.yml <br>
General settings, such as langauage, fonts, cookies...
- others.yml <br>
Settings for each subpages
- posts.yml <br>
Settings for posts, such as query and share.

#### const
- contact.yml <br>
Contact info constants. Including icon, url.
- share.yml <br>
Share links constants.

#### lang
Language settings. Every settings that have something to do with language.
Such as texts to display, date form, and so on.

#### owner
Personal information, such as brand name, name, other titles.

### \_layouts
main file(.md) of each pages.

### tabs
md files for every subpages.

### \_include
#### default
##### header/header.html
header for each .html
##### footer.html
footer for each .html
