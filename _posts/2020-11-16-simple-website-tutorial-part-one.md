---
layout: post
title:  "Making A Simple Static Website: Part One, Why Code Your Own Website?"
categories: [tutorial, tech]
author: ada.wrong
excerpt_separator: <!--more-->
related-articles: [2020-11-23-simple-website-tutorial-part-two, 2021-1-21-simple-website-tutorial-part-three]
---

This is the first part of a multi-part series on creating your own static website for complete beginners. First, we will discuss *why* you may want to code your own website.<!--more--> Then, I will go over how to set up your development environment and how to use github pages to host your site. Finally, I will suggest resources for learning how to build a site from scratch and how to use templates of websites that are compatible with github pages. Everything used in this tutorial is free! All you need is a computer (Mac, Windows, or Linux) and an internet connection to get started.

For those of you that are already familiar with programming or web technologies, this is the breakdown of the technologies/frameworks I'm going over step by step in this tutorial series:
- bash
- git
- github and github pages
- jekyll (optional)  

If that list meant nothing to you, that is completely okay! You will be using all of these if you follow the steps in this tutorial series. We are also going to be using more stuff such as HTML and CSS but I won't cover step by step. Instead I will teach you how to learn what you need from free resources on the internet. That said, this tutorial assumes you know nothing other than how to type, use a web browser, and search engine.

### So why code your own website? ###   
My inspiration for writing this tutorial was this text that I originally wrote in January 2020 which is transcribed below.

<div class="row">
	<div class="col-sm">
		<img class="img-fluid" src='/images/post_images/2020-11-16-simple-website-tutorial-part-one.md/whyihatefacebook_post1.png'>
	</div>
	<div class="col-sm">
		<img class="img-fluid" src='/images/post_images/2020-11-16-simple-website-tutorial-part-one.md/whyihatefacebook_post2.png'>
	</div>
	<div class="col-sm">
		<img class="img-fluid" src='/images/post_images/2020-11-16-simple-website-tutorial-part-one.md/whyihatefacebook_post3.png'>
	</div>
	<div class="col-sm">
		<img class="img-fluid" src='/images/post_images/2020-11-16-simple-website-tutorial-part-one.md/whyihatefacebook_post4.png'>
	</div>
</div>


>reasons why i hate facebook  
>some notes adapted for dissemination on their platform instagram  
>1. they disregard their own content creators  
>- there is no way for content creators to monetize the traffic they bring to the site. the only reason why instagram has users is because of their content creators but their is no monetary benefit for users (only paid in "exposure").  
>- reveals facebook's view of their users. they are obvious about their unequal view of themselves (as a company) vs. their users. they think we are fools and are proud of their ability to exploit us. this is a feedback loop -- creating an increasingly unequal relationship through their policy decisions.  
>2. their community guidelines do not reflect the ideals we would have for our ideal society/space.  
>- it does not account for the uneven playing field of society or the past. all negative speech or criticism is "hate speech" regardless of the power dynamics of the people involved. this is how the site is moderated. any community created on the platform will not be able to transcend these guidelines.  
>- "A post calling someone 'my favorite n-----' is allowed to stay up, because under the policy it is considered 'explicitly positive content.'
>'Autistic people should be sterilized' seems offensive to him, but it stays up as well. Autism is not a 'protected characteristic' the way race and gender are, and so it doesn’t violate the policy. ('Men should be sterilized' would be taken down.)", from an excerpt from ["The Trauma Floor" by Casey Newton on theverge.com](https://www.theverge.com/2019/2/25/18229714/cognizant-facebook-content-moderator-interviews-trauma-working-conditions-arizona){:target="_blank"}, which i suggest you read if you would like to see why you may have frustrating experiences with ig moderation.  
>- no matter how many posts you make about how "reverse racism" is not real, "reverse racism" is real on facebook's platforms.  
>3. they rely on their user's supposed ignorace of technology while also eroding society's opportunities to learn and understand internet tech.  
>- another feedback loop: users are "too stupid" to learn basic web technologies so they "need" facebook to do it for them, simultaneously giving up their data and their rights (on the site). but as facebook takes up more of the internet, users are basically giving up their rights on the entire internet.  
>- people used to learn to code to create their own sites in order to express themselves on the internet. now we are addicted to the ease and hyperconnectivity that large centralized social media platforms afford us. but it comes at a price.  
>- tech literacy is pertinent knowledge and site building skills are power. facebook tries to obscure this from us.  
>- so what do we do from here?

This text was a reflection on my experience creating content for instagram in the name of "self expression". At first, I used instagram because I wanted to create content that the platform wasn't intended for and post them on it. Why not post weird memes on a site meant for selfies and travel photography? I thought it was subversive. But after some years, I realized, why was I spending so much time on a platform that simply does not want me on there? Currently, I obviously don't have a solution for large tech companies' restrictive and racist/sexist/abelist moderation policies or their takeover of the internet. This tutorial series utilizes github pages for free hosting and github is owned by Microsoft and hosted on Amazon Web Services. However, I hope it will help people develop the basic web development skills needed to even consider becoming independent from larger platforms.

Even if you don't care about any of this, coding your own static website to host your portfolio or resume is cheaper than paying for a website builder service. Also, it's not as hard as people make it seem like it is! Although I studied computer science in college, I didn't learn frontend web development formally in a class. I needed a portfolio website so I just made one with the basic knowledge I had. Whatever I didn't know, I Googled and tried it until it worked. My first iterations were rough and did not meet modern web standards. However, with each new site I made, I learned a new framework commonly used in web development today and tried to implement it for my needs. Although everyone learns differently, for web development, I really suggest "learning by doing" and motivating yourself by working on a project you need to actually use.

Thanks for reading this far! The next part will focus on setting up your development environment with git and github. In the meantime, you can checkout the [github repository](https://github.com/virtualgoodsdealer/virtualgoodsdealer.github.io){:target="_blank"} for this website and see a possible 'end product' of this tutorial series. [Continue to part two to get started.]({% post_url 2020-11-23-simple-website-tutorial-part-two %})
