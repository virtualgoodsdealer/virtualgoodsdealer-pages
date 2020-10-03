# virtualgoodsdealer.github.com
virtualgoodsdealer pages repository

adapted from [aidewoode/jekyll-theme-mint](https://github.com/aidewoode/jekyll-theme-mint)

## Getting started (how to run a local version)
open the terminal

[install ruby with rvm](https://pragmaticstudio.com/blog/2010/9/23/install-rails-ruby-mac)
except remember use ruby ver 2.6.3
only go up to step #8

install bundler and jekyll
`gem install bundler jekyll`

clone this repository to where you want it
`git clone https://github.com/virtualgoodsdealer/virtualgoodsdealer.github.io.git`

try running the site locally
`bundle exec jekyll serve`

go to `localhost:4000` in your browser to see the site running locally. note that if you change the `_config.yml` file, you have to stop the local server (with ctrl-c) and rerun it for the changes to be reflected.

## Adding a new article
first, make a new branch for yourself or go to your branch

create a new article by adding a file `yyyy-mm-dd-title-of-article.md` in the `_posts` folder. the file name must be in this format and everything must be separated by dashes (no spaces).

open the file and fill out the following front matter:

```
layout: post
title: title of article
categories: category ((optional))
author: name ((optional))
```

if the article has multipled categories, write it in brackets.
```
categories: [category1, category2]
```

## Adding a new artist to the artist directory
add a new artist by adding a file `artistname.md` in the `_artists` folder. the file name should be the artist's name but no period characters or spaces (use dashes instead of spaces).

open the file and fill out the following front matter:
```
title: name
permalink: /artistdirectory/artistname
name: name ((optional))
website: store url ((optional))
shop: store url ((optional))
instagram: instagram username ((optional))
twitter: twitter username ((optional))
photo: artistname.jpg
```

`title` should be the same as `name`.

for `permalink`, after `/artistdirectory/` enter the artist markdown file name.
the photo filename should also the same as the artist markdown file name.

urls need to include `https://` or `http://`.
for instagram and twitter, only enter the username for that site (not the full url)

please note that if the artist is also an author of articles, the `name` field in the `artistname.md` file must match with the `author` field in the article files for them to be linked.

save the artist photo in the `images/artist_images` folder.

## Adding a new article category page
add a new category page so that all the articles with that category can show up on its own page. to do this, add a file `categoryname.md` in the `_category` folder.

open the file and fill out the following front matter:
```
tag: categoryname
permalink: /articles/categoryname
```

