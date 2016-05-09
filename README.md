# The Crimsonian
---

Welcome the the main repository for [crimsonian.com](http://crimsonian.com), your new blogging engine powered by [Jekyll](http://jekyllrb.com/) and hosted via [Github Pages](https://pages.github.com/). Adding new content to the site is as easy as editing a text file. Below, I'll cover some of the most common tasks you'll perform when working with this set of tools.

* [Directory Structure](https://github.com/crimsonian/crimsonian.github.io/blob/master/README.md#directory-structure)
* [Adding New Posts](https://github.com/crimsonian/crimsonian.github.io/blob/master/README.md#adding-new-posts)
* [Intro to Markdown](https://github.com/crimsonian/crimsonian.github.io/blob/master/README.md#brief-intro-to-markdown)
  * [Headers](https://github.com/crimsonian/crimsonian.github.io/blob/master/README.md#1-headers)
  * [Links](https://github.com/crimsonian/crimsonian.github.io/blob/master/README.md#2-links)
  * [Emphasis](https://github.com/crimsonian/crimsonian.github.io/blob/master/README.md#emphasis)
  * [Images](https://github.com/crimsonian/crimsonian.github.io/blob/master/README.md#images)
  * [Using Flickr for Images](https://github.com/crimsonian/crimsonian.github.io/blob/master/README.md#using-flickr-for-images)


## Directory Structure

In general, the directory structure looks something like this...

    .
    ├── _includes
    ├── _layouts
    ├── _posts
    |   ├── 2007-10-29-some-post.md
    |   └── 2009-04-26-welcome.md
    ├── about.md
    └── index.html


When adding new content to the site, you really only need to concern yourself with the files that end with `.md`. These are "Markdown" files and denote content pages that are formatted with a lightweight markup language designed to make writing both easy and powerful. You can think of Markdown like HTML's laid-back cousin.

You can do lots of cool stuff with Markdown but its not required either– the site will employ sensible defaults where you've not added any specific formatting. But, if you need to use links, add images, etc. Markdown will make your life easier without having to remember the specifics of HTML.

## Adding New Posts

The majority of your content will come from Markdown files located within the `_posts` directory. Similar to other blogging platforms, a "post" is a timely piece of content that shows up on the homepage of the site (the most recent post will show up first).

Once you've created your content and are ready to publish it to the site, the process of creating a new post is simple... 

1. Create a new file in the `_posts` directory named according to the following format... `2016-01-01-this-is-my-title.md`
1. Add YAML front-matter to the beginning of the file. Front-matter looks like the following (denoted by 3 hypens before and after) and is used to provide additional detail for the site such as layout, title and date-time the content was posted. _NOTE: The front-matter is required, so don't forget it!_

<pre>---
layout: post
title:  "This is the title of my post"
date:   2016-05-10 13:05:14 +0400
---</pre>

## Brief Intro to Markdown

As mentioned before, Markdown is intended to make your life easier by providing some simple methods to format your content in typical ways. Things like links, lists, italiziced or bolded text are super easy to implement in a forgiving way, decreasing the likelihood of screwing up the site layout by forgetting to properly close your HTML tags. Here are some of the most common things you'll be doing in Markdown but you can see a comprehensive list of everything it supports [right here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

### 1. Headers

To create a header, simply place a hash character (`#`) at the beginning of the line. The number of hashes you use will determine which heading to render.

    # This is an H1

    ## This is an H2

    ### This is an H3... you get the idea

When using this convention, you'll see three header elements rendered on the page, like so...

> # This is an H1
> ## This is an H2
> ### This is an H3... you get the idea


### 2. Links

You can create a link in Markdown by using two square brackets and parenthesis, like so...

    [This is text that will be clickable](http://google.com/)

When using this convention, you should see a link rendered on the page, like so:

> [This is text that will be clickable](http://google.com/)

### 3. Lists

Lists are where Markdown really shines. By placing a numeric value or asterisk at the beginning of the line, your text will automatically be rendered as an ordered or unordered list...

    1. First ordered list item
    2. Another item
    ⋅⋅* Unordered sub-list. 
    1. Actual numbers don't matter, just that it's a number
    ⋅⋅1. Ordered sub-list
    4. And another item.

    ⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

    ⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
    ⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅
    ⋅⋅⋅(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

    * Unordered list can use asterisks
    - Or minuses
    + Or pluses

And this is what it will look like, rendered on the page...

> 1. First ordered list item
2. Another item
⋅⋅* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
⋅⋅1. Ordered sub-list
4. And another item.

> ⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

> ⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅
⋅⋅⋅(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

> * Unordered list can use asterisks
- Or minuses
+ Or pluses

### Emphasis

You can bold or italicize content by wrapping word(s) in asterisks or underscores. Consider the following examples...

    Emphasis, aka italics, with *asterisks* or _underscores_.  
    Strong emphasis, aka bold, with **asterisks** or __underscores__.  
    Combined emphasis with **asterisks and _underscores_**.  
    Strikethrough uses two tildes. ~~Scratch this.~~

And here all that is, rendered on the page...

> Emphasis, aka italics, with *asterisks* or _underscores_.  
> Strong emphasis, aka bold, with **asterisks** or __underscores__.  
> Combined emphasis with **asterisks and _underscores_**.  
> Strikethrough uses two tildes. ~~Scratch this.~~

### Images

Images are the best! They're almost identical to links, except that you have to put an exclamation point in-front. You can render an image within Markdown by adhering to the following convention, the site will take care of the rest...

    ![](https://farm4.staticflickr.com/3434/3206727133_e0726cb7b9_q.jpg)

If you've ever fooled HTML for images, this should be a refreshing change of pace. This is what it looks like rendered on the page...

> ![](https://farm4.staticflickr.com/3434/3206727133_e0726cb7b9_q.jpg)

### Using Flickr for Images

While you can use the above method to easily add markup for images, getting those online in an accessible place might be a little trickier. You can certainly use this repository to host your images if you want but a better solution would be to use Flickr to host your images and simply copy the embed code from there and paste it into your posts. While Markdown is generally preferable for quick content creation, the site does still support basic HTML.

Here's a quick example of using Flickr to generate an image tag...

![](https://help.yahoo.com/library/YAHOO/IMAGES/AGIFs/agif_flkr_htmlembed_en_02.gif)

The above GIF was pulled from Yahoo's help section. For more information on this solution, checkout the following resource... [https://help.yahoo.com/kb/flickr/sln22515.html](https://help.yahoo.com/kb/flickr/sln22515.html)

The only catch to this approach is ensuring that you use an image larger than 750 pixels wide. Because the layout is responsive, using an image of this size should allow the site to resize the image according to the width of the user's device.
