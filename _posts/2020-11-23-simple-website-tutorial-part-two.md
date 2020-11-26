---
layout: post
title:  "Making A Simple Static Website: Part Two, Setting Up Your Development Environment and Workflow for Github Pages"
categories: [tutorial, tech]
author: ada.wrong
excerpt_separator: <!--more-->
---

This is the second part of a multi-part series on creating your own static website for complete beginners. It will focus on setting up your development environment and the workflow for using github pages.<!--more--> I will also suggest resources for developing the actual website using HTML and CSS. Again, everything used in this tutorial is free! All you need is a computer (Mac, Windows, or Linux) and an internet connection to get started. If you haven't already, check out [part one]({% post_url 2020-11-16-simple-website-tutorial-part-one %}) for why we are coding our own website.

## Overall Project Structure ##
In the previous part, I listed the technologies/frameworks this tutorial will cover:
- bash
- git
- github and github pages
- jekyll (optional)

Now, I will explain the purpose of each part on extremely basic terms. If you are already familiar with these terms, you can skip to the next section. Also, please note that I'm not an expert (if you think I'm saying anything technically wrong, [please email me](mailto:jillianzhong@gmail.com)).

The goal is to have a static website viewable from any web browser. To do this, we need a hosting service. That is why we are using Github Pages. Github Pages is a hosting service offered by Github where files you upload to their servers can easily be served as websites. This service is free and we are even currently using it to host this site. In order to get our files on Github, we need to use git to upload them. [Git](https://git-scm.com/){:target="_blank"} is a version control software where you can track changes to every file in a project. It is really convenient for projects with many files, working with others on the same project, or if you are like me and get confused easily. 

When using git, a project folder that you are tracking with git is called a **repository**. [Github](https://github.com/){:target="_blank"} is a hosting service website that provides hosting for git repositories. You can think of it as the Google Drive for git repositories. Basically, use git to track your local file changes, then upload the files to Github so they can be accessed through the internet, then set up Github Pages so those files can be viewed as a webpage.

There are many ways to use git. This tutorial will cover using it through the bash shell. A shell is a program that interprets text commands and executes them. If you heard the term "command line" before, it is referring to the commands entered to be interpreted by a shell. Bash is a shell that is installed on many UNIX and UNIX-like systems such as MacOS and Ubuntu (operating systems used in this tutorial).

There is a learning curve for modern computer/smartphone users, but I still recommend learning this because of the amount of documentation available online for bash users. Although there are [many softwares available for using git](https://git-scm.com/downloads/guis){:target="_blank"}, I think using git through bash is the most common way of using git. It also works well with creating a local host to test your site locally and installing other frameworks if you want to continue to learn more and expand your website. For example, later we will be using bash to install and run jekyll (more on that in the next part).

I also wanted to make this tutorial useful for both Windows and MacOS users. Instead of making a separate parallel tutorial with different commands and clients for Windows users, I decided to concentrate on getting everyone to a UNIX or UNIX-like operating system and using bash. That said, the next part differs depending on if you are using MacOS or Windows. So skip to the section for the operation system you are using.

## MacOS: Setting up bash and git ##
### Setting up bash ###
If you are using any MacOS before MacOS Catalina, bash should be the default shell on your computer. You can check what OS you are running by clicking the Apple logo on the top left of your screen and then "About this Mac". If you are using Catalina, the default shell used by Terminal is zsh, but you can easily switch to bash.

Search for "Terminal" in your Applications and open it.

You should see something like this:   
![image of terminal](/images/post_images/2020-11-23-simple-website-tutorial-part-two.md/terminal.png)   
If it does not say "bash" at the top of the window and says "zsh" instead, type run this command to change the default shell to bash:   
`chsh -s /bin/bash`

The rectangle on the last line of text is the cursor. When you type commands, the text should appear in front of it. To run a command, press the enter key on your keyboard.

After running that command, it will prompt you for your system password (the password you use to login to your Mac). Type your password and press enter. Text characters will not appear on your screen when entering your password. Then, close the Terminal window and open it again. You should now be running the bash shell. Check that it says "bash" at the top of the Terminal window like the image above.   
[Source: "How to Change the Default Shell to Bash in MacOS Catalina" from howtogeek.com](https://www.howtogeek.com/444596/how-to-change-the-default-shell-to-bash-in-macos-catalina/#:~:text=From%20System%20Preferences&text=Hold%20the%20Ctrl%20key%2C%20click,Zsh%20as%20your%20default%20shell.){:target="_blank"}


We will be using this terminal window to run all our commands from now on. You can also install other terminal applications that include more features. I use [iterm2](https://iterm2.com/){:target="_blank"} instead of the Terminal application. I recommend using it but it's completely optional!


### Setting up git ###
Now, it's time to set up git. Check to see if you already have git installed by running this command in Terminal.   
`git version`

If it outputs "git version" and a version number, then you already have git installed and you can skip to the next section. If the git command is not recognized, we are going to install it through [Homebrew](https://brew.sh/){:target="_blank"}, a package manager for MacOS.   

To install Homebrew, you need to have Apple's XCode command line tools installed.   
`xcode-select --install`

After running that command, there should be a popup window that guides you through the installation process for XCode command line tools. Then, install Homebrew with the following command.
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Follow the command line prompts to finish the installation. Then, run this command to install git through Homebrew:   
`brew install git`   
[Source: Homebrew documentation](https://brew.sh/)   
[Source: Github git guide](https://github.com/git-guides/install-git)

After the installation is complete, use `git version` to make sure it has been installed. Now you should be ready to use git and Github!

## Windows: Setting up bash and git ##
### Setting up bash ###
If you are using a Windows operating system, it's a bit more complicated to set up bash. We are going to use a feature called "Windows Subsystem for Linux" that allows us to run Linux programs on Windows 10. Then, we will install Ubuntu, a Linux operating system, which includes the bash shell. This solution only works for Windows 10 64-bit. If you are using Windows 7, [you can upgrade to Windows 10 for free](https://www.theverge.com/2020/1/14/21065140/how-to-upgrade-microsoft-windows-7-10-free-os){:target="_blank"} or try using a client like [git for Windows](https://gitforwindows.org/){:target="_blank"}.

Search "Control Panel" in the Start Menu and open it. Go to "Programs" and then "Turn Windows Features On Or Off". In the "Windows Features" window, check the box next to “Windows Subsystem for Linux” and click "OK".   
Wait for the files to install and restart your computer when prompted.

After your computer boots up again, go to the Microsoft Store. Here you can install different Linux distributions. For this tutorial we are using [Ubuntu](https://www.microsoft.com/en-us/p/ubuntu/9nblggh4msv6?activetab=pivot:overviewtab){:target="_blank"}.

Click "Get" to install the program. After installation, search "Ubuntu" in the Start Menu and open the program. The first time you open this program, it will run some installations. Wait a bit and it will prompt you to create a UNIX username and password. This is specific to your Ubuntu installation and isn't related to your Windows username and password. Press enter after typing to submit your username and password.

After following the prompts, you should see something like this:   ss   

We will be using this terminal window to run all our commands from now on. The blinking rectangle on the last line of text is the cursor. When you type commands, the text should appear in front of it. To run a command, press the enter key on your keyboard.   
[Source: "How to Install and Use the Linux Bash Shell on Windows 10" from howtogeek.com](https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/){:target="_blank"}   
[Source: Ubuntu Windows 10 Tutorial](https://ubuntu.com/tutorials/ubuntu-on-windows#5-launch-ubuntu-on-windows-10){:target="_blank"}

### Setting up git ###
Git is included with the Ubuntu distribution. Run the command `git version` to verify that it has been installed. It should output the text "git version" and a version number.

Remember that this Ubuntu distribution is running as a subsystem on your Windows system. Use the command `pwd` to find out what directory you are in.
ss   
You probably do not recognize this file location because it is inside the newly created filesystem for your Ubuntu distribution.

Use the command `cd ..` to move to the directory that is the parent of the current directory. `cd foldername` will move you to that folder (replace `foldername` with the name of a folder). `..` means the parent of the current directory whereas `.` means the current directory.   
Use `cd ..` again to move up one more level.
Then use the command `ls` to list all the files in the current directory.   
ss   
You should see a folder called `/mnt`. This folder contains your Windows filesystem.   
Use `cd /mnt` to move to it. You should now see folders for the familiar drives that hold all your files.   
ss   

If you want to edit your files outside of the Ubuntu terminal, make sure your files are saved in your Windows filesystem (within the folders in the `/mnt` folder). It is **not** recommended to edit any of the files in the Ubuntu distribution filesystem with any Windows software. Later you will probably be editing files with Windows software installed on your computer such an image editing software or a text editor, so it's best to keep your website files in the Windows filesystem.   
[Source: "How to Access Your Ubuntu Bash Files in Windows" from howtogeek.com](https://www.howtogeek.com/261383/how-to-access-your-ubuntu-bash-files-in-windows-and-your-windows-system-drive-in-bash/){:target="_blank"}

Our goal is to use Github and upload and download files from it easily; however by default when using Windows Subsystems for Linux, we cannot make changes to a folder within the `/mnt` folder from within the Ubuntu terminal because of file permissions. To solve this issue, we are going to run the following two commands. Note that if you have multiple drives, make sure to replace the `c` with the letter of the drive folder you are using. After running the first command, you may be prompted to enter the UNIX account password you just created.    
`sudo umount /mnt/c`   
`sudo mount -t drvfs C: /mnt/c -o metadata`

For example, I'm using my **D** drive so I ran:   
`sudo umount /mnt/d`   
`sudo mount -t drvfs D: /mnt/d -o metadata`   
[Source: "How to solve 'Operation not permitted' on cloning repository" from askubuntu.com](https://askubuntu.com/questions/1115564/wsl-ubuntu-distro-how-to-solve-operation-not-permitted-on-cloning-repository){:target="_blank"}   
[Source: Chmod/Chown WSL Improvements](https://devblogs.microsoft.com/commandline/chmod-chown-wsl-improvements/){:target="_blank"}

Now you should be ready to use git and Github!

## Basic git and Github ##
As mentioned in the first section, git is a version control software for tracking changes to files. Github is a hosting service website where you can upload your git repositories. Now, we are going to be creating our first git repository on our local filesystem, creating a repository on Github, connecting the two repositories, then uploading our first files to Github.

From now on, I will refer to the git repository (repo for short) on your local filesystem as **local** and the repository hosted on github.com as **remote**. It's important to keep track of the difference between the two because your changes won't reflect across them automatically. Think of it as files on your computer vs. files on Google Drive. If you edit a photo on your computer, the latest version won't be on Google Drive unless you upload it yourself. If your friend uploads a new photo to a shared Google Drive folder, you won't have it on your computer unless you download it first.

### Creating a Github account ###
First, you need a Github account. In a web browser, go to [github.com](https://github.com/){:target="_blank"} and sign up for an account. Keep in mind that your username may be important to your final Github Pages site. Unless you are using a custom domain name, the url of your site will be "yourgithubusername.github.io" where "yourgithubusername" is your Github username. However, you can purchase a domain name at any time and connect it to your Github Pages site so it's not a huge deal. Go to [jirrian.github.io](https://jirrian.github.io){:target="_blank"} for an example.

### Setting your git identity ###
To start making commits with git, we need to set a username and email. From within your terminal window, run the following command to set a username for git (replace `yourgitusername` with your name or username of choice). This is not the same thing as your Github username and it does not have to be the same.   
`git config --global user.name "yourgitusername"`   
Then, add your email with the following command (replace `youremailaddress@example.com` with your email address).   
`git config --global user.email youremailaddress@example.com`

This information is used in every git commit. The `--global` **flag** sets this user information for all git repositories on your machine.   
[Source: Setting your username in Git](https://docs.github.com/en/free-pro-team@latest/github/using-git/setting-your-username-in-git#:~:text=Git%20uses%20a%20username%20to,same%20as%20your%20GitHub%20username.){:target="_blank"}

### Creating a local git repository ###
Now we need to create a local folder where our website files will be saved. From within the terminal window, navigate to a folder in your file system that you typically save documents in, such as the "Documents" folder.

#### How to navigate through your filesystem in the terminal ####
Use the `pwd` command to see what folder you are currently in.   
Use the `cd foldername` command to move into a folder (replace `foldername` with the name of a folder).   
Use `cd ..` to move to the parent of the current folder. There is a lot more to using `cd`, see [the top solution on this page](https://askubuntu.com/questions/607413/when-to-use-a-preceding-slash-in-path-names-e-g-for-the-cd-command){:target="_blank"} to read more about specifying absolute or relative paths for folder names.   
Use the `ls` command to list every file in the folder you are currently in.

There are a lot of commands you can use to do basically anything you are used to doing on your graphical user interface for browsing files (Finder in MacOS or File Explorer in Windows). If you want to find a command for something, just use a search engine to search "unix" and what you want to do and you will find documentation on how to do it. For example, I want to find out how to list all the files in a folder including hidden files, so I Googled "unix view all hidden files".   
![image of google search](/images/post_images/2020-11-23-simple-website-tutorial-part-two.md/googlingcommands.png)   
The first result gives me the answer, which is the command `ls -a`. There is a lot of documentation online as well as solutions to common issues on [Stack Overflow](https://stackoverflow.com/){:target="_blank"} or [Ask Ubuntu](https://askubuntu.com/){:target="_blank"}. Be aware that while a lot of the commands are available on all UNIX operating systems, some commands are specific to Linux distributions and some are specific to macOS, so you may need to do more research if a command isn't working on your terminal. One example is `open` on macOS and `xdg-open` on Linux.

#### Initiating the local git repository ####
So, now you are ready to create the folder where your website files are going to be saved. The name for the folder is based on 2 conventions. First, it's easiest to make the name of the local folder that contains your git repository match the name of the remote repository on github.com. Second, the Github repository you are using to serve a Github Pages site must be named "yourgithubusername.github.io" where "yourgithubusername" is replaced with your github username.   
For example, the name for our Github (organization) account is "virtualgoodsdealer", so the repository for this site's files on Github is named "virtualgoodsdealer.github.com". Since I always match my local and remote repo names, I named my local folder "virtualgoodsdealer.github.io".

Run the following commands to create the folder and move into it.   
`mkdir yourgithubusername.github.io`   
`cd yourgithubusername.github.io`

Then initiate a git repository in this folder:   
`git init`   
You should see an output like "Initialized empty Git repository in ..."

#### Installing a code editor ####
So now we have our git repository initiated, but how do we start creating files to add to it? We need to install a code editor. A code editor is a program for editing files that contain code. You can think of it like Microsoft Word but for code. There are many code editors out there; some popular free ones are [Microsoft VS Code](https://code.visualstudio.com/){:target="_blank"}, [Atom](https://atom.io/){:target="_blank"}, and [Sublime Text](https://www.sublimetext.com/){:target="_blank"}. I use Sublime Text because it's light and simple and works for the scope of projects I am doing. I would recommend it for this project if you are a beginner. If you want to be a super nerd, I recommend learning how to use [vim](https://www.vim.org/){:target="_blank"}. It's a command line editor that is already installed on most UNIX systems. I still like using this editor but I **do not** recommend using it if this is your first time using a code editor because of the amount of commands you have to remember. Personally, I hate Microsoft VS Code and Atom confuses me but you can choose whatever you are comfortable with. Everyone has their own preferences and in the end it doesn't matter for this project as long as you are able to open and save files.

#### Creating a .gitignore file ####
Now, we need to create a **.gitignore file**. A .gitignore file is a file that contains a list of folders and files that you want git to ignore. Any file or folder that is listed will not be tracked as part of git's version control system. The contents of this file really depends on the languages and frameworks you are using in your program. Mostly, it is used so that specific files that are generated by operating systems or frameworks are not uploaded to Github. For the barebones website we are creating in this part of the tutorial you only need to add content if you are using a Mac.

Run the following command in your terminal.
`touch .gitignore`   
Then navigate to the folder that holds your local repo and open the .gitignore file in your code editor. If you are using a file browser program (Finder or File Explorer), you may need to enable viewing hidden files in the program settings to see the file.

Add the text `.DS_Store` to the file. Then, save and close.   
![image of .gitignore file](/images/post_images/2020-11-23-simple-website-tutorial-part-two.md/gitignore.png)   
This is mainly to ignore a file that is generated on MacOS systems but it's good to add it even if you aren't using MacOS in case you work with someone that does on the repo. Here is [a collection of .gitignore file templates](https://github.com/github/gitignore){:target="_blank"} for different programming languages and frameworks that you can use depending on your project.

#### Staging and commiting changes ####
Now we have our first new file, but we have to save this change to git. Use the `git status` command to see the status of your git repo.   
The output should look something like the image below. Keep in mind your terminal window will look different from mine if you are using Ubuntu on Windows or a different terminal application.      
![image of git status command](/images/post_images/2020-11-23-simple-website-tutorial-part-two.md/gitstatus.png)  
The output says there are no new changes you can currently save to git but there are changes in **untracked files**. This is because we created a new .gitignore file but that file is currently not being tracked by git.

Use the `git add .` command to add all changes to files in the current folder to the **staging area**. `.` means the current folder; however, you can add individual files to be staged with `git add filename` (replace `filename` with the name of the file).      
Then, run `git status` again. All the changes that are in the staging area will be listed under the text "Changes to be committed".
![image of git add . command](/images/post_images/2020-11-23-simple-website-tutorial-part-two.md/gitaddthis.png)   
Now, you can see that the creation of the .gitignore file is **staged**. When a change is staged, it is marked as being ready to be saved. So, make sure you are only staging changes that you want to keep.

Now, we are going to **commit** our staged changes. After doing so, the staged changes will be included in an entire snapshot of the git repo. This snapshot, also referred to as a **commit**, is saved by git. Think of this as the equivalent of saving changes to a file. This is why you must only stage changes you want to commit. However, the whole purpose of using git is to add version control to your project, so you can always roll back to a past commit.

Run the following command to commit your staged changes.   
`git commit -m 'description of commit'`   
You should write a detailed description of the commit within quotations so you can understand at a glance what changed in each commit.
![image of git commit command](/images/post_images/2020-11-23-simple-website-tutorial-part-two.md/gitcommit.png) 

You just made your first git commit! Since the .gitignore file was included in the lastest snapshot of your git repo, the file is now being tracked by git. From now on, when we are staging changes, git will ignore the folder referenced in the .gitignore file. Repeat the steps in this section everytime you want to save changes to your project files to your local git repo.

### Creating a repository on Github ###
We committed changes to our local git repo, but now we have to get those changes onto Github. In a web browser, go to [github.com/new](https://github.com/new){:target="_blank"} to create a new github repository.

Under "Repository name", enter "yourgithubusername.github.io" where "yourgithubusername" is replaced with your github username. Keep everything else at the default settings. Then, click "Create Repository".

### Connecting the local repository to the Github repository ###
You should now be redirected to the web page for your new github repository. Follow the instructions under "…or push an existing repository from the command line" and run the following commands.   
`git remote add origin https://github.com/yourgithubusername/yourgithubusername.github.io.git` (replace `yourgithubusername` with your github username)   
`git branch -M main`   
`git push -u origin main`   
The output will prompt you to enter your Github username and password. Text characters will not appear on your screen when entering your password. Just type it and press enter. Note that this is your Github account username and password (what you use to login to github.com).

Now your local git repo is connected to your remote github repo and set to **push** changes to it and **fetch** updates from it. Your latest commit is also now reflected on your github repository. Refresh the web page and you should see your .gitignore file there. Congrats on pushing to github for the first time!

From now on, you can use the command `git push origin main` to push your local git commits to your remote github repo. Think of this as the equivalent of uploading a new version of a file to Google Drive.

There is so much more functionality to git and I only gave you the basic commands you need to get this working. If you are interested in learning more or need to look up how to do something, check the [git documentation](https://git-scm.com/docs){:target="_blank"} for a list of commands or read articles from the [Pro Git Book](https://git-scm.com/book/en/v2){:target="_blank"}. We briefly learned the concepts of commit, push, and remote. Some basic concepts you should eventually learn are clone, push, fetch, merge, pull, and branches.

Another thing you can set up is [connecting to Github with SSH](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/connecting-to-github-with-ssh){:target="_blank"} so you do not have to enter your Github username and password everytime you push to the remote repo.

## A barebones website and resources to get started ##

## Serving your Github Pages site ##