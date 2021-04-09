---

layout: post

title: "Making With GIMP: Patterns and Textures"
categories: [tutorial]
author: saqmemes
related-articles:
post_description: [How drawing certain boundaries between you and your higher self may reveal your true potential. Plus the one thing you should know before next voyage]

---



## Table of Content
1. [What You Will Learn To Make](/articles/2021/03/26/making-with-gimp-part-one/#in-this-tutorial)
2. [Why GIMP?](articles/2021/03/26/making-with-gimp-part-one/#why-gimp)
3. [Getting Started](articles/2021/03/26/making-with-gimp-part-one/#why-gimp)
4. [Navigating GIMP](articles/2021/03/26/making-with-gimp-part-one/#navigating-gimp)
  - [The Toolbox](/articles/2021/03/26/making-with-gimp-part-one/#the-tool-box)
  - [Colors]
  - [Dockable vs. Floating Dialogues]
  - [Layers]
  - [How-To Summary](/articles/2021/03/26/making-with-gimp-part-one/#how-to-summary)
5. [Patterns: An Overview]
  - [Method 1]
  - [Method 2]


## In This Tutorial:
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





## Why GIMP?
I got by as a content creator by making most of my content in my phone, using a combination of the following mobile photo editors:

- [Phonto](https://phon.to/download){:target="_blank"}: for text editing
- [PicsArt](https://picsart.com/){:target="_blank"}: for cropping/blending/enhancing images
- [Background eraser](https://play.google.com/store/apps/details?id=com.handycloset.android.eraser&hl=en_US&gl=US){:target="_blank"}: for its auto erase tool
- [IbisPaint X](https://ibispaint.com/?lang=en-US){:target="_blank"}: for brushes and other drawing tools
- [Cut+Mix Studio](https://play.google.com/store/apps/details?id=pictriev.cutout&hl=en_US&gl=US){:target="_blank"}: for layering/affining/face swapping
- [Mirrorlab](https://play.google.com/store/apps/details?id=com.ilixa.mirror&hl=en_US&gl=US){:target="_blank"}: for distorting, blurring, and generating patterns and gradients
- Powerpoint: cataloguing albums, batch saving, and text box tool

I still use, and highly recommend each of those apps, but as my audience and body of work grew, so did my interest in design, typography, collage, and optical art. I also began to think about developing an artist portfolio and business brand alongside my social media presence. In other words, I needed to build an online store and portfolio, and fter some trial and error, I realized the free apps wouldn’t cut it. Here are a few reasons why:

- **Resizing for prints:** in order to get your designs printed, they need to be up to 4800px – none of the apps I mentioned can produce images over 2200px
- **Color management:** GIMP gives you more control over color profiles, and allows you to create monotone versions of your designs (as those are cheaper to print) 
- **optimizing photos for web:** In order to start cataloguing my work, I needed a tool to edit, tag, and save my work, preferebly in batches. I would come to discover, thanks to Forensic Files of all things, that The GIMP community created this free plug-in that helps you do just that.

I was introduced to GIMP in this highly questionable [episode of Forensic Files](https://youtu.be/uI9mjJH9cW8?t=384) where an IT specialist with no forensic anthropology training was able to uncover the identity of a skeleton using GIMP. He simply took a photo of the skull, then superimposed, first his own face as a control, then various missing people’s faces until luckily the right one fit. What made me curious was that throughout the episode, he referred to GIMP as the “free photoshop.” At that time this is exactly what I was looking for.

**Gnu Image Manipulation Program** is an open-source photo editing software used by professional illustrators, designers, photographers, and scientists alike. This is due to GIMP’s sophisticated layering system which allows you to add/blend/transform/erase very specific components inside an image without compromising the surrounding areas or losing your earlier edits. This unlimited editing functionality, coupled with GIMP’s highly customizable library of tools, brushes, gradients, textures, and patterns is why GIMP is the best-known free alternative to Photoshop. 

And thanks to GIMP’s community of contributors (as the source in "open source") there are now over 100 GIMP-compatible plug-ins you can download for free. Here are my [first] and [second] favorites. They, along with the software, are in constant maintenance and development, meaning any bugs are swiftly dealt with. 

To conclude my *why* behind this tutorial: GIMP is a remarkable and magnificent tool that can outperform photoshop in many ways despite being 100% free, for anyone to own forever.


## Getting Started
 
### Installing GIMP

 Download and install GIMP [here](https://www.gimp.org/downloads/){:target="_blank"}

### Preparing Your Local Folder Tree:

In your local drive, create a “My GIMP” folder. Inside it, create the following folder tree:
- “My XCF Files”: this is where you’ll `Save` multi-layer projects if you want to be able to modify those layers at a later time.
  - `Save` or `Save As`: `filename.xcf` 
- "My GIMP Exports": this is where you can "Export" your creations. You can export a layer or a selection, or as by default, all the visible areas in your canvas as a single image.
  - Note: in GIMP you may need to manually add the file extension. Use `Export As`:
    - `filename.png` for drawings, text, logos, icons, and images with transparent background.
    - `filename.jpeg` when it's important to have a smaller file size/faster loading time
    - `filename.gbr` to make any image or selection into a brush, and
    - `filename.pat` to make any image or selection into a tileable pattern
  - Inside “My GIMP Exports” create a folder named “My GIMP Patterns" - this is where you’ll export your .pat files temporarily before you can add them to GIMP’s built-in `patterns` folder.

### Locating GIMP’s Built-in “Patterns” Folder
1. Open GIMP
2. Go to: `Edit – Preferences – Folders` (+) to expand
3. select the `patterns` folder and copy its location from the address bar above. If there are 2 folders, select the one with "Roaming" in its address. Exit Preferences dialogue without saving.
4. Go to: `File – Open - Search`. Paste the address in the search bar, select the `patterns` folder, then add it to GIMP's shortcuts using the (+) at the bottom left of the Open dialogue.
5. While you’re still in the Open dialogue, navigate to your local “My GIMP” folder tree and add each of the folders you just created to GIMP's shortcuts. 
6. While GIMP's built-in `patterns` folder is still in your clipboard, Open your local File Explorer and paste that location into the address bar. Select, then add the folder to your computer's shortcuts/Quick Access Bar. 

If you're never going to work with GIMP again, this step might have been a waster of time. But if you do end up using GIMP, I just saved you many hours that I myself wasted rummaging through folders. Even if you don't find this tutorial to be helpful, I hope that you'll continue making, saving, and exporting things to fill these folders.


<div class="alert alert-success" role="alert">
Visit the <a href="/articles/2021/03/26/making-with-gimp-part-one/#helpful-tools">Helpful Tools</a> section for a list of my favorite GIMP resources.
</div>



## Navigating GIMP

### General Tips

**clicking anywhere on the canvas/layer activates whatever tool is selected**
For example: if the text tool is selected, clicking on any preexisting text boxes enables you to edit the text. Clicking anywhere else on the canvas opens a new text box.

**Until you are more familiar with GIMP's interface, this is how you can find the various tools, windows, and settings you want to configure:**
- Hover over the tools/sections one-by-one. The name and description of each should appear. 
**or**
- Go to: `Windows - Dockable Dialogues` - Select the window you're looking for - if it's already docked and visible, it should flash in place. If not, a new dialogue should apprear.

**If you want your icons to look like the ones below:**
1. Go to: `Edit - Preferences - Interface - Icon Theme`
2. To switch to color mode: Pick the `Color` theme 
3. To increase the size of the icons, select: `Custom Icon Size` then drag to large.
4. click "OK"


More specifically, in this tutorial we will utilize the following tools, features, and dialogues/windows in GIMP


### The Toolbox:
What happens when you click on your canvas is determined by what is selected inside the toolbox. For example
  - With the Move tool selected: if you click and drag anywhere in your canvas, you will move the whatever occupies the top visible layer.
  - With the Scale tool selected: if you clcik and drag anywehre in your canvas, you will select whatever occupies the top visible layer and scale it, opening the Scale floating dialogue.

With that in mind, here's every tool we will use in this turorial:

<ul class="list-unstyled">
  <li class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/move.jpg" alt="Move Tool">
    <div class="media-body">
      <h5 class="mt-0 mb-1">Move Tool (m)</h5>
      Select this tool (or press `m` on your keyboard) almost every time you want to move an object or a selection. 
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
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/rotate.jpg" alt="Move Tool">
    <div class="media-body">
      <h5 class="mt-0 mb-1">Rotate Tool (shift+r)</h5>
      Use this tool to rotate a selection. Configure the increment and angle of rotation using the Tool Options Window
    </div>
  </li>
  <li class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/align.jpg" alt="Ellipse Select Tool">
    <div class="media-body">
      <h5 class="mt-0 mb-1">Alignment Tool</h5>
      Allign/arrange selections and images horizontally or vertically in respect of eachother or the layer the occupy
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

### Tool Options
<div class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/bucketfilltooloptions.jpg" alt="bucket-fill Tool Options">
  <div class="media-body">
    <h5 class="mt-0">Bucket-Fill Tool Options</h5>
    By default this dialogue is docked below the toolbox. Tip: the last thing copied to your clipboard can temporarily be used as a pattern. We will use this feature to test how our patterns look before we export them.
  </div>
</div>

### Colors
<div class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/activecolors.jpg" alt="active colors">
  <div class="media-body">
    <h5 class="mt-0">Active Colors: Foreground and Background</h5>
    Clicking either will open a color dialogue with a color picker included
  </div>
</div>

### Layers
oversimply-put, layers are like those transparent projector sheets your middle school teachers used to display compound diagrams, formulas, and concepts. By the end of this tutorial, you will become very familiar with the Layers Dialogue pictured below:

<div class="media">
  <div class="media-body">
    <h5 class="mt-0 mb-1">Layers Dialogue</h5>
    in this tutorial you will be working a lot inside the layers window, which is one of GIMP's Dockable Dialogues.
  </div>
  <img class="ml-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/layers.png" alt="GIMP layers window">
</div>

### Layer Boundaries
![Boundaries](\assets\post_media\2021-3-31-gimp-tutorial\icons\layer-image-boundaries.jpg "GIMP layers")


## How-to Summary

<table class="table table-hover">
  <thead>
    <tr>
      <th scope="col">Action</th>
      <th scope="col">How to do it</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">To move something inside a layer</th>
      <td> Make sure you're in the correct layer and that the object is visible. Find the Move tool in the toolbox. click and drag to move your object. </td>
    </tr>
    <tr>
      <th scope="row">To delete something inside a layer</th>
      <td> Make sure it's selected and visible then hit the `Delete` key on your keyboard </td>
    </tr>
    <tr>
      <th scope="row">To copy something inside a layer</th>
      <td> Make sure you're in the correct layer and that the object is selected. Go to: `Edit - Copy` or `ctrl + c` </td>
    </tr>
    <tr>
      <th scope="row">To copy an entire layer:</th>
      <td>Select the layer and ake sure it's visible, copy or `ctrl + c` by default, only the top visible layer will be copied.</td>
    </tr>
    <tr>
      <th scope="row">To copy all the visible things inside all the visible layers</th>
      <td>Go to: `Edit - Copy Visible` </td>
    </tr>
    <tr>
      <th scope="row">To paste what's in your clipboard</th>
      <td> .... </td>
    </tr>
    <tr>
      <th scope="row">To zoom in and out</th>
      <td>click (+) or (-) on your keyboard</td>
    </tr>
    <tr>
      <th scope="row">To unselect everything:</th>
      <td colspan="2">Go to: `Select - None` or `Shift + ctrl + A` Do this then reselect if you're ever not sure if you selected the right thing</td>
    </tr>
    <tr>
      <th scope="row">To change the active colors</th>
      <td>To change the color of your foreground or background, click the one you want to change and a color dialogue should pop up. type in the color's html code or use the Color Picker tool</td>
    </tr>
    <tr>
      <th scope="row">To find the name and function of a tool or feature</th>
      <td>mouse over the icons/options one by one. The name and a short description should appear</td>
    </tr>
    <tr>
      <th scope="row">To quickly rename a layer</th>
      <td>double click the layer name, type it in, then click enter</td>
    </tr>
  </tbody>
</table>


## Making Patterns in GIMP: Method Overview
A pattern is a small image tiled side-by-side to fill a larger canvas. before we get into each method, here are some important concepts you should be aware of:

#### Tile to canvas ratio:
while creating patterns, you will need to create at least 2 files, a small one for the pattern tile (50px - 250px) and a larger one to be used as a test canvas (1080px - 3600px)

#### Testing your patterns via the clipboard
"The Clipboard" is a where your computer *temporarily* stores the last selection you copied with the "Copy" command found in most programs, GIMP included. In GIMP however, there's a cool feature in the pattern Dialogue, where the first pattern block is always reserved for whatever is stored in the clipboard at the time. This will prove useful for testing patterns before you commit to exporting/saving them.


#### Saving/Exporting your patterns
there are 3 different methods to save your pattern creations. 
1. to add the pattern you created to GIMP's patterns window
  - Go to: `File - Export As`
  - remember the 


With that said, there are many ways to create patterns with GIMP. Here are the few methods I learned over the last year: 

### Method 1: tiling GIMP’s built-in patterns using the Bucket tool
This is probably the simplest way to create your first pattern. It works great if you are only looking to stack a preexisting GIMP pattern side by side in a rigid grid.

1. Create at least one test canvas:
you will keep coming back to this document to test all the methods
    - Go to: `File – New`
    - Set width and height: 1920*1080
    - Go to `Advanced Options` using the (+)
    - Fill with: transparency White
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
Side bar: If you want to get into collaging and tiling long-term, it would be wise to create another folder for your royalty-free image collection. After you’ve been remixing things for a while, a line blurs in your memory between what’s original/ok to use for profit, and what needs to be credited.
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
  
*To manipulate the spacing, angle, and size of your tiles, go to:* [Method 7: Offsetting](/articles/2021/03/26/making-with-gimp-part-one/#method-7-offsetting)


## Method 4: Tiling a specific part of an image using the Select Tool
for this example we're going to tile the face of Pikachloe in the image below



## Method 5: Drawing your own pattern using the select tools
for this tutorial we're going to use the ellipse tool to make this dot pattern:

![Dots](\assets\post_media\2021-3-31-gimp-tutorial\intro\dotpattern1.jpg "GIMP patterns")

1. Create new pattern file
  - Go to: `File – New`
  - Set size 60*60 px
  - Go to: `Advanced Options`
  - Set fill color to "White"
2. Add and snap to center guides:
  - Vertical guide: `Image – guides – new guide by percent – vertical – 50%`
  - Horizontal guide:`image – guides – new guide by percent – horizontal – 50%` 
  - Go to: `View` and check `Snap to Guides`
3. Create new transparent layer above the white background (Foreground should be Black by default)
4. Draw a 30X30p circle using the Ellipse Tool
  - with the Ellipse tool selected, click and drag down anywhere in the layer to draw. Don't hit enter yet. *at this point you may need to zoom in and out using + or - on your keyboard*
  
  *if you want your pattern to look exactly like the one pictured above, you may skip this step: In the "Tool Options" dialogue, I left "feathered edges" unchecked for this look. Check it if you want your dot to have softer edges.*

  - Configure the size to 30px using the `Tool Options` dialogue found under the toolbox.
  - Click anywhere inside the circle to move it, then drag it towards the center. The mid point of your selection should easily "snap" to the center of the layer.
  - Click `Enter` depending on zoom level, you should either see a really tiny or a really blurry black dot in the middle of the layer. that's ok, it won't be blurry when tiled!
5. Hide white background layer
6. with only the top layer visible, go to `Edit - Copy` or `ctrl+c`to temporarily store your dot as a GIMP pattern
7. In the test canvas, create a new layer, set Fill to "white"
8. Apply pattern to your canvas
  - Select Fill-Bucket tool
  - in the Tool Options dialgoue, make sure fill type is set to "pattern" and that the pattern source is set to "clipboard"
  - click anywhere inside the layer to tile your dots

[How to export and/or save this pattern](/articles/2021/03/26/making-with-gimp-part-one/#savingexporting-your-patterns)


## Method 6: Drawing your own pattern using a brush


## Method 7: Offsetting

This method can only be used in addition to methods 3-6

1. Go back to your pattern layer
2. Duplicate it using the `duplicate current layer` button at the bottom of the layers window
3. in duplicate layer only (which should be on top of the original): 
  - go to: `layer - layer to image size`
  - again in duplicate layer, go to: `layer - transform - offset - by width/2, height/2` now you should see the same pattern copied in all 4 corners
4. Copy both layers to your clipboard:
  - go to: `edit - copy visible` (this should copy both layers into your clipboard and temporarily occupy the the first block in your patterns dialogue)
5. Test your new pattern
  - go to your test canvas.
  - create new layer and fill it with BG or FG (whichever contrasts better with your design)
  - in new layer: select bucket-fill tool. set Fill Type to "pattern fill - clipboard image"
  - click anywhere in the layer to apply fill. 
6. more tweaks: scale/flip tools.. tbc







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

<!DOCTYPE html>
<html>
<head>
<style>
.city {
  background-color: tomato;
  color: white;
  border: 2px solid black;
  margin: 20px;
  padding: 20px;
}
</style>
</head>
<body>

<div class="city">
<h2>London</h2>
<p>London is the capital of England.</p>
</div> 

<div class="city">
<h2>Paris</h2>
<p>Paris is the capital of France.</p>
</div>

<div class="city">
<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan.</p>
</div>

</body>
</html>

- [Preparing Your local Folder Tree](/articles/2021/03/26/making-with-gimp-part-one/#preparing-your-local-folder-tree)
  - [Locating GIMP's Patterns Folder](/articles/2021/03/26/making-with-gimp-part-one/#locating-gimps-built-in-patterns-folder)