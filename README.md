# virtualgoodsdealer.github.io
live at [pages.virtualgoodsdealer.com](https://pages.virtualgoodsdealer.com/)

[jekyll](https://jekyllrb.com/docs/) generated site. theme adapted from [aidewoode/jekyll-theme-mint](https://github.com/aidewoode/jekyll-theme-mint) and using [bootstrap](https://getbootstrap.com/docs/4.5/getting-started/introduction/).

## Getting started (how to run a local version)
open the terminal

check that you have gcc installed  
`gcc --version`

check that you have git installed  
`git --version`

install rvm  
`curl -L https://get.rvm.io | bash -s stable`

check that rvm was installed  
`rvm --version`

install ruby ver 2.6.3  
`rvm install 2.6.3`

set 2.6.3 as the default ruby version  
`rvm --default use 2.6.3`

install bundler and jekyll
`gem install bundler jekyll`

clone this repository to where you want it
`git clone https://github.com/virtualgoodsdealer/virtualgoodsdealer-pages.git`

install all the gems needed for the repository
`bundle install`

go inside the repo folder and try running the site locally
`bundle exec jekyll serve`

go to `localhost:4000` in your browser to see the site running locally. 

from now on, you only need to go inside the repo folder and run `bundle exec jekyll serve` to test the site in your browser. note that if you change the `_config.yml` file, you have to stop the local server (with ctrl-c) and rerun it for the changes to be reflected. otherwise, you can just refresh the browser.

## Adding a new article
create a new article by adding a file `yyyy-mm-dd-title-of-article.md` in the `_posts` folder. the file name must be in this format and everything must be separated by dashes (no spaces).

open the file and fill out the following front matter and content:

```
---
layout: post
title: title of article
categories: category ((optional))
author: name ((optional))
guest: guestname ((optional - for interview posts ))
related-articles: [article file name] ((optional))
---

Insert text content of article here.
```
please note that the `author` field must match with the `name` field in the `creatorname.md` creator file for them to be linked.   
if the article has multiple authors, write them in brackets.
```
author: [name1, name2]
```

if the article has multiple categories, write it in brackets.
```
categories: [category1, category2]
```

the `guest` value is for interview posts only. put the name of the guest that is being interviewed here. this field must match with the `name` field in a `creatorname.md` creator file for them to be linked.

the `related-articles` field is for a list of related articles that you definitely want to be listed underneath this article. list the article filenames without the markdown extension.
```
related-articles: [yyyy-mm-dd-title-of-article]
```   
the max number of articles shown under a post is 3. if there is less than 3 related articles listed in the front matter, the latest posts in the same categories as the article will be displayed. if that still doesn't reach 3 articles, the most recent posts on the pages site will be displayed.

then, insert the content of the article below the front matter. 

### Article excerpts/descriptions
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

You can also write a separate post description that will only show up on the main articles page.
```
---
layout: post
title: title of article
categories: category ((optional))
author: name ((optional))
related-articles: [article file name] ((optional))

post_description: Description of post is here!!!!
---
```

### Adding media to posts
all media for posts (images, mp3 files, video files) go in the `assets/post_media` folder.

create a folder with the file name (without extension) of the corresponding post inside `assets/post_media`.

add all media for that post into that folder. for example, add all media used in `_posts/yyyy-mm-dd-title-of-article.md` into `assets/post_media/yyyy-mm-dd-title-of-article/`

reference the media in the post markdown file with `/assets/post_media/yyyy-mm-dd-title-of-article/nameoffile.jpg` where "nameoffile.jpg" is your image file.

### Embedding Youtube videos
Add the embed URL of the Youtube video within `src`.
```
{% include youtube-video-embed.html src="..." %}
```
### Embedding Videos
Add the path to the video within `src` and the path to the thumbnail image within `poster`.
```
{% include video-embed.html poster="..." src="..."%}
```
### Embedding Audio
Add the path to the audio file within `src`. Add a caption that will be displayed above the player by adding text within `caption`.
```
{% include open-embed.html caption="Add Your Caption Here" src="..." %}
```
## Adding a new exhibit
create a new exhibit by adding a file `yyyy-mm-dd-title-of-exhibit.md` in the `_posts` folder. the file name must be in this format and everything must be separated by dashes (no spaces).

open the file and fill out the following front matter:
```
---
layout: exhibit
title: title of exhibit
author: name
author_description: description of author of exhibit ((optional))
post_description: description of exhibit
demo: /assets/exhibit_previews/name_of_exhibit/name_of_exhibit_preview.mp4
demo_poster: /assets/exhibit_previews/name_of_exhibit/name_of_exhibit_preview_poster.png
link: url of exhibit
permalink: /exhibits#title-of-exhibit
---
```
please note that the `author` field must match with the `name` field in the `creatorname.md` creator file for them to be linked.   
if the article has multiple authors, write them in brackets.
```
author: [name1, name2]
```
the `author_description` field is only used if the creator of the exhibit does not have a corresponding creator page. for example, there may be several creators that worked on the exhibit. some or all can be listed in the `author` field but they may want their collective name to be used for the exhibit page display. in that case, use the `author_description` field to display the collective name instead of the individual creators. a combination of text and links can be used in this field.

`demo` and `demo_poster` fields have the path to a video of the exhibit and the path to the preview image of the video. for the image and video files, create a new folder in `/assets/exhibit_previews` with the name of the exhibit. place the image and video file in that folder.

the url for the `link` field needs to include `https://www.` or `http://www.`.

## Adding a new creator to the creator directory
add a new creator by adding a file `creatorname.md` in the `_creators` folder. the file name should be the creator's name but no period characters or spaces (use dashes instead of spaces).

open the file and fill out the following front matter and content:
```
---
title: name
permalink: /creatordirectory/creatorname
name: name

shop: virtualgoodsdealer.com store page ((optional))

website: website url ((optional))
blog: blog url ((optional))
instagram: instagram username ((optional))
twitter: twitter username ((optional))
facebook: facebook username ((optional))
bandcamp: bandcamp url ((optional))
soundcloud: soundcloud url ((optional))
spotify: spotify url ((optional))
patreon: patreon url ((optional))
gumroad: gumroad url ((optional))
tiktok: tiktok url ((optional))
itch: itch.io url ((optional))

photo: creatorname.jpg
donationlink: url of donation link ((optional))
---

Insert bio of creator here.
```

`title` should be the same as `name`.

for `permalink`, after `/creatordirectory/` enter the creator markdown file name.
the photo filename should also the same as the creator markdown file name.

website, donation link, bandcamp, spotify, soundcloud, patreon, and gumroad urls need to include `https://www.` or `http://www.`.
for instagram and twitter, only enter the username for that site (not the full url)

only use shop if the creator's products are active on virtualgoodsdealer.com. enter the tag of their category on the virtualgoodsdealer.com shop.

please note that if the creator is also an author of articles, the `name` field in the `creatorname.md` file must match with the `author` field in the article files for them to be linked.

save the creator photo in the `assets/creator_images` folder.

then, insert the bio of the creator below the frontmatter.

## Adding a new article category page
add a new category page so that all the articles with that category can show up on its own page. to do this, add a file `categoryname.md` in the `_category` folder.

open the file and fill out the following front matter:
```
---
tag: categoryname
permalink: /articles/categoryname
---
```

## Adding a new submissions page
add a submissions page by adding a file `submissionscallname.md` in the `_submissions` folder. the file name should be revelant to the submissions call title but no period characters or spaces (use dashes instead of spaces).

open the file and fill out the following front matter and content:
```
---
layout: submissions
title:  title of submissions call
permalink: /submissions/submissionscallname
date: yyyy-mm-dd
open: true
---

Insert submission description here.
```

the date is used to sort the submissions by most recent.

set `open` to "true" if the submissions call is open. set it to "false" if the call is closed.

## Workflow and Pushing changes
check for new updates to master branch/live site  
`git checkout master`  
`git pull origin master`

create new branch for updates you are working on  
`git checkout -b newbranch`

make your changes and test locally with `bundle exec jekyll serve` and then going to `localhost:4000` in your browser

check the status of your changes to see what files were changed  
`git status`

stage and commit all your changes to the new branch you are on
`git add .`  
`git commit -m 'description of changes made`

push your changes to github, creating a remote version of the branch you created
`git push origin newbranch`

go on the github website and create a pull request to merge `newbranch` with master

if there are no conflicts, click "merge" inside the pull request to merge into master and make your changes live

changes will be live on [https://pages.virtualgoodsdealer.com/](https://pages.virtualgoodsdealer.com/) in around 15 minutes

## Helpful quick links
[markdown guide](https://www.markdownguide.org/cheat-sheet/) for formatting article content

[bootstrap lead](https://getbootstrap.com/docs/4.0/content/typography/#lead)   
[bootstrap figure](https://getbootstrap.com/docs/4.0/content/figures/)

[jekyll docs](https://jekyllrb.com/docs/)

