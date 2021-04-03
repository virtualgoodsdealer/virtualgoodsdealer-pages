---

layout: post

title: "Making With GIMP: Patterns, Textures, and Text"
categories: [tutorial]
author: saqmemes
related-articles:
post_description: [How drawing certain boundaries between you and your higher self may reveal your true potential. Plus the one thing you should know before next voyage]

---

![Dots](\assets\post_media\2021-3-31-gimp-tutorial\intro\dotpattern1.jpg "GIMP patterns")

# Table of Content
1. [What You Will Learn To Make](/articles/2021/03/26/making-with-gimp-part-one/#in-this-tutorial)
2. [Why GIMP?](/articles/2021/03/26/making-with-gimp-part-one/#audio-transcription)
3. [Getting Started]
  - [Preparing Your local Folder Tree]
  - [Locating GIMP's Patterns Folder]
4. [Navigating GIMP]
  - Layers Window
  - The Toolbox


# In This Tutorial:
I will tell you about the different types of patterns I learned to make using GIMP, and show you step-by-step, how to make each design into your own creation. This is a complete beginner’s guide, as I, too, am a beginner. I hope this tutorial will help you become more familiar with GIMP's interface and toolboxes. By the end, you should be able to create something similar to each of the following examples:

<div class="row">
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/feathers-portrait.jpg/whyihatefacebook_post1.png'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/pikachloe-portrait-geen.jpg'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/trash-portrait.jpg/whyihatefacebook_post3.png'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/square-portrait-4.jpg/whyihatefacebook_post4.png'>
  </div>
</div>





# Why GIMP?
I got by as a content creator by making most of my content in my phone, using a combination of the following mobile photo editors:

- [Phonto](https://phon.to/download){:target="_blank"}: for text editing
- [PicsArt](https://picsart.com/){:target="_blank"}: for cropping/blending/enhancing images
- [Background eraser](https://play.google.com/store/apps/details?id=com.handycloset.android.eraser&hl=en_US&gl=US){:target="_blank"}: for its auto erase tool
- [IbisPaint X](https://ibispaint.com/?lang=en-US){:target="_blank"}: for brushes and other drawing tools
- [Cut+Mix Studio](https://play.google.com/store/apps/details?id=pictriev.cutout&hl=en_US&gl=US){:target="_blank"}: for layering/affining/face swapping
- [Mirrorlab](https://play.google.com/store/apps/details?id=com.ilixa.mirror&hl=en_US&gl=US){:target="_blank"}: for distorting, blurring, and generating patterns and gradients
- Powerpoint: cataloguing albums, batch saving, and text box tool

I still use, and highly recommend each of those apps, but as my audience and body of work grew, so did my interest in design, typography, collage, and optical art. I also began to think about developing an artist portfolio and business brand alongside my social media presence. In other words, I needed to build an online store and portfolio, and fter some trial and error, I realized the free apps wouldn’t cut it. Here are a few reasons why:

- **resizing for prints:** in order to get your designs printed, they need to be up to 4800px – none of the apps I mentioned can produce images over 2200px
- **color management:** GIMP gives you more control over color profiles, and allows you to create monotone versions of your designs (as those are cheaper to print) 
- **optimizing photos for web:** In order to start cataloguing my work, I needed a tool to edit, tag, and save my work, preferebly in batches. I would come to discover, thanks to Forensic Files of all things, that The GIMP community created this free plug-in that helps you do just that.

I was introduced to GIMP in this highly questionable [episode of Forensic Files](https://youtu.be/uI9mjJH9cW8?t=384) where an IT specialist with no forensic anthropology training was able to uncover the identity of a skeleton using GIMP. He simply took a photo of the skull, then superimposed, first his own face as a control, then various missing people’s faces until luckily the right one fit. What made me curious was that throughout the episode, he referred to GIMP as the “free photoshop.” At that time this is exactly what I was looking for.

Gnu Image Manipulation Program is an open-source photo editing software used by professional illustrators, designers, photographers, and scientists alike. This is due to GIMP’s sophisticated layering system which allows you to add/blend/transform/erase very specific components inside an image without compromising the surrounding areas or losing your earlier edits. This unlimited editing functionality, coupled with GIMP’s highly customizable library of tools, brushes, gradients, textures, and patterns is why GIMP is the best-known free alternative to Photoshop. 

And thanks to GIMP’s community of contributors (as in the source in "open source",) there are now over 100 GIMP-compatible plug-ins you can download for free. Here are my [first] and [second] favorites. They, along with the software, are in constant maintenance and development, meaning any bugs are swiftly dealt with. 

To conclude my why behind this tutorial: GIMP is a remarkable and magnificent tool that can outperform photoshop in many ways despite being 100% free, for anyone to own, forever.


# Getting Started with GIMP:
 
 Download and install GIMP [here](https://www.gimp.org/downloads/){:target="_blank"}

## Preparing Your Local Folder Tree:

In your local drive, create a “My GIMP” folder. Inside it, create the following folder tree:
- “My XCF Files”: this is where you’ll `Save` multi-layer projects if you want to be able to modify those layers at a later time. `Save` or `Save As`: `filename.xcf` 
- "My GIMP Exports": this is where you can "Export" your creations. You can export a layer or a selection, or as by default, all the visible areas in your canvas as a single image.
  - Note: in GIMP you may need to manually add the file extension. Use `Export As`:
    - `filename.png` for drawings, text, logos, icons, and images with transparent background.
    - `filename.jpeg` when it's important to have a smaller file size/faster loading time
    - `filename.gbr` to make any image or selection into a brush, and
    - `filename.pat` to make any image or selection into a tileable pattern
  - Inside “My GIMP Exports” create a folder named “My GIMP Patterns" - this is where you’ll export your .pat files before you can add them to GIMP’s built-in `patterns` folder.

## Locating GIMP’s built-in “Patterns” folder
1. Open GIMP
2. Go to: `Edit – Preferences – Folders` (+) to expand
3. select the `patterns` folder and copy its location from the address bar above. If there are 2 folders, select the one with "Roaming" in its address. Exit Preferences dialogue without saving.
4. Go to: `File – Open - Search`. Paste the address in the search bar, select the `patterns` folder, then add it to GIMP's shortcuts using the (+) at the bottom left of the Open dialogue.
5. While you’re still in the Open dialogue, navigate to your local “My GIMP” folder tree and add each of the folders you just created to GIMP's shortcuts. 
6. While GIMP's built-in `patterns` folder is still in your clipboard, Open your local File Explorer and paste that location into the address bar. Select, then add the folder to your computer's shortcuts/Quick Access Bar. 

If you're never going to work with GIMP again, this step might have been a waster of time. But if you do end up using GIMP, I just saved you many hours that I myself wasted rummaging through folders. Even if you don't find this tutorial to be helpful, I hope that you'll continue making, saving, and exporting things to fill these folders. **Visit the [Helpful Tools](/articles/2021/03/26/making-with-gimp-part-one/#helpful-tools) section for a list of my favorite GIMP resources.**




# Navigating GIMP

## Finding Things: 
> **Until you are more familiar with GIMP's interface:**
1. hover over the tools/sections one-by-one and a description of each should appear. 
**or**
2. go to: `windows - dockable dialogues` - Select the window you're looking for - if it's already docked, it should flash in place. If not, a new dialogue should apprear.
> 
**If you want your icons to look like the ones below:**
- Go to: `Edit - Preferences - Interface - Icon Theme`
- to switch to color mode: Pick the `Color` theme 
- to increase the size, select: `Custom icon Size` then drag to large. 
- click "OK"


In this tutorial we will utilize the following tools, features, and dialogues in GIMP

## Layers:

<div class="media">
  <div class="media-body">
    <h5 class="mt-0 mb-1">Layers Window</h5>
    in this tutorial you will be working a lot inside the layers dialogue.
    
    - modes:

    - bottom row: 

    - lock/hide:

  </div>
  <img class="ml-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/layers.jpg" alt="GIMP layers window">
</div>

## The Toolbox:

<ul class="list-unstyled">
  <li class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/move.jpg" alt="Move Tool">
    <div class="media-body">
      <h5 class="mt-0 mb-1">Move Tool (m)</h5>
      Select this tool (or press `m` on your keyboard) each time you want to move an object or a selection. 
    </div>
  </li>
  <li class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/ellipse.jpg" alt="Ellipse Select Tool">
    <div class="media-body">
      <h5 class="mt-0 mb-1">Ellipse Select Tool (e)</h5>
      Use it to select (draw) a round region. In Tool Options: check "feather edges" for a softer, more seamless look.
    </div>
  </li>
  <li class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/zoom.jpg" alt="Zoom Tool">
    <div class="media-body">
      <h5 class="mt-0 mb-1">Zoom Tool (+) or (-)</h5>
     I recommend using the keyboard shortcut to zoom in(+) or out (-)
    </div>
  </li>
  <li class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/scale.jpg" alt="Scale Tool">
    <div class="media-body">
      <h5 class="mt-0 mb-1">Scale/Resize Tool (shift+s)</h5>
     Use to Resize an object, layer, or selection. To maintain a fixed aspect ratio, make sure the chain symbols next to the width/hight dialogue are linked.  
    </div>
  </li>
  <li class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/flip.jpg" alt="Flip Tool">
    <div class="media-body">
      <h5 class="mt-0 mb-1">Flip Tool</h5>
     Flip the layer, object, or selection on a vertical or horizontal axis. configure the direction using the Toolbox Options dialogue. 
    </div>
  </li>
  <li class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/bucketfill.jpg" alt="Bucket-Fill Tool">
    <div class="media-body">
      <h5 class="mt-0 mb-1">Bucket-Fill Tool (shift+b)</h5>
     Use to Fill a selection or area with a color or pattern. Configure the fill of your bucket in the Bucket-Fill Tool Options Window (pictured below) 
    </div>
  </li>
</ul>
<div class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/bucketfilltooloptions.jpg" alt="bucket-fill Tool Options">
  <div class="media-body">
    <h5 class="mt-0">Bucket-Fill Tool Options</h5>
    By default this dialogue is docked below the toolbox. Tip: the last thing copied to your clipboard can temporarily be used as a pattern. We will use this feature to test how our patterns look before we export them.
    </div>
  </div>
</div>
<div class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/activecolors.jpg" alt="active colors">
  <div class="media-body">
    <h5 class="mt-0">Active Colors: Foreground and Background</h5>
    Clicking either will open a color dialogue with a color picker included
    </div>
  </div>
</div>


# Making Patterns in GIMP: Method Overview
A pattern is a small image tiled side-by-side to fill a larger canvas. There are many ways to create patterns with GIMP, here are the few i learned over the last year:

tile to canvas ratio:

## Method 1: tiling GIMP’s built-in patterns using the Bucket tool
This is probably the simplest way to create your first pattern. It works great if you are only looking to stack the pattern file side by side a a grid.

1. Create a test canvas
    - Go to: `File – New`
    - Set width and height: 1920*1080
    - Go to `Advanced Options` using the (+)
    - Fill with: White
    - Click ok
2. Choose a pattern from GIMP's pattern menu
  - in your test canvas, Go to: `Windows - Dockable Dialogues - Patterns`
  - If your patterns window is already docked, it should flash, otherwise a window should appear
  - in the pattens window, expand the filter drop down menu
  - select the `plant` tag
  - select the `maple leaves` pattern
  - Find the Fill Bucket tool in your toolbox, it should look like this: 
![Maple Leaf Pattern](/assets/post_media/2021-3-31-gimp-tutorial/methods/leaftile.jpg "Leaf Pattern")

## Method 2: Blending GIMP’s built-in patterns by applying the Pattern Seamless Filter
Use this method to blend rocks, bricks, water, fire, or plant patterns to create a more seamless and realistic texture. it's slower-running and does not work on layers with transparent fill.

1. in test canvas: create new layer. Fill with white
2. in new layer, go to: `Edit - Fill with pattern seamless`
3. select `maple leaf` pattern using the browse menu if it's not already selected
4. click ok. rendering may take up to a minute but this is the result in comparison to Method 1. Not perfect but looks more interesting than merely tiling.

<div class="row">
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/methods/leaftile.jpg/whyihatefacebook_post1.png'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/methods/leafseamless.jpg'>
  </div>
</div>


## Method 3: tiling any image from the web using the Bucket-Fill Tool
Find an image on the web that you want to make into a pattern. For this example, I am using this photo

<figure class="figure">
  <img src="/assets/post_media/2021-3-31-gimp-tutorial/cat.png" class="figure-img img-fluid rounded" alt="diamond cat ">
  <figcaption class="figure-caption">
    from <a href="https://openclipart.org/" target="_blank">from openclipart.org - a free image library and a goldmine for blersed content</a>
  </figcaption>
</figure>

<div class="alert alert-success" role="alert">
(side bar: it would be wise to create another folder for your royalty-free image collection. After you’ve been remixing things for a while, a line blurs in your memory between what’s original/ok to use for profit, and what needs to be credited.)
</div>

1.  Right click the image you want and `Save Image As` to download.

2.  Create a new test canvas if you don’t have one open
  - Open Gimp: `File – New`
  - set size to 1920*1080
  - Expand `Advanced Options` using the (+)
  - Fill with: Foreground color (note: by default this is set to Black, which is what we need for contrast with the example image used in this exercise. to change the color of your background:******)
  - `Ok` to create new image

3.  Create your pattern file
  - set size to 180*180
  - Go to `Advanced Options` using the (+)
  - Fill with: Foreground color
  - `Ok` to create new image

4. drag image from your local file explorer into the layers window. The image will be pasted as a new layer  with the same name as the image file.
  -if the image pasted below the background, click  (or use the arrows at the bottom of the layers window) and shift it to the top
5. scale the image down
  - select the `scale` tool and resize the image holding the `shift` key to lock dimensions until it fits nicely inside the layer boundary.
6. hide the background layer below using the lock "eye" to the left of the layer name. 
7. with the image layer selected, go to: `edit - copy` (or `ctrl`+`c` on your keyboard)
8. Test pattern
  - go to test canvas then create new layer and fill with BG or FG (whichever contrasts better with your design)
  - in new layer: select bucket-fill tool. set Fill Type to "pattern fill - clipboard image"
  - click anywhere in the layer to apply fill. 
you should get something that looks similar to this:
  ![diamond cat pattern](/assets/post_media/2021-3-31-gimp-tutorial/catcompact.jpg "diamond cat pink background")
  
*The next method will teach you how to manipulate the spacing of your tiles.*

## Method 4: Offsetting 

1. Go back to your cat pattern layer
2. duplicate it using the `duplicate current layer` button at the bottom of the layers window
3. in duplicate layer only (which should be on top of the original): 
  - go to: `layer - layer to image size`
  - again, go to: `layer - transform - offset - by width/2, height/2` now you should see the pattern copied in all 4 corners
4. go to: `edit - copy visible` (this should copy both layers into your clipboard and the first space in your patterns dialogue)
5. Test pattern
  - go to test canvas. create new layer and fill with BG or FG (whichever contrasts better with your design)
  - in new layer: select bucket-fill tool. set Fill Type to "pattern fill - clipboard image"
  - click anywhere in the layer to apply fill. 
6. more tweaks: scale/flip tools.. tbc

*****Cindie this is the end of the first draft





in the image layer select the scale tool
click anywhere inside the image and a scaluntil face fills most of the layer boundary:
- select the scale tool






• Using GIMP’s built-in Patterns
o Bucket fill method: Using the bucket-fill tool to simply tile a pattern file
o pattern-seamless method: using bucket tool with a filter to blend pattern tiles into a seamless texture. 
• drawing your own patterns
o select tool method: shapes
o brush method: 
o text
• offseting


Bucket fill method: probably the simplest way to create your first pattern. It works great if you are only looking to stack the pattern design in a grid.
Pattern-seamless method:

Offset method
100x100 – 250x250px

Upload pic
Center
Duplicate layer
In copy layer only:
layer – layer to image size (
layer - transform-offset 2/h 2/w
export into pattern into pattern folder
patten seamless method (for textures)
*doesn’t work with transparent background 
bucket tool-pattern 
edit – fill with pattern seamless
pick pattern
downside: cant do live preview
Dot patterns
Make new file size 1920*1080 – this will be used to text out each pattern
File – new – size 60*60 (white)
Add center guides:
image – guides – new guide by percent – vertical – 50%
image – guides – new guide by percent – horizontal – 50%

method 1
create new transparent layer
draw circle and center it 30*30px
fill with bucket tool
unselect – hide white background

<div class="card">
  <div class="card-header">
      <h4 id="quick-bundler-jekyll-command-reference" style="margin:0px;">Quick Bundler/Jekyll Command Reference</h4>
    </div>
    <div class="card-body">
    <p style="margin-bottom:1rem;" class="card-text">
 {{ commands | markdownify | remove: '<p>' | remove: '</p>' }}
    </p>
    <a href="https://bundler.io/docs.html" target="_blank" class="card-link">Bundler Docs</a>
    <a href="https://jekyllrb.com/docs/usage/" target="_blank" class="card-link">Jekyll Command Line Usage</a>
  </div>
</div>

<div class="card">
  <div class="card-header">
      <h4 id="quick-git-command-reference" style="margin:0px;">Quick Git Command Reference</h4>
    </div>
    <div class="card-body">
    <p style="margin-bottom:1rem;" class="card-text">
    {% capture commands %}`git init` - create a new git repository   
  `git status` - view changes to git repo and staging area   
  `git add filename` where "filename" is the name of a file or folder - stage changes to file to be committed   
  `git commit -m "description of commit"` - commit staged changes   
  `git push origin main` - push local commits to remote Github repo's main branch{% endcapture %}
    {{ commands | markdownify | remove: '<p>' | remove: '</p>' }}
    </p>
    <a href="https://git-scm.com/docs" target="_blank" class="card-link">Git Docs</a>
    <a href="https://git-scm.com/book/en/v2" target="_blank" class="card-link">Git Book</a>
  </div>
</div>

![Blue Myself](\assets\post_media\2021-3-31-gimp-tutorial\intro\bluemyself "GIMP patterns")

<figure class="figure">
  <img src="" class="figure-img img-fluid rounded" alt="collage ">
  <figcaption class="figure-caption">
    Images from <a href="https://www.bequietclaire.com/myvideos/mbti-memes" target="_blank">bequietclaire.com</a>
  </figcaption>
</figure>

<div class="alert alert-success" role="alert">
Ok, lets start making!
</div>


<div class="alert alert-success" role="alert">
Tip: if you want your icons to look like the ones below. Go to: Edit - Preferences - Interface - Icon Theme. Pick the "color" theme then click "OK"
</div>

![brick](\assets\post_media\2021-3-31-gimp-tutorial\intro\ffff.png "GIMP patterns")
![lamp2](\assets\post_media\2021-3-31-gimp-tutorial\intro\roselamp2.png "GIMP patterns")
![pikachloe](\assets\post_media\2021-3-31-gimp-tutorial\intro\pikachloe.jpg "GIMP patterns")
![lamp](\assets\post_media\2021-3-31-gimp-tutorial\intro\lamp.png "GIMP patterns")
![greendots](\assets\post_media\2021-3-31-gimp-tutorial\intro\pattern2.jpg "GIMP patterns")
![Diamond Cats](\assets\post_media\2021-3-31-gimp-tutorial\intro\catoffsets.jpg "GIMP patterns")


4/1 grid
<div class="row">
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/feathers-portrait.jpg/whyihatefacebook_post1.png'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/pikachloe-portrait.jpg'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/trash-portrait.jpg/whyihatefacebook_post3.png'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/f.jpg/whyihatefacebook_post4.png'>
  </div>
</div>

<table class="table table-hover">
  <thead>
    <tr>
      <th scope="col">Action</th>
      <th scope="col">How to do it</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">moving an object</th>
      <td>make sure you're in the layer you want to move, click "m" on your keyboard or find the move tool in the toolbox. click and drag to move your object </td>
    </tr>
    <tr>
      <th scope="row">zooming in and out</th>
      <td>click (+) or (-) on your keyboard</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td colspan="2">![water pattern](/assets/post_media/2021-3-30-gimp-tutorial/water-pattern.jpg"water pattern")</td>
    </tr>
      <th scope="row">finding a tool</th>
      <td>until you get familiar with GIMP's toolbox, mouse over the tools in the toolbox one-by-one until you find the one you need.</td>
    </tr>
  </tbody>
</table>