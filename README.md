# Stutz Medien Theme folder and file structure #

This is a very opinionated base theme for WordPress, created from several iterations of the themes of our projects in production. It is based on the WordPress recommendation. 

Although WordPress themes technically only need two files (index.php and style.css), they usually consist of many files. This means they can quickly become confusing! This can help you organise your themes.
---

## Theme folder structure

```
├─┬ assets
│ ├── css
│ ├── images
│ ├── js
│ └── vendor
├── inc
├── languages
├─┬ template-parts
│ ├── footer
│ ├── header
│ ├── navigation
│ ├── page
│ └── post
└── page-templates 
```

## Root Files 
```
404.php
archive.php
comments.php
footer.php
front-page.php
functions.php
header.php
index.php
page.php
rtl.css
screenshot.png
search.php
searchform.php
sidebar.php
single.php
style.css
…
team.txt
```
---
## assets
The assets folder contains the CSS, JavaScript, image files aswell as vendor files. 
This folder can contain an SCSS folder that contains other folders with SCSS files if it is to be used.
Put external files in the vendor folder so that you do not confuse them with your own files.

## inc
The inc folder contains the PHP functions of the theme. The functions.php simply contains all these files. The functions should be grouped in different files.

```actions.php``` all add_action() calls.
```cache-functions.php``` all functions which work with transients.
```filter-functions.php``` functions which are called by add_filter().
```filters.php``` the add_filter() calls.
```front-page-panel-functions.php``` all functions which have to do with the front page panels feature.
```template-functions.php``` all functions which are not directly called from template files but cannot be grouped into other files.
```template-tags.php``` functions which are called from template files.
```theme-updates.php ``` functions to provide automatic theme updates.

## languages
It is recommended to internationalise your theme so that it can be translated into other languages. These standard themes contain the languages folder, which contains a .pot file for translation and all translated .mo files. The name of this folder is languages by default, but you can change it. If you do, you need to update load_theme_textdomain().
https://developer.wordpress.org/themes/functionality/internationalization/ 
https://developer.wordpress.org/reference/functions/load_theme_textdomain/

## template-parts
The template-parts folder contains the theme's template pieces. It is structured in other folders for more clarity and structure. You can create or edit your own folders if needed. Just make sure you update the folder path in the files when you call a template.
https://developer.wordpress.org/reference/functions/get_template_part/

## page-templates 
The page-templates folder contains the page templates that can be applied to a specific page or a group of pages. WordPress recognises the page-templates subfolder. Therefore, it is a good idea to store your global page templates in this folder to keep them organized.
https://developer.wordpress.org/themes/template-files-section/page-template-files/

## 404.php
File Template for displaying Error 404 pages 
https://codex.wordpress.org/Creating_an_Error_404_Page

## archive.php
File Template for displaying archive pages. You can display archive title (tag, category, date-based, or author archives).
There are other archive files you can use, see the archive structure: https://developer.wordpress.org/files/2014/10/Screenshot-2019-01-23-00.20.04.png
https://developer.wordpress.org/themes/basics/template-hierarchy/

## comments.php
Template File that displays comments in your theme.
https://developer.wordpress.org/themes/template-files-section/partial-and-miscellaneous-template-files/comment-template/

## footer.php
File Template for displaying the Footer. It is called when using the wp_footer()
https://developer.wordpress.org/themes/basics/template-hierarchy/

## front-page.php
If there is a front-page.php file in the theme, this template is always used for the start page. Without the template file, either home.php (blog index) or page.php (static start page) is loaded as normal.
https://developer.wordpress.org/themes/basics/template-hierarchy/#home-page-display

## functions.php
In WordPress, functions.php or the theme functions file is a template included in WordPress themes. It acts like a plugin for your WordPress site that's automatically activated with your aIn WordPress, functions.php or the theme functions file is a template included in WordPress themes. It acts like a plugin for your WordPress site that's automatically activated with your current theme.
https://developer.wordpress.org/themes/basics/theme-functions/

## header.php
This is the template that displays all of the <head> section and everything up until main. It is called when using the wp_header().
https://developer.wordpress.org/themes/basics/template-hierarchy/

## index.php
Display a list of posts in excerpt or full-length form. Choose one or the other as appropriate. Include wp_link_pages() to support navigation links within posts.
https://developer.wordpress.org/themes/basics/template-hierarchy/

## page.php
File Template for displaying single pages
https://developer.wordpress.org/themes/basics/template-hierarchy/#single-page


## rtl.css
Adding support for language written in a Right-To-Left (RTL) direction.
https://codex.wordpress.org/Right-to-Left_Language_Support

## screenshot.png
The new WordPress screenshot size for themes is 1200×900px. The official WordPress Codex or WordPress Docs recommends that during theme development you must create a screenshot for your theme.
https://codex.wordpress.org/Theme_Development#Screenshot

## search.php
File template for displaying search results pages. Display a list of posts in excerpt or full-length form. Choose one or the other as appropriate.
https://developer.wordpress.org/themes/basics/template-hierarchy/#search-result

## searchform.php
File Template for searchform.php template. It is Used any time that get_search_form() is called.
https://developer.wordpress.org/reference/functions/wp_unique_id/
https://developer.wordpress.org/reference/functions/get_search_form/

## sidebar.php
The Theme should be widgetized as fully as possible. Any area in the layout that works like a widget (tag cloud, blogroll, list of categories) or could accept widgets (sidebar) should allow widgets.
You can need to use multiple files to organize multiple sidebars.
https://developer.wordpress.org/themes/functionality/sidebars/

## single.php
File Template for displaying single posts
https://developer.wordpress.org/themes/basics/template-hierarchy/#single-post

## style.css

