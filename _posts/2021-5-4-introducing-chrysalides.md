---

layout: post
title: "Introducing: Chrysalides"
categories: [art]
author: Eric Hu
related-articles:
post_description: ["Motivation and thoughts behind the creator's new series of digital artwork."]
---

<script>
  document.addEventListener("DOMContentLoaded", function() {
  var lazyImages = [].slice.call(document.querySelectorAll("img.lazy"));

  if ("IntersectionObserver" in window) {
    let lazyImageObserver = new IntersectionObserver(function(entries, observer) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          let lazyImage = entry.target;
          lazyImage.src = lazyImage.dataset.src;
          lazyImage.classList.remove("lazy");
          lazyImageObserver.unobserve(lazyImage);
          fetch('https://ipfs.io/ipfs/Qmdp2T77ut3fP5pZ14UrJvXwKGVMoqchF6g8Wn5aMDubsn/metadata.json')
            .then(response => response.json())
            .then(data => {
              document.getElementById("one").innerHTML = data.name;
            });
              fetch('https://ipfs.io/ipfs/QmQMUEGRd8PHgsU8UwmGMnPBPBomwhj7dJCGmnnzdG3fnT/metadata.json')
            .then(response => response.json())
            .then(data => {
              document.getElementById("two").innerHTML = data.name;
            });
            fetch('https://ipfs.io/ipfs/QmcJ3G5VnYS4auySrHvTHEfc7xhYaPsGedqYAg62yK28Jk/metadata.json')
            .then(response => response.json())
            .then(data => {
              document.getElementById("three").innerHTML = data.name;
            });
              fetch('https://ipfs.io/ipfs/QmV68nSEg5KzcFE8E55gzXodYq7ZMrMFy6eSZabpn54KQM/metadata.json')
            .then(response => response.json())
            .then(data => {
              document.getElementById("four").innerHTML = data.name;
            });
        }
      });
    });

    lazyImages.forEach(function(lazyImage) {
      lazyImageObserver.observe(lazyImage);
    });
  } else {
    // Possibly fall back to event handlers here
  }
});
</script>

<style>
    figure {
      margin-bottom: 0px!important;
    }
    .img-full {
      max-width: 60%!important;
    }

    .lazy {
      width: 100%;
    }
</style>

I'd love to give a brain dump of some of my motivations and thinking behind this series of NFTs I recently created.

<div class="row">
  <div class="col- col-sm-6">
    <figure class="figure">
      <image class="lazy" src="data:image/gif;base64,R0lGODlhAQABAIAAAAUEBAAAACwAAAAAAQABAAACAkQBADs=" data-src="https://ipfs.io/ipfs/QmdTYAp64EJPfKUmNUEwwyL9u9hpTsx6zmR24SNkPHhTxL/nft.png" />
      <figcaption class="figure-caption" id="one"></figcaption>
    </figure>
  </div>
  <div class="col- col-sm-6">
    <figure class="figure">
      <image class="lazy" src="data:image/gif;base64,R0lGODlhAQABAIAAAAUEBAAAACwAAAAAAQABAAACAkQBADs=" data-src="https://ipfs.io/ipfs/QmeYre1gcRHniBJiiTxUxbLfCs5BbFKW36BawamF6446Zo/nft.png" />
      <figcaption class="figure-caption" id="two"></figcaption>
    </figure>
  </div>
</div>

<div class="row">
  <div class="col- col-sm-6">
    <figure class="figure">
      <image class="lazy" src="data:image/gif;base64,R0lGODlhAQABAIAAAAUEBAAAACwAAAAAAQABAAACAkQBADs=" data-src="https://ipfs.io/ipfs/QmUNED5ZvCZYoNcztcaf1hdLdasRfXVXVVS1aZuKPxk1xy/nft.png" />
      <figcaption class="figure-caption" id="three"></figcaption>
    </figure>
  </div>
  <div class="col- col-sm-6">
    <figure class="figure">
      <image class="lazy" src="data:image/gif;base64,R0lGODlhAQABAIAAAAUEBAAAACwAAAAAAQABAAACAkQBADs=" data-src="https://ipfs.io/ipfs/QmNPTC7VXxS39TVQsMHnJAGE51FuzPnFSf7qyobndJXzCs/nft.png" />
      <figcaption class="figure-caption" id="four"></figcaption>
    </figure>
  </div>
</div>
<br />
I've been interested in the idea of drawing with light and what that means. Light as both a particle and wave, something that is formless. It's something I thought about when I got asked by Nosaj Thing to do the cover art for his single "For the Light." How do I give light a feeling of having mass?
<br />
<image class="img-full mb-3" src="/assets/post_media/2021-5-4-introducing-chrysalides/thread1.jfif" />
I was into the idea that when creating density with light, even when represented visually, it contains no mass. As volumetric as you can paint light it rarely feels solid.
<br />
<image class="img-full mb-3" src="/assets/post_media/2021-5-4-introducing-chrysalides/thread2.jfif" />
Working with Nosaj, there were a lot of different ideas and drafts I was exploring on how to represent light. I had been thinking of Saul Bass's rejected drafts for the movie poster for The Shining, how menacing yet wispy it was. (Note Kubrick's harsh notes in ink.)
<br />
<br />
![](/assets/post_media/2021-5-4-introducing-chrysalides/thread3.png)
<br />
I was so seduced by its ability to take up so much density yet feel like nothing it all that it led me on some wild goose chases in trying to see if it was something I could replicate in other ways. None of these versions worked for the song.
<br />
<div class="row mb-3 mt-4">
  <div class="col- col-sm-6 mb-3">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread4.jfif" />
  </div>
  <div class="col- col-sm-6 mb-3">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread5.jfif" />
  </div>
