---
layout: post
title:  "Making A Simple Static Website: Part Three, Using Jekyll with Github Pages"
categories: [tutorial, tech]
author: ada.wrong
excerpt_separator: <!--more-->
related-articles: [2020-11-16-simple-website-tutorial-part-one, 2020-11-23-simple-website-tutorial-part-two]
---

This is the third part of a multi-part series on creating your own static website for complete beginners. It will focus on using Jekyll with Github Pages and customizing Jekyll themes.<!--more--> In [part two]({% post_url 2020-11-23-simple-website-tutorial-part-two %}), we covered using git to save our work and Github Pages to host a webpage. Now, we will take our static site to the next level, making it easy to upload new content and manage a large number of web pages. By the end of the tutorial, you will have a static site setup similar to [this blog example](https://jekyll.github.io/minima/){:target="_blank"} or this [image grid example](https://www.jzhong.today/image-grid-example/){:target="_blank"}. Again, everything used to complete this tutorial is free! All you need is a computer (Mac, Windows, or Linux) and an internet connection.

<div class="row">
	<div class="col">
		<img class="img-fluid" src="/images/post_images/2021-1-21-simple-website-tutorial-part-three.md/minima.png" />
	</div>
	<div class="col">
		<img class="img-fluid" src="/images/post_images/2021-1-21-simple-website-tutorial-part-three.md/image-grid.png" />
	</div>
</div>

## Why do we need to use Jekyll? ##
After following part two, you now know how to create a basic web page with HTML and CSS. That would be fine for a simple website with only a few pages. However, as mentioned at the end of that part, what if you wanted to create a website that you are adding content to everyday? For example, if you were to create a blog site similar to this one, how would you keep all of your pages organized and consistent over a period of several years? How would you make an edit to the layout of the site, such as adding a new link to the navigation bar, without manually editing every single HTML file? This is where [Jekyll](https://jekyllrb.com/){:target="_blank"} comes in. Jekyll is a static site generator. This means that it is software that takes folders of files that are formatted in specific ways and uses them to generate the HTML and CSS files that build up your website. Static site generators make it easy for you to start adding content to your site and keep it organized.

There are other static site generators. We are using Jekyll because it is compatible with Github Pages, the free hosting service we are using. Jekyll can also be run on other hosting services. You can also use Jekyll to build your site locally, and then host the generated website files on any hosting service. So, even though we are using these specific software and platforms, you and your content are not locked to them forever.

Another reason to use Jekyll is the amount of community made themes available for use with it. If you are not interested in learning the details of web development technology or customizing your website, you can easily install a theme with Jekyll and just start posting content. If you are interested in customizing your website, it is easy to work off of pre-made themes and get them to exactly what you want. For example, this site was built off of [mint theme by aidewoode](https://github.com/aidewoode/jekyll-theme-mint){:target="_blank"}. You can see how different this site looks now compared to the theme it was built off of.

Finally, I wanted to include Jekyll in this tutorial series because I created an [image grid theme](https://github.com/jirrian/jekyll-theme-image-grid){:target="_blank"} that can be used with it. [Part one]({% post_url 2020-11-16-simple-website-tutorial-part-one %}) of this tutorial series covered reasons to learn web development; many of those reasons were inspired by my experience posting on instagram for several years. To address the specific needs of our online community, this theme was made to make it easy for instagram users to display their existing image-based content on their own self-made website. A customized version of this theme was also used in Virtualgoodsdealer's ["Deleted in 2020"](https://pages.virtualgoodsdealer.com/deleted2020/){:target="_blank"} web exhibit. So if you are interested in displaying your work in a similar way, follow this tutorial.

## Installing Ruby and Jekyll ##
In order to install and run Jekyll, we have to install [ruby](https://www.ruby-lang.org/en/){:target="_blank"}. Ruby is a programming language that Jekyll is built with. Before we install ruby, we are going to install [RVM](https://rvm.io/){:target="_blank"}. RVM or Ruby Version Manager allows you to easily install and manage different ruby environments on your system. Like part two, the installation instructions differ if you are using a Mac or a Linux subsystem with Windows 10. So, skip to the section for the operating system you are using.

### MacOS: Installing RVM ###
First, open your terminal window. [See part two if you need a refresher.]({% post_url 2020-11-23-simple-website-tutorial-part-two %}#macos-setting-up-bash)  
Check if you have GCC installed. [GCC](https://gcc.gnu.org/){:target="_blank"} is needed by RVM to compile the ruby versions.   
`gcc --version`   

You should see an output that says 'gcc' and a version number if it is already installed. If it is not installed, you will be prompted to install it bundled with Apple's Command Line Tools for Xcode. You can also install Apple's [Command Line Tools for Xcode](https://developer.apple.com/download/more/){:target="_blank"} through their developer website.

After installation, restart your terminal by quiting it and relaunching it. Run `gcc --version` again to verify that it has been installed.

Now, run the following command to install RVM.   
`curl -L https://get.rvm.io | bash -s stable`

After installation, restart your terminal and run `rvm --version` to verify that it has been installed. You should see an output that says "rvm" and some version numbers. We can now move on to [installing ruby]({% post_url 2021-1-21-simple-website-tutorial-part-three %}#installing-ruby).

[Source: Installing Ruby and Rails on Mac OSX](https://pragmaticstudio.com/blog/2010/9/23/install-rails-ruby-mac){:target="_blank"}

### Windows: Installing RVM ###
First, open your Ubuntu terminal window. [See part two if you need a refresher.]({% post_url 2020-11-23-simple-website-tutorial-part-two %}#windows-setting-up-bash)  

Run the following commands to install RVM.
`sudo apt-get install software-properties-common`   
`sudo apt-add-repository -y ppa:rael-gc/rvm`   
`sudo apt-get update`   
`sudo apt-get install rvm`

Add your Ubuntu user to RVM with the following command where "yourusername" is replaced with your Ubuntu username.   
`sudo usermod -a -G rvm yourusername`

After installation, restart your terminal by quiting it and relaunching it. Run `rvm --version` to verify that it has been installed. You should see an output that says "rvm" and some version numbers.

[Source: RVM package for Ubuntu](https://github.com/rvm/ubuntu_rvm){:target="_blank"}

### Installing ruby ###
Install ruby with RVM.       
`rvm install 2.7.2`   
This is installing version 2.7.2 of ruby. You can read more about the different versions of ruby available on the [ruby website](https://www.ruby-lang.org/){:target="_blank"}.

After installation, restart your terminal again. You want to tell rvm to use the version you just installed and not the default one that comes with your operating system.   
`rvm --default use 2.7.2`

Make sure that you are using the correct version of ruby by running `ruby -v`. You should see an output of "ruby 2.7.2p137".   

[Source: The Basics of RVM](https://rvm.io/rvm/basics){:target="_blank"}

### Installing Bundler and Jekyll ###
Jekyll is built with ruby. When you create your site with Jekyll, in order to generate the website files, Jekyll will use a lot of libraries of ruby code. In order for your Jekyll site to run properly, you need to have access to all the libraries of code that were used to create it. [Bundler](https://bundler.io/){:target="_blank"} is a software that will organize and install all of those libraries so you always have the correct dependencies installed. In ruby, libraries of code are called **gems**, so we will be using that terminology from now on.

Let's install Bundler and Jekyll.
`gem install bundler jekyll`

## Creating a new Jekyll site ##
Navigate to a folder that you would like to save your site in. In the previous part, we created the folder and git repo "yourgithubusername.github.io" for a Github Pages site (where "yourgithubusername" is your Github username). However, now that we are creating a site with Jekyll, we need to start over from scratch. You need to either delete the existing local folder and Github repo or rename them both to something else. If you decide to save your previous files and rename the repo on Github.com, [you will need to update the url of the remote repo in your local repo if you still want to push files from it](https://stackoverflow.com/questions/2432764/how-to-change-the-uri-url-for-a-remote-git-repository){:target="_blank"}.

Then, run the following command but replace "yourgithubusername" with your github username.
`jekyll new yourgithubusername.github.io`   
This will create a new basic Jekyll site in the folder "yourgithubusername.github.io".

### Running the Jekyll site locally ###
Navigate inside of the new folder with `cd yourgithubusername.io`. You should now see a bunch of files that make up your new Jekyll site.     
![photo of jekyll site folder](/images/post_images/2021-1-21-simple-website-tutorial-part-three.md/jekyll_new.png)

To test your site locally, run the following command in the **root** of your Jekyll site (directly inside the folder "yourgithubusername.github.io").   
`bundle exec jekyll serve`

After you see the text "Server running...", open your web browser and type `localhost:4000` in the address bar. After pressing enter, you should now see your new basic Jekyll site running locally.
From now on, use `bundle exec jekyll serve` to generate your website from your local files and view it in your browser. You should do this anytime you make changes to your files to make sure everything is working correctly.

### Hosting your site on Github Pages ###
Now we have to connect our new site to Github and host it on Github Pages. A lot of this process is going to be the same as what we covered in part two. In this part, I will go through the necessary steps quickly, but you can view the links to specific sections of part two for more details. First we need to create a new git repo and [make our first commit]({% post_url 2020-11-23-simple-website-tutorial-part-two %}#staging-and-commiting-changes).

Create a git repo in your new Jekyll site folder.   
`git init`

If you are using MacOS, open the `.gitignore` file in your code editor and add `**/.DS_Store` after all the text in the file. Then save and close the file.   
![photo of gitignore file](/images/post_images/2021-1-21-simple-website-tutorial-part-three.md/macos_gitignore.png)

Stage all of the changes to files in this folder.   
`git add .`

Check to see if the correct files are staged to be committed.   
`git status`

Commit all of the new files.
`git commit -m 'initial commit'`

Now we are going to [create a remote repo on github.com and push our new commit to it]({% post_url 2020-11-23-simple-website-tutorial-part-two %}#creating-a-repository-on-github).   
In a web browser, go to [github.com/new](https://github.com/new){:target="_blank"} to create a new github repository named "yourgithubusername.github.io" where "yourgithubusername" is replaced with your github username.

On the web page for your new repository, follow the instructions under "…or push an existing repository from the command line" and run the following commands.   
`git remote add origin https://github.com/yourgithubusername/yourgithubusername.github.io.git` (replace `yourgithubusername` with your github username)   
`git branch -M main`   
`git push -u origin main`   
Enter your Github login information when prompted. The web page for your repository should now be updated with the new files.

Finally, we have to [serve our new site on Github Pages]({% post_url 2020-11-23-simple-website-tutorial-part-two %}#setting-up-github-pages). In a web browser, go to the settings page for your new github repo (github.com/yourgithubusername/yourgithubusername.github.io/settings).   
Scroll down to the "Github Pages" section.   
Under "Source", click on the drop down that currently says "None" and change it to "main".   
Now, refresh the page and scroll back down to the "Github Pages" section. It should now say that your site is published. You can check the box next to "Enforce HTTPS".

Your new Jekyll site is now live at yourgithubusername.github.io and can be visited by anyone at that address! Github Pages is using the files in your remote repo to generate this site. From now on, everytime you push changes to Github, they will automatically be reflected on your live site. That's why it is important to test your site locally with `bundle exec jekyll serve` and going to `localhost:4000` on your web browser before pushing changes to Github.

## Using a basic Jekyll site ##
### Understanding the site directory structure ###
Now, let's take a closer look at some of the files that Jekyll uses to generate your website. You should see all of these files inside your project folder "yourgithubusername.github.io".
- `Gemfile` - file that [Bundler uses to install the necessary gems for your site](https://bundler.io/gemfile.html){:target="_blank"}
- `config.yml` - file that contains configuration settings for your Jekyll site
- `index.markdown` - file that is used to generate index.html (the default home page of your website).
- `_posts` - folder that all your files that represent posts will go inside

Check out the Jekyll documentation for [more information on the structure of the Jekyll site directory](https://jekyllrb.com/docs/structure/){:target="_blank"}.   
For an example of a Jekyll site project folder, check out [the github repo for this site](https://github.com/virtualgoodsdealer/virtualgoodsdealer.github.io){:target="_blank"}. We have more folders and files than your current basic Jekyll site. Note that we have seperate folders for storing images and audio files (`images` and `mp3`) in the root folder.

### Using front matter ###
Jekyll uses markdown files saved in specific folders to generate web pages. In order for a markdown file (files with .md or .markdown extentions) to be used by Jekyll, it must have a front matter. Open the `index.markdown` file in your code editor. The frontmatter is the two lines of dash characters and anything inside of them. [More on front matter in the Jekyll docs.](https://jekyllrb.com/docs/front-matter/){:target="_blank"}.
```markdown
---
layout: home
---
```
Markdown files in the root of your website directory, such as `index.markdown` and `about.markdown`, will be generated at yourgithubusername.github.io/index.html or yourgithubusername.github.io/about.html. The only value inside the frontmatter that is necessary for these files is "layout". That determines the layout that will be used to generate the corresponding web page. Depending on the theme you decide to use for your site, you may have to add more values in the front matter of your files than the examples in this tutorial (more on this later).   

### Adding a new page ###
If you run your site locally and go to `localhost:4000/about`, you will see the content inside `about.markdown`. Notice that the "layout" value in `about.markdown` is "page". This means that the about page is being generated with a layout called "page". If you want to add another **page** to your site (such as a contact page), copy the setup and frontmatter values of `about.markdown`.

For example, you could create a file `contact.md` and save it in the root of your website folder with the following content.
```markdown
---
layout: page
title: Contact
permalink: /contact/
---

Contact me at myemail@example.com
```
This new page would then be linked in the navigation bar at the top of the site and accessible at `localhost:4000/contact` or yourgithubusername.github.io/contact (this may vary depending on your theme and configuration settings). [More on pages here.](https://jekyllrb.com/docs/pages/){:target="_blank"}

### Adding a new post ###
Organizing and displaying text-based content is built into Jekyll sites with **posts**. Use posts to organize content that is dated (has a date attached to it). The most common usage for posts is blogging.

All posts must be saved in the `_posts` folder. Go inside that folder and you should see a markdown file for an example post. When adding a new post, you can copy the front matter in this example post.   
Post filenames must follow the specific format `yyyy-mm-dd-name-of-post.md`, where "yyyy-mm-dd" is replaced with the date of the post and the name of the post is seperated by dash characters.

For example, you could create your first post by creating a file named `2020-1-21-first-blog-post.md` and saving it inside the `_posts` folder with the following content inside the file.
```markdown
---
layout: post
title:  "My First Blog Post"
---

This is my first blog post!
```
Now, your post will be included in the home page's list of posts (this may vary depending on your theme) and also have it's own individual webpage.

### Adding content with markdown ###
You might have already noticed that any text after the front matter section becomes the content of your pages or posts. Markdown supports a large amount of formatting features such as bullet points, links, images, and headings. Check out the [Markdown Guide](https://www.markdownguide.org/basic-syntax/){:target="_blank"} for the syntax needed to format the content of your pages and posts.

## Installing a Jekyll theme ##
By now, you should have everything you need to start adding content to your basic Jekyll site. The next section of the tutorial will focus on changing the design of the site to fit your needs and tastes. To do this, we will install a Jekyll theme and customize it.

### Picking a theme ###
The rest of this tutorial's steps will reference a Jekyll theme that I created, [image grid](https://github.com/jirrian/jekyll-theme-image-grid){:target="_blank"},  If your content is mostly text, it would be better to use the many blog oriented themes available.

### Installing a gem-based theme to run locally ###

### Installing a theme to run on Github pages ###

## Customizing a Jekyll theme ##
### Editing layouts and styles ###

### Resources for customization ###
theme you are using's readme
Resources from part two
Jekyll docs
Liquid reference sheets

## Now it's up to you! ##