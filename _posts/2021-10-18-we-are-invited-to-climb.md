---
layout: post
title: "We Are Invited to Climb"
categories: poetry
author: andrew yoon
related-articles:
post_description: Live-generating excerpts from a book of chance poetry
---

<script src="/scripts/bml/bml.bundle.js" type="text/javascript"></script>

![A pocketbook laying on a bed of wires](/assets/post_media/2021-10-18-we-are-invited-to-climb/book-on-wires.jpg "Photo by Phoebe Waldron")

These are a few poems from my recently published book of generative "chance poetry" [_We Are Invited to Climb_](https://awst-press.com/shop/we-are-invited-to-climb){:target="_blank"}. The book is not only written with chance systems but available in a free live-generating edition at [weareinvitedtoclimb.org](//weareinvitedtoclimb.org){:target="_blank"}. In the spirit of virtual goods, these excerpts are embedded here in live-generating versions as well, realized anew every time you load or refresh this page.

The book is written using my pet poetry programming language, [BML](//bml-lang.org){:target="_blank"}, which incorporates carefully composed randomized elements into linear text. On each generation of the book, thousands of poetic elements---words, phrases, line breaks, layout---are chosen by chance. Curious readers may be interested to read [the book's appendix](https://weareinvitedtoclimb.org/#appendix){:target="_blank"}, which delves into the technical construction and artistic motivations behind the project, as well as a brief survey of the generative text scene.

The book and these excerpts are published under a [Creative Commons BY-NC-SA License](https://creativecommons.org/licenses/by-nc-sa/4.0/){:target="_blank"} and the book's source code is available [here](https://gitlab.com/ajyoon/weareinvitedtoclimb.org/){:target="_blank"}.

<div style="text-align: right"><i>—ay</i></div>

<h3 id="we-are-invited-to-climb">we are invited to climb</h3>
<div id="poem-1-target">
  <!-- An arbitrary render is hard-coded for SEO and noscript purposes -->
  <p style="max-width: 36em; margin-left: auto; margin-right: auto; text-align: left; padding-left: 0%; padding-right: 12%;">new and old us met today. we ask what day it is; it doesn’t matter. we ask if we are happy, and it matters. we ask how many rows are crossed off on that list of things we’ll never do, and we learn about a whole new list. the plant in our window is starting to dry out in those longer leaves that droop over the pot, and our phone is filled with names we don’t remember.</p>
  <p style="max-width: 36em; margin-left: auto; margin-right: auto; text-align: left; padding-left: 14%; padding-right: 6%;">these are the side effects of change—the things none of us were looking for—the things which contain the world, and that vast chasm whose walls are so far that we float around between them—a mountain above us—a birdflock below—the gridlines are laughing in a genuine kind of way, and we feel a strange comfort in the scope of it all.</p>
  <p style="max-width: 36em; margin-left: auto; margin-right: auto; text-align: justify; padding-left: 17%; padding-right: 4%;">what does change look like? does it have a smell? the skypoems are wider now, those upsidedown kites whose strings reach down from the clouds—we’ve been looking for one that gives us permission, but mostly we’ve just found nonsense. the kitestrings go taut, then slack, then taut again:</p>
  <p style="max-width: 36em; margin-left: auto; margin-right: auto; text-align: justify; padding-left: 17%; padding-right: 2%;">we are invited to climb.</p>
</div>

<h3 id="beforemaroon">beforemaroon</h3>
<div id="poem-2-target">
  <!-- An arbitrary render is hard-coded for SEO and noscript purposes -->
  <p style="max-width: 36em; margin-left: auto; margin-right: auto; text-align: justify; padding-left: 17%; padding-right: 3%;">wayingsong behind the eyelids, the underthere, a beforemaroon again with questions and ideas—how to see around a color when we’re stuck inside it—how to count from eight to blue with only one hand—everything moving so slowly but the clock seems to be working as usual with those metaled clunks and woodenbits. the hour hand seems different this time around.</p>
</div>

<h3 id="damp-sticks">the smell of damp sticks from outside</h3>
<div id="poem-3-target">
  <!-- An arbitrary render is hard-coded for SEO and noscript purposes -->
  <p style="max-width: 36em; margin-left: auto; margin-right: auto; text-align: justify; padding-left: 0%; padding-right: 6%;">the smell of damp sticks from outside. a littlemoving sound. we notice how everything is so softandgreen, and how the cars driving by sound like leaves.</p>
  <p style="max-width: 36em; margin-left: auto; margin-right: auto; text-align: left; padding-left: 8%; padding-right: 4%;">we ask if it can stay this way for a while.</p>
  <p style="max-width: 36em; margin-left: auto; margin-right: auto; text-align: justify; padding-left: 9%; padding-right: 19%;">it doesn’t, but that’s okay.</p>
</div>

<script>
 let poem1Source = `
new and old us met today. we ask what {(day), (month), (year)} it is; it doesn't matter. we ask if we are happy{(;), (, and)} it matters. we ask how many rows are crossed off on {(our) 70, (the), (that)} list of things we'll never do, and we learn about a whole new list. the plant in our window {(has started to dry out), (has dried out), (is starting to dry out), (is drying out)} in those longer {(leaves), (arms)} that {(grew), (grow), (droop)} over the pot, and {(we've run out of money on our subway card), (our phone is filled with names we don't remember)}.

these are the side effects of change---the things none of us were looking for---the things which contain the world, and that {(gray), (vast), (vast gray)} chasm whose walls are so far {(that), ()} we float around between them---a {(mountain), (valley), (planet), (forest)} above us---a birdflock below---the gridlines are laughing in a genuine kind of way, and we feel a strange {(compassion), (comfort)} in the {(scale), (size), (scope)} of it all.

what does change look like? does it have a smell? the skypoems are {(wider), (broader), (slower)} now, those upsidedown kites whose strings {(reach into), (reach down from)} the clouds---we've been looking for one that {(tells us something), (brings us together), (gives us permission), (answers something)}, but mostly we've just found nonsense. the kitestrings go taut, then slack, then taut again:

we are invited to climb.`;

 let poem2Source = `
eval {
  var _DIGIT_MAP = {
      0: 'zero',
      1: 'one',
      2: 'two',
      3: 'three',
      4: 'four',
      5: 'five',
      6: 'six',
      7: 'seven',
      8: 'eight',
      9: 'nine'
  };
  function digitToWord(digit) {
      if (digit < 0 || digit > 9) {
          throw '' + digit + ' is not a valid single digit';
      }
      return _DIGIT_MAP[digit];
  }

  function randomNumberWord(min, max) {
      return digitToWord(randomInt(min, max));
  }

  function randomNumber1to9() { return randomNumberWord(1, 9); }
}
wayingsong {(behind), (before)} the eyelids, the underthere, a {(before), (behind)}maroon {(again), (againagain), (again again)} with questions and ideas---how to see {(above), (around)} a color when we're stuck {(inside), (outside)} it---how to count from {call randomNumber1to9} to {(blue), (red)} with {(just), (only)} one hand---{(these things all), (everything)} moving so slowly {(but), (while)} the clock seems to be working as usual with those metaled clunks and woodenbits{(---), (. ), (: )}the hour hand seems different this time around.
 `;

 let poem3Source = `
{(the), (a)} smell of damp sticks from outside. a {(slowmoving), (littlemoving), (smallmoving)} sound. we notice how everything is so {(soft), (pink)}andgreen, and how the cars {(driving by), (going by)} sound like {(trees), (leaves)}.

we ask if it can stay {(this way), (like this)}{(, at least), ()} for a while.

{(it does.) 70, (it doesn't, but that's okay.)}
 `;

 function randomInt(min, max) {
   return Math.floor(randomFloat(min, max));
 }

 function randomFloat(min, max) {
   return (Math.random() * (max - min)) + min;
 }

 // assumes there is more than 1 weight
 function weightedChoice(weights) {
   let probSum = 0;
   for (let i = 0; i < weights.length; i++) {
     probSum += weights[i][1];
   }
   let pick = randomFloat(0, probSum);
   let currentPos = 0;
   for (let i = 0; i < weights.length; i++) {
     currentPos += weights[i][1];
     if (currentPos >= pick) {
       return weights[i][0];
     }
   }
   console.error("failed to calculate weightedChoice value, using fallback");
   return weights[0][0];
 }

 function randomFormatDiv(div) {
   for (let i = 0; i < div.children.length; i++) {
     let alignment = weightedChoice([['left', 10], ['justify', 6], ['right', 3]]);
     let marginLeftPct = randomInt(0, 20);
     let marginRightPct = randomInt(0, 20);
     div.children[i].style = `max-width: 36em; ` +
                             `margin-left: auto; ` +
                             `margin-right: auto; ` +
                             `text-align: ${alignment}; ` +
                             `padding-left: ${marginLeftPct}%; ` +
                             `padding-right: ${marginRightPct}%`;
   }
 }

 function renderToDiv(src, targetId) {
   let innerHTML = bml(
     src, {}, {renderMarkdown: true, markdownSettings: {smartypants: true}});
   let target = document.getElementById(targetId);
   target.innerHTML = innerHTML;
   // gotta make sure this doesn't run before the html update finishes
   randomFormatDiv(target);
 }

 renderToDiv(poem1Source, 'poem-1-target');
 renderToDiv(poem2Source, 'poem-2-target');
 renderToDiv(poem3Source, 'poem-3-target');

 if (location.hash) {
   // Since the page layout has changed since initial load,
   // we need to reset the location hash to snap the window
   // to bring the id into view
   location.hash = location.hash;
   // But even this doesn't work on some browsers (Chrome...)
   // so, set a backup on a few increasingly long delays.
   // This way, fast browsers will scroll to the element faster
   // but slow browsers will stil catch up.
   // (This can cause a noticeable snap-back if a user scrolls
   // immediately after loading the page, but I think this is
   // the best I can do)
   let scroll = function() {
     document.getElementById(location.hash.substring(1))
             .scrollIntoView({behavior: 'auto'});
   }
   setTimeout(scroll, 50);
   setTimeout(scroll, 200);
   setTimeout(scroll, 500);
 }
</script>