</div>
I was happy with the ultimate result of where that ended up, but I also loved a lot of the drafts that were rejected. In fact No. 2 from this NFT series actually started out as a draft of the single art. I felt like I was getting close but it too was also deemed not appropriate.
<br />
<image class="img-full mb-3" src="/assets/post_media/2021-5-4-introducing-chrysalides/thread6.jfif" />
But I liked where it was going. The density felt so different to other things that I've done with similar compositions and similar amounts of elements. More was going on visually, the imagery was more complex but it felt like it took up less space.
<br />
<div class="row mb-3 mt-4">
  <div class="col- col-sm-6 mb-3">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread7.jfif" />
  </div>
  <div class="col- col-sm-6 mb-3">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread8.jfif" />
  </div>
</div>
There's always been this long back and forth dialogue in my work between minimalism and maximalism. There's moments where I want something to be as quiet as possible with nothing extraneous.
<br />
<br />
![](/assets/post_media/2021-5-4-introducing-chrysalides/thread9.png)
<br />
<p class="lead text-center mb-0">
  And then there's other times where frankly, I just want to lay shit on like a mf.
</p>
<br />
<image class="img-full" src="/assets/post_media/2021-5-4-introducing-chrysalides/thread10.jfif" />
<br />
And the parts of me that are attracted to lightness, quietness, and the parts of me that are attracted the density are two different facets of my personality. My Virgo Moon and Leo Rising signs. My design sensibility tell me to eliminate, and who I am as a person says don't.
<br />
<div class="row mb-3 mt-4">
  <div class="col- col-sm-6 mb-3">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread11.jfif" />
  </div>
  <div class="col- col-sm-6 mb-3">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread12.jfif" />
  </div>
</div>
Sometimes I end up in extremes but mostly I strive for a balance of both heaviness and lightness with composition and scale. I lay things out in a way that cover the canvas as much as possible but with only extra large and extra small elements. No in-betweens. It creates tension because of the contrast in sizes between two elements but the elements themselves are limited in count.
<br />
<div class="row mb-3 mt-4">
  <div class="col- col-sm-6 mb-3 align-self-center">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread13.jfif" />
  </div>
  <div class="col- col-sm-6 mb-3 align-self-center">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread14.png" />
  </div>
</div>
I make both image-heavy and type-heavy work, but it's all one thing: composition. The arrangement of objects. If I had to say what's unique about my work—it's the way I arrange things. A lot of that love came from being obsessed with Japanese fish tank layouts when I was younger.
<br />
<br />
![](/assets/post_media/2021-5-4-introducing-chrysalides/thread15.png)
<br />
There genre of fish tank design I loved most: Iwagumi. It's a Zen Buddhist framework of arranging rocks in a tank. One large rock (the Buddha), and smaller rocks orbiting it. The arrangement creates movement, the rocks feel suddenly weightless.
<br />
<br />
![](/assets/post_media/2021-5-4-introducing-chrysalides/thread16.png)
<br />
<p class="lead text-center">
  It shows up in my work in many ways.
</p>
<br />
![](/assets/post_media/2021-5-4-introducing-chrysalides/thread17.jfif)
<br />
The fish I loved observing most in these tanks weren't the fish themselves. It was the shrimps. The bottom feeders. The insects. They rarely moved around a lot, but it was the way they, and the plants they surrounded themselves reflected the extreme, artificially harsh fish tank light. Under that unforgiving fluorescent I witnessed magical moments.
<br />
<br />
<div class="row">
  <div class="col- col-sm-6 mb-3 align-self-center">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread18.jfif" />
  </div>
  <div class="col- col-sm-6 mb-3 align-self-center">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread19.jfif" />
  </div>
</div>
<br />
Shrimp, like other insects represent this primal assault on the visual senses. Even the harmless ones seen as threatening because of how they look, and often not much else. You also don't have to paint an insect realistically either. Their silhouettes are universally known.
<br />
<br />
![](/assets/post_media/2021-5-4-introducing-chrysalides/thread20.png)
<br />
In that sense it was a good subject matter to investigate some of these visual strategies I was working through. You can change an insect's color, and reduce and take away the fidelity of the image, yet they're recognizable. It would take a lot light or shadow to drown them out.
<br />
<image class="img-full mb-3" src="/assets/post_media/2021-5-4-introducing-chrysalides/thread21.jfif" />
<br />
And with animals in nature, bright colors more often signify danger.
<br />
<br />
<div class="row">
  <div class="col- col-sm-6 mb-3 align-self-center">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread22.png" />
  </div>
  <div class="col- col-sm-6 mb-3 align-self-center">
    <image src="/assets/post_media/2021-5-4-introducing-chrysalides/thread23.png" />
  </div>
</div>
<br />
The combination of all these elements and loose thoughts swirling resulted in this limited series, where I deal with how much space both physically and metaphorically some thing takes up? How confrontational can you be while feeling like nothing at all? It's a question that's confronted me as a life many times for various reasons: what does it mean to take up space? When are you too much?

This is something I intend to probably answer in as many ways as I can throughout the rest of my career out of both necessity and curiosity. For now, I'm choosing to look at the bright side of things (sorry.)

---
This article was adapted from a [Twitter thread](https://twitter.com/_EricHu/status/1385344481516560389){:target="_blank"}. The first four works of Chrysalides were listed on [Foundation](https://foundation.app/eric){:target="_blank"} on 23 April 2021.