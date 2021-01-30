# virtualgoodsdealer.github.io
live at [pages.virtualgoodsdealer.com](https://pages.virtualgoodsdealer.com/)

[jekyll](https://jekyllrb.com/docs/) generated site. theme adapted from [aidewoode/jekyll-theme-mint](https://github.com/aidewoode/jekyll-theme-mint) and using [bootstrap](https://getbootstrap.com/docs/4.5/getting-started/introduction/).

## Getting started (how to run a local version)
open the terminal

[install ruby with rvm](https://pragmaticstudio.com/blog/2010/9/23/install-rails-ruby-mac)
except remember to use ruby ver 2.6.3. only go up to step #8 in the linked tutorial.

install bundler and jekyll
`gem install bundler jekyll`

clone this repository to where you want it
`git clone https://github.com/virtualgoodsdealer/virtualgoodsdealer.github.io.git`

install all the gems needed for the repository
`bundle install`

go inside the repo folder and try running the site locally
`bundle exec jekyll serve`

go to `localhost:4000` in your browser to see the site running locally. 

from now on, you only need to go inside the repo folder and run `bundle exec jekyll serve` to test the site in your browser. note that if you change the `_config.yml` file, you have to stop the local server (with ctrl-c) and rerun it for the changes to be reflected. otherwise, you can just refresh the browser.

## Adding a new article
first, go to article drafts branch or make a new one

create a new article by adding a file `yyyy-mm-dd-title-of-article.md` in the `_posts` folder. the file name must be in this format and everything must be separated by dashes (no spaces).

open the file and fill out the following front matter:

```
---
layout: post
title: title of article
categories: category ((optional))
author: name ((optional))
related-articles: [article file name] ((optional))
---
```

if the article has multipled categories, write it in brackets.
```
categories: [category1, category2]
```

the `related-articles` value is for a list of related articles that you definitely want to be listed underneath this article. list the article filenames without the markdown extension.
```
related-articles: [yyyy-mm-dd-title-of-article]
```   
the max number of articles shown under a post is 3. if there is less than 3 related articles listed in the front matter, the latest posts in the same categories as the article will be displayed. if that still doesn't reach 3 articles, the most recent posts on the pages site will be displayed.

then, insert the content of the article below the front matter. 

### Article excerpts
the main articles pages display an excerpt of the article text that is taken from the first paragraph by default. if you want the preview text to be shorter, add a custom excerpt separator to the article markdown file's frontmatter.
```
---
layout: post
title: title of article
categories: category ((optional))
author: name ((optional))
related-articles: [article file name] ((optional))

excerpt_separator: <!--more-->
---
```
then, insert `<!--more-->` after where you want the preview to cut off in the article's content.

[jekyll doc example](https://jekyllrb.com/docs/posts/#post-excerpts)

## Adding a new creator to the creator directory
first, go to artist bios branch or create a new one

add a new creator by adding a file `creatorname.md` in the `_creators` folder. the file name should be the creator's name but no period characters or spaces (use dashes instead of spaces).

open the file and fill out the following front matter:
```
---
title: name
permalink: /creatordirectory/creatorname
name: name ((optional))
website: website or store url ((optional))
shop: virtualgoodsdealer.com store page ((optional))
instagram: instagram username ((optional))
twitter: twitter username ((optional))
photo: creatorname.jpg
donationlink: url of donation link ((optional))
---
```

`title` should be the same as `name`.

for `permalink`, after `/creatordirectory/` enter the creator markdown file name.
the photo filename should also the same as the creator markdown file name.

website and donationlink urls need to include `https://www.` or `http://www.`.
for instagram and twitter, only enter the username for that site (not the full url)

only use shop if the creator's products are active on virtualgoodsdealer.com. enter the tag of their category on the virtualgoodsdealer.com shop.

please note that if the creator is also an author of articles, the `name` field in the `creatorname.md` file must match with the `author` field in the article files for them to be linked.

save the creator photo in the `images/creator_images` folder.

then, insert the bio of the creator below the frontmatter.

## Adding a new article category page
first, make a new branch for yourself or go to your branch

add a new category page so that all the articles with that category can show up on its own page. to do this, add a file `categoryname.md` in the `_category` folder.

open the file and fill out the following front matter:
```
tag: categoryname
permalink: /articles/categoryname
```

## Adding a new submissions page
first, go to submissions branch or create a new one

add a submissions page by adding a file `submissionscallname.md` in the `_submissions` folder. the file name should be revelant to the submissions call title but no period characters or spaces (use dashes instead of spaces).

open the file and fill out the following front matter:
```
---
layout: submissions
title:  title of submissions call
permalink: /submissions/submissionscallname
date: yyyy-mm-dd
open: true
---
```

the date is used to sort the submissions by most recent.

set `open` to "true" if the submissions call is open. set it to "false" if the call is closed.

## Pushing changes
push changes to your current branch and then create a merge request on the github website.

## Helpful quick links
[markdown guide](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) for formatting article content

[jekyll docs](https://jekyllrb.com/docs/)

