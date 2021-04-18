---

layout: post

title: "Making With GIMP: Patterns and Textures"
categories: [tutorial, tech]
author: saqmemes
related-articles:
post_description: [a step-by step guide into making patterns and textures using GIMP]

---

![feathers](\assets\post_media\2021-3-31-gimp-tutorial\intro\feathersheader.jpg "feathers")

## TABLE OF CONTENTS
1. [What You Will Learn](/articles/2021/04/16/making-with-gimp-part-one/#in-this-tutorial)
2. [Why GIMP?](/articles/2021/04/16/making-with-gimp-part-one/#why-gimp)
3. [Getting Started](/articles/2021/04/16/making-with-gimp-part-one/#getting-started)
4. [Navigating GIMP](/articles/2021/04/16/making-with-gimp-part-one/#navigating-gimp)
  - [The Toolbox](/articles/2021/04/16/making-with-gimp-part-one/#the-tool-box)
  - [Colors](/articles/2021/04/16/making-with-gimp-part-one/#colors)
  - [Layers](/articles/2021/04/16/making-with-gimp-part-one/#layers)
  - [How-To Summary](/articles/2021/04/16/making-with-gimp-part-one/#how-to-summary)
5. [Creating Patterns](/articles/2021/04/16/making-with-gimp-part-one/#making-patterns-in-gimp)
  - [Tile to Canvas Ratio](/articles/2021/04/16/making-with-gimp-part-one/#tile-to-canvas-ratio)
  - [Testing Your Patterns](/articles/2021/04/16/making-with-gimp-part-one/#testing-your-patterns-via-the-clipboard)
  - [Layer Boundaries](/articles/2021/04/16/making-with-gimp-part-one/#layer-boundaries)
  - [Saving Your Creations](/articles/2021/04/16/making-with-gimp-part-one/#savingexporting-your-creations)
  - [Method 1](/articles/2021/04/16/making-with-gimp-part-one/#method-1-tiling-gimps-built-in-patterns-using-the-bucket-tool)
  - [Method 2](/articles/2021/04/16/making-with-gimp-part-one/#method-2-blending-gimps-built-in-patterns-by-applying-the-pattern-seamless-filter)
  - [Method 3](/articles/2021/04/16/making-with-gimp-part-one/#method-3-drawing-your-own-pattern-using-the-select-tools)
  - [Method 4](/articles/2021/04/16/making-with-gimp-part-one/#method-4-tiling-any-image-from-the-web-using-the-bucket-fill-tool)
  - [Method 5](/articles/2021/04/16/making-with-gimp-part-one/#method-5-tiling-a-specific-part-of-an-image-using-the-select-tool)
  - [Offsetting](/articles/2021/04/16/making-with-gimp-part-one/#offsetting)
  - [Adding a Border & Bevel](/articles/2021/04/16/making-with-gimp-part-one/#adding-a-border--bevel)
6. [Helpful Resources](/articles/2021/04/16/making-with-gimp-part-one/#helpful-resources)


## IN THIS TUTORIAL:
I will tell you about the different types of patterns I learned to make using GIMP, and show you step-by-step, how to make each design into your own creation. This is a complete beginner’s guide, as I, too, am a beginner. I hope this tutorial will help you become more familiar with GIMP's interface and toolboxes. By the end, you should at least be able to create something similar to each of the following designs:

<div class="row">
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/feathers-portrait.jpg'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/pikachloe-portrait-geen.jpg'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/trash-portrait.jpg'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/intro/square-portrait-4.jpg'>
  </div>
</div>





## WHY GIMP?
I got by as a content creator making most of my content in my phone, using a combination of the following mobile photo editors:

- [Phonto](https://phon.to/download){:target="_blank"}: for text editing
- [PicsArt](https://picsart.com/){:target="_blank"}: for their stickers and filters, also for cropping/blending/enhancing images
- [Background eraser](https://play.google.com/store/apps/details?id=com.handycloset.android.eraser&hl=en_US&gl=US){:target="_blank"}: for its auto erase tool
- [IbisPaint X](https://ibispaint.com/?lang=en-US){:target="_blank"}: for brushes and other drawing tools
- [Cut+Mix Studio](https://play.google.com/store/apps/details?id=pictriev.cutout&hl=en_US&gl=US){:target="_blank"}: for layering/affining/face swapping
- [Mirrorlab](https://play.google.com/store/apps/details?id=com.ilixa.mirror&hl=en_US&gl=US){:target="_blank"}: for distorting, blurring, and generating patterns and gradients
- Powerpoint: cataloguing albums, batch saving, and text box tool

I still use, and highly recommend each of those apps, but as my audience and body of work grew, so did my interest in design, typography, collage, and optical art. I also began to think about developing an artist portfolio and business brand alongside my social media presence. In other words, I needed to build an online store and portfolio, and fter some trial and error, I realized the free apps wouldn’t cut it. Here are a few reasons why:

- **Resizing for prints:** in order to get your designs printed, they need to be up to 4800px – none of the apps I mentioned can produce images over 2200px
- **Color management:** GIMP gives you more control over color profiles, and allows you to create monotone versions of your designs (as those are cheaper to print) 
- **optimizing photos for web:** In order to start cataloguing my work, I needed a tool to edit, tag, and save my work, preferebly in batches. I would come to discover, thanks to Forensic Files of all things, that The GIMP community created this free plug-in that helps you do just that.

Yes, I was introduced to GIMP in this highly questionable yet entertaining [episode of Forensic Files](https://youtu.be/uI9mjJH9cW8?t=384) where a well-meaning IT specialist with no forensic anthropology training was able to uncover the identity of a skeleton using GIMP. He simply took a photo of the skull, then superimposed, first his own face as a control, then various missing people’s faces until luckily the right one fit. What made me curious was that throughout the episode, he referred to GIMP as the “free photoshop.” At that time this is exactly what I was looking for.

**Gnu Image Manipulation Program** is an open-source photo editing software used by professional illustrators, designers, photographers, and scientists alike. This is due to GIMP’s sophisticated layering system which allows you to add/blend/transform/erase very specific components inside an image without compromising the surrounding areas or losing your earlier edits. This unlimited editing functionality, coupled with GIMP’s highly customizable library of tools, brushes, gradients, textures, and patterns is why GIMP is the best-known free alternative to Photoshop. 

And thanks to GIMP’s community of contributors (as the source in "open source") there are now over 100 GIMP-compatible plug-ins you can download for free. They, along with the software, are in constant maintenance and development, meaning any bugs are swiftly dealt with. 

To conclude my *why* behind this tutorial: GIMP is a remarkable and magnificent tool that can outperform photoshop in many ways despite being 100% free, for anyone to own, forever.


## GETTING STARTED
[mise en place](https://en.wikipedia.org/wiki/Mise_en_place){:target="_blank"}
 
### Installing GIMP

 Download and install GIMP [here](https://www.gimp.org/downloads/){:target="_blank"}

### Installing Resynthesizer
Resynthesizer is a very useful plug-in that we will use for [Method 2](/articles/2021/04/16/making-with-gimp-part-one/#method-2-blending-gimps-built-in-patterns-by-applying-the-pattern-seamless-filter) in this tutorial. Download and install it [here](https://github.com/pixlsus/registry.gimp.org_static/blob/master/registry.gimp.org/files/Resynthesizer_v1.0-i686.zip){:target="_blank"}


### Preparing Your Local Folder Tree:

In your local drive, create a “My GIMP” folder. Inside it, create the following folder tree:
- “**My XCF Files**”: this is where you’ll `Save` multi-layer projects if you want to be able to modify those layers at a later time.
  - `Save` or `Save As`: `filename.xcf` 
- "**My GIMP Exports**": this is where you can "Export" your creations. You can export a layer or a selection, or as by default, all the visible areas in your canvas as a single image.
  - Note: in GIMP you may need to manually add the file extension. Use `Export As`:
    - `filename.png` for drawings, text, logos, icons, and images with transparent background.
    - `filename.jpeg` when it's important to have a smaller file size/faster loading time.
    - `filename.gbr` to make any image or selection into a brush.
    - `filename.pat` to make any image or selection into a tileable pattern.
  - Inside “My GIMP Exports” create a folder named “**My GIMP Patterns**" - this is where you’ll export your .pat files temporarily before you can add them to GIMP’s built-in `patterns` folder.

### Locating GIMP’s Built-in “Patterns” Folder
1. Open GIMP
2. Go to: `Edit – Preferences – Folders` (+) to expand
3. select the `patterns` folder and copy its location from the address bar above. If there are 2 folders, select the one with "Roaming" in its address. Exit Preferences dialogue without saving.
4. Go to: `File – Open - Search`. Paste the address in the search bar, select the `patterns` folder, then add it to GIMP's shortcuts using the (+) at the bottom left of the Open dialogue.
5. While you’re still in the Open dialogue, navigate to your local “My GIMP” folder tree and add each of the folders you just created (especially "My GIMP Patterns") to GIMP's shortcuts. 
6. While GIMP's built-in `patterns` folder is still in your clipboard, Open your local File Explorer and paste that location into the address bar. Select, then add the folder to your computer's shortcuts/Quick Access Bar. 

If you're never going to work with GIMP again, this step might have been a waster of time. But if you do end up using GIMP, I just saved you many hours that I myself wasted rummaging through folders. Even if you don't find this tutorial to be helpful, I hope that you'll continue making, saving, and exporting things to fill these folders.


<div class="alert alert-success" role="alert">
Visit the <a href="/articles/2021/04/16/making-with-gimp-part-one/#helpful-tools">Helpful Tools</a> section for a list of my favorite GIMP resources.
</div>



## NAVIGATING GIMP

### General Tips

**clicking anywhere on the canvas/layer activates whatever tool is selected**
For example: if the text tool is selected, clicking on any preexisting text boxes enables you to edit the text. Clicking anywhere else on the canvas opens a new text box.

**Until you are more familiar with GIMP's interface, this is how you can find the various tools, windows, and settings you want to configure:**
- Hover over the tools/sections one-by-one. The name and description of each should appear. 
**or**
- Go to: `Windows - Dockable Dialogues` - Select the window you're looking for - if it's already docked and visible, it should flash in place. If not, a new dialogue should apprear.

**To ungroup/show all the tools we will use in this tutorial**
1. Go to: `Edit - Preferences - Interface - Toolbox`
2. Deselect the box that reads "Use Tool Groups"


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

By default this dialogue is docked below the toolbox, and looks different based on the tool selected.
<div class="row">
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/icons/tooloptions-bucketfill.png'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/icons/tooloptions-ellipse.png'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/icons/tooloptions-crop.png'>
  </div>
</div>

### Colors
<div class="media">
    <img class="mr-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/activecolors.jpg" alt="active colors">
  <div class="media-body">
    <h5 class="mt-0">Active Colors: Foreground and Background</h5>
    Clicking either will open a floating color dialogue
  </div>
</div>


<div class="media">
  <div class="media-body">
    <h5 class="mt-0 mb-1">Floating Color Dialogue</h5>
    To change the color of your foreground or background, click the one you want to change and this window should pop up. To configure the color: 
<ul>
  <li>Type in the color's HTML notation</li>
  <li>Use a palette</li>
  <li>use the Color Picker next to the HTML textbox if the color you want is present on your canvas</li>
</ul>  
</div>
  <img class="ml-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/colordialogue.png" alt="Active colors">
</div>

### Layers
oversimply-put, layers are like those transparent projector sheets your middle school teachers used to display compound diagrams, formulas, and concepts. By the end of this tutorial, you will become very familiar with most of the componenets in the Layers Dialogue pictured below:

<div class="media">
  <div class="media-body">
    <h5 class="mt-0 mb-1">Layers Dialogue</h5>
    You will be working a lot inside the layers window, which is one of GIMP's Dockable Dialogues.
<ul>
  <li>Layer modes: for this tutorial, keep it set to "normal"</li>
  <li>To hide/unhide a layer: Click the eye to the left of the layer icon</li>
  <li>The Bottom row, from left to right:</li>
<ol>
<li>add a new layer</li>
<li>add a new layer group</li>
<li>move current layer up</li>
<li>move current layer down</li>
<li>duplicate current layer</li>
<li>anchor floating layer</li>
<li>add layer mask</li>
<li>delete layer</li>
</ol>
</ul>  
</div>
  <img class="ml-3" src="/assets/post_media/2021-3-31-gimp-tutorial/icons/layers.png" alt="GIMP layers window">
</div>


## HOW-TO SUMMARY

<table class="table table-hover">
  <thead>
    <tr>
      <th scope="col">Action</th>
      <th scope="col">How to do it</th>
    </tr>
  </thead>
  <tbody>
    <tr class="table-light">
      <th scope="row">To move something inside a layer</th>
      <td> Make sure you're in the correct layer and that the object is visible. Find the Move tool in the toolbox. click and drag to move your object. </td>
    </tr>
    <tr class="table-light">
      <th scope="row">To delete something inside a layer</th>
      <td> Make sure it's selected and visible then hit the `Delete` key on your keyboard </td>
    </tr>
    <tr class="table-light">
      <th scope="row">To copy something inside a layer</th>
      <td> Make sure you're in the correct layer and that the object is selected. Go to: `Edit - Copy` or `ctrl + c` </td>
    </tr>
    <tr class="table-light">
      <th scope="row">To copy an entire layer:</th>
      <td>Select the layer and ake sure it's visible, copy or `ctrl + c` by default, only the top visible layer will be copied.</td>
    </tr>
    <tr class="table-light">
      <th scope="row">To copy all the visible things inside all the visible layers</th>
      <td>Go to: `Edit - Copy Visible` </td>
    </tr>
    <tr class="table-light">
      <th scope="row">To paste what's in your clipboard</th>
      <td> make sure you're in the layer you want to paste in, then "ctrl+v" or go to "Edit-Paste" </td>
    </tr>
    <tr class="table-light">
      <th scope="row">To zoom in and out</th>
      <td>click (+) or (-) on your keyboard</td>
    </tr>
    <tr class="table-light">
      <th scope="row">To unselect everything:</th>
      <td colspan="2">Go to: `Select - None` or `Shift + ctrl + A` Do this then reselect if you're ever unsure if you selected the right thing</td>
    </tr>
    <tr class="table-light">
      <th scope="row">To change the active colors</th>
      <td>To change the color of your foreground or background, click the one you want to change and a color dialogue should pop up. Type in the color's html notation, use one of GIMP's palettes, or use the Color Picker tool</td>
    </tr>
    <tr class="table-light">
      <th scope="row">To find the name and function of a tool or feature</th>
      <td>mouse over the icons/options one by one. The name and a short description should appear</td>
    </tr>
    <tr class="table-light">
      <th scope="row">To quickly rename a layer</th>
      <td>double click the layer name, type it in, then click enter</td>
    </tr>
  </tbody>
</table>


## MAKING PATTERNS IN GIMP
A pattern is a small image tiled side-by-side to fill a larger canvas. before we get into each method, here are some important concepts you should be aware of:

#### Tile to canvas ratio:
while creating patterns, you will need to create at least 2 files, a small one for the pattern tile (50x50p - 250x250p) and a larger one to be used as a test canvas (1080x1080p - 3600x3600p)

For this tutorial we will use the following ratios:
- Pattern (tile) files: 60x60 px and 180x180px
- Test canvas: 1920x1080 px. you can also create a square or portrait test canvas if you'd like


#### Testing your patterns via the clipboard
"The Clipboard" is a where your computer *temporarily* stores the last selection you copied using the "Copy" command found in most programs, GIMP included. In GIMP however, there's a cool feature in the pattern Dialogue, where the first pattern block is always reserved for whatever is stored in the clipboard at the time. This will prove useful for testing patterns before you commit to exporting/saving them.

#### Layer Boundaries
Sometimes you will need to fit the layer into the image or vice-versa. Follow this graphic to know which adjustment to make

![Boundaries](\assets\post_media\2021-3-31-gimp-tutorial\icons\layer-image-boundaries.jpg "GIMP layers")

#### Saving/Exporting your creations
There are 3 different methods to save your pattern creations. 
1. To add the pattern you created to GIMP's patterns dialogue
- Go to: `File - Export As`
- Name it `filename.pat`
- Save file in your local [My GIMP Patterns](/articles/2021/04/16/making-with-gimp-part-one/#preparing-your-local-folder-tree) folder, which you should have added to GIMP's shortcuts [earlier in this tutorial](/articles/2021/04/16/making-with-gimp-part-one/#locating-gimps-built-in-patterns-folder).
- Open your local "My GIMP Patterns" Folder and either drag or copy the pattern you just saved into GIMP's built-in `patterns` folder which should also be added to your quick access bar or local short cuts
- In GIMP: refresh your pattern dialogue using the refresh button in the bottom right of the window and you should see your pattern. 
- If you want to 

2. To export your test canvas as a flat image file
- In your test canvas: move the layer you want to save to the top
- Go to: `File - Export As`
- Name it:`filename.jpg` or `filename.png` 
- Save it in your local "My GIMP Exports" folder

3. If you don't think you'll want to modify the individual layers of your pattern at a later time, you can exit without saving. If you want to keep working on the pattern later:
- Go to: `File - Save`
- Name it: `filename.xcf`
- Save it in your local "My XCF Files" folder as `filename-pattern.xcf`


**With that said, there are so many ways to create patterns and textures using GIMP. Here are the few methods I learned over the last year:**

### METHOD 1: tiling GIMP’s built-in patterns using the Bucket tool
This is probably the simplest way to create your first pattern. It works great if you are only looking to stack a preexisting GIMP pattern side by side in a grid.

1. Create at least one test canvas:
you will keep coming back to this document to test all the methods
    - Go to: `File – New`
    - Set width and height: 1920*1080
    - Go to `Advanced Options` using the (+)
    - Fill with: transparency
    - Click ok
2. Choose a pattern from GIMP's pattern menu
  - in your test canvas, Go to: `Windows - Dockable Dialogues - Patterns`
  - If your patterns window is already docked, it should flash in place, otherwise a window should appear
  - in the pattens window, expand the filter drop down menu
  - select the `plant` tag
  - select the `maple leaves` pattern
  - Select the Bucket-Fill tool in your toolbox, set Fill Type to "pattern"
  - Click anywhere inside the layer to apply your pattern. The result should look like this:

![Maple Leaf Pattern](/assets/post_media/2021-3-31-gimp-tutorial/methods/leaftile.jpg "Leaf Pattern")

[Export and/or save this pattern](/articles/2021/04/16/making-with-gimp-part-one/#savingexporting-your-creations)


## METHOD 2: Blending GIMP’s built-in patterns by applying the Pattern Seamless Filter
This filter comes with the [Resynthesizer](/articles/2021/04/16/making-with-gimp-part-one/#installing-resynthesizer) plug-in. Use this method to blend rocks, bricks, water, fire, or plant patterns to create a more seamless and realistic texture. it's slower-running and does not work on layers with transparent fill. 

1. in test canvas: create new layer. Fill with: white
2. in new layer, go to: `Edit - Fill with pattern seamless`
3. select `maple leaf` pattern using the browse menu if it's not already selected
4. click ok. rendering may take up to a minute but this is the result in comparison to Method 1. Not perfect but looks more interesting than merely tiling.

<div class="row">
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/methods/leaftile.jpg'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/methods/leafseamless.jpg'>
  </div>
</div>

[Export and/or save this pattern](/articles/2021/04/16/making-with-gimp-part-one/#savingexporting-your-creations)

you can try this method with other GIMP patterns or use it to blend your own creations into a seamless texture.

## METHOD 3: Drawing your own pattern using the select tools
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
5. if you want your pattern to look exactly like the one pictured above, you may skip this step:
  - In the "Tool Options" dialogue, I left "feathered edges" unchecked for this look. Check it if you want your dot to have softer edges.

6. Configure the size to 30px using the `Tool Options` dialogue found under the toolbox.
7. Click anywhere inside the circle to move it, then drag it towards the center. The mid point of your selection should easily "snap" to the center of the layer.
8. Click `Enter` depending on zoom level, you should either see a really tiny or a really blurry black dot in the middle of the layer. that's ok, it won't be blurry when tiled!
9. Hide white background layer
10. with only the top layer visible, go to `Edit - Copy` or `ctrl+c`to temporarily store your dot as a GIMP pattern
11. In the test canvas, create a new layer, set Fill to "white"
12. Apply pattern to your canvas
  - Select Fill-Bucket tool
  - in the Tool Options dialgoue, make sure fill type is set to "pattern" and that the pattern source is set to "clipboard"
  - click anywhere inside the layer to tile your dots
13. To manipulate the spacing, angle, and size of your tiles, go to: [Offsetting](/articles/2021/04/16/making-with-gimp-part-one/#offsetting)

[How to export and/or save this pattern](/articles/2021/04/16/making-with-gimp-part-one/#savingexporting-your-patterns)

## METHOD 4: tiling any image from the web using the Bucket-Fill Tool
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
  ![diamond cat pattern](/assets/post_media/2021-3-31-gimp-tutorial/methods/catcompact.jpg "diamond cat pink background")
9. To manipulate the spacing, angle, and size of your tiles, go to: [Offsetting](/articles/2021/04/16/making-with-gimp-part-one/#offsetting)

[How to export and/or save this pattern](/articles/2021/04/16/making-with-gimp-part-one/#savingexporting-your-creations)

## METHOD 5: Tiling a specific part of an image using the Select Tool
for this example we're going to tile the face of Pikachloe in the image below:
you should get something that looks similar to this:
  ![pikachloe](/assets/post_media/2021-3-31-gimp-tutorial/methods/pikachloefull.png "pikachloe")

1.  Create your pattern file
  - set size to 180*180
  - Go to `Advanced Options` using the (+)
  - Fill with: Transparency
  - `Ok` to create new image
2. Save and drag image from your local file explorer into the layers window. The image will be pasted as a new layer with the same name as the image file.
  -if the image pasted below the background, click it (or use the arrows at the bottom of the layers window) and drag it to the top.
3. Scale the image down
  - Select the `scale` tool and resize the image holding the `shift` key to lock dimensions until it fits nicely inside the layer boundary.
4. Cut out the part of the image you want to tile
  - select the "Ellipse Select" tool
  - in "Tool Options" check "Feathered Edges" and set the radius to about 40%
  - draw a circle around the face, then click enter
  - Go to: `Edit - Copy` or `ctrl+c`
  - Go to: `Edit - Paste` or `ctrl+v` - A floating layer should appear at the top of your layers dialogue, click "Add New Layer" to anchor it as a full layer. 
  - Hide uncut image layer
5. Test your pattern
  - make sure only the ellipse selection layer is visible and is on top.
  - go to: `Edit - Copy`
  - go to test canvas
  - create a new layer
  - select bucket-fill tool, make sure fill type is set to `pattern` and that pattern is set to `clipboard`
  -click anywehre on the screen to apply fill. This is the result you will get:

![pikachloe](/assets/post_media/2021-3-31-gimp-tutorial/methods/pikachloe1.jpg "pikachloe")

*To get your tiles to look like the ones below, go to [Offsetting](/articles/2021/04/16/making-with-gimp-part-one/#offsetting) to configure the spacing, angle, and size of your tiles.*

<div class="row">
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/methods/pikachloeflipped.jpg'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/methods/pikachloecentered.jpg'>
  </div>
  <div class="col-sm">
    <img class="img-fluid" src='/assets/post_media/2021-3-31-gimp-tutorial/methods/pikachloeoffset.jpg'>
  </div>
</div>

[Export and/or save this pattern](/articles/2021/04/16/making-with-gimp-part-one/#savingexporting-your-creations)



## OFFSETTING


<div class="alert alert-danger" role="alert">
  This method can only be used in addition to methods 3-5
</div>

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
6. More tweaks you can try after you duplicate the original pattern layer (step 2)
  - use the `scale` tool to change the size of either the duplicate or original pattern layer (or both)
  - use the `flip` tool to vertically or horizontally flip the original or duplicate pattern layer (or both)
  - use the `rotate` tool to change the angle of either the original or duplicate layer. For example, changing a square into a diamond.

## ADDING A BORDER & BEVEL
To add a border to any image:
1. Go to `Filters - Decor - Add Border`
2. Configure the color and thickness (I have my X and Y set to 12 and delta level set to 25)
3. To add a bevel to your border, go to: `Filters - Decor - Add Bevel`
4. Make sure `work on copy` and `keep bump layer` are both checked
5. Play around with the thickness (I had my bevel thickness set to 5)
6. Click OK

## HELPFUL RESOURCES
- Download GIMP:
  - [Here](https://www.gimp.org/downloads/){:target="_blank"}
- Helpful Plug-ins:
  - [Resynthesizer](https://github.com/pixlsus/registry.gimp.org_static/blob/master/registry.gimp.org/files/Resynthesizer_v1.0-i686.zip){:target="_blank"}
  - [BIMP-Batch Image Manipulation Program for batch editing](https://alessandrofrancesconi.it/projects/bimp/){:target="_blank"}
- Useful Brushes:
  - [Arrows](https://www.gimphelp.org/arrow_brushes_color_1.html){:target="_blank"}
  - [Cards](https://www.deviantart.com/chrisdesign/art/GIMP-Playingcard-Brush-196530703){:target="_blank"}
- Video Tutorials:
  - [How to put someone's face on an object](https://www.youtube.com/watch?v=bVbYXsBxpiY&list=PLadY4zckiOFGka6i6em6XYRanbtPFuVSN&index=1){:target="_blank"}
  - [Photo enhancement techniques](https://www.youtube.com/watch?v=TiavEWDVQGE&list=PLadY4zckiOFGka6i6em6XYRanbtPFuVSN&index=7){:target="_blank"}
  - [Intro to layers](https://www.youtube.com/watch?v=pCyBF0NwIDU){:target="_blank"}
  - [All layer modes explained](https://www.youtube.com/watch?v=17Iivi0tmug&list=PLadY4zckiOFGka6i6em6XYRanbtPFuVSN&index=21){:target="_blank"}
  - [Creating T-shirt mock-ups](https://www.youtube.com/watch?v=qEs6Ml64twE&list=PLadY4zckiOFGka6i6em6XYRanbtPFuVSN&index=25){:target="_blank"}
  - [Creating seamless patterns from a drawing](https://www.youtube.com/watch?v=Lt3U7dtT8g0&list=PLadY4zckiOFGka6i6em6XYRanbtPFuVSN&index=32){:target="_blank"}
  - [Top 10 Filters in GIMP](https://www.youtube.com/watch?v=Pbb2q65AxL0&list=PLadY4zckiOFGka6i6em6XYRanbtPFuVSN&index=36){:target="_blank"}
  - [Clone tool explained](https://www.youtube.com/watch?v=5p7mqkQ7YzM&list=PLadY4zckiOFGka6i6em6XYRanbtPFuVSN&index=39){:target="_blank"}
  - [Clone, Healing, and Perspective tools](https://www.youtube.com/watch?v=qS_S87JkUN0&list=PLadY4zckiOFGka6i6em6XYRanbtPFuVSN&index=46){:target="_blank"}
  - [Creating 3D text](https://www.youtube.com/watch?v=j-uOl6dJ5CM&list=PLadY4zckiOFGka6i6em6XYRanbtPFuVSN&index=48){:target="_blank"}
  - [Steal the color grading from any image](https://www.youtube.com/watch?v=8oZ5xOegS-s&list=PLadY4zckiOFGka6i6em6XYRanbtPFuVSN&index=47){:target="_blank"}
  - [Creatinng a dot pattern with GIMP](https://www.youtube.com/watch?v=6TTLVlR7KHA&list=PLadY4zckiOFGka6i6em6XYRanbtPFuVSN&index=95){:target="_blank"}
- Royalty-Free Images:
  - [Openclipart.org](openclipart.org){:target="_blank"}
  - [Pexels](https://www.pexels.com/royalty-free-images/){:target="_blank"}
  - [EveryPixel](https://www.everypixel.com/){:target="_blank"}