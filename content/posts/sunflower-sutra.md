---
date: 2020-08-13T16:00:09Z
title: Playing with Other Content Management Systems
author: Darren Beattie
hero_image: "/content/images/adrien-olichon--aOsCcTJXWY-unsplash.jpg"

---
I admit I've become a bit of a [Ghost](https://ghost.org/ "Ghost") fanboy. I even applied to an engineering support position recently, though I'm sad to say I did not get through to the final round.

However, that doesn't mean Ghost is without its flaws. $29 per install for managed

After discovering that running multiple instances of Ghost on a small $5 DigitalOcean Droplet creates an updating challenge (in my last post) I started looking for alternatives.

## The Search

My search has taken me a lot of places and I am contemplating constructing a CMS breakdown post with my pros/cons list for everything I've tried. This is the interim post.

The most obvious con for me is the price, which eliminates an enormous number of CMS options from the fold. Many are outrageously priced for an individual and clearly catered to enterprise situations.

Those with affordable (or free) tiers tend to be over-the-top, basically, a visual graphical interface for an entire back-end ([Contentful](https://www.contentful.com/ "Contentful")/[DatoCMS](https://www.datocms.com/ "DatoCMS") etc...). A lot more than I need.

You can always go with the classics:

* WordPress
* Drupal

But I'm trying to get away from slow monolithic do-it-all solutions of the past that have poor writing experiences.

Unfortunately, you can no longer set up custom domains on Medium or I'd just leave it all there.

It's also tempting just to set up a static JAMstack site hosted on Vercel, Netlify or GitHub Pages and link it out to Medium for writing. But then all the SEO for any of my personal musings would end up on Medium and not [darrenbeattie.com](https:/darrenbeattie.com "(darrenbeattie.com)"). The whole point of owning and using this domain is to drive awareness.

I'm generally looking for alternatives that will help me with some elements of web development as a by-product of their use.

The open-source ones (like Ghost or [Strapi](https://strapi.io/ "Strapi")) are great for this because I can go into the source code and play around. They can also both be used with Next.js or Gatsby.js in the JAMstack as static sites. My jam at the moment because they are both React-based.

The problem is both require a server-based set-up to expose a backend API to the front-end. I don't really want to spend $50-80 USD a year to host static content that receives very little traffic.

I really just want to write periodically and have a place to statically share information on me and the projects I've done or are working on. Something that can be hosted on Vercel, Netlify or GitHub Pages would be ideal.

## Enter Git-based CMS's

I found two unique options:

1. [NetlifyCMS](https://www.netlifycms.org/ "NetlifyCMS")
2. [Forestry](https://forestry.io/ "Forestry")

Both tie directly into a [GitHub](https://github.com/ "GitHub") (or [GitLab](https://about.gitlab.com/ "GitLab")/[Bitbucket](https://bitbucket.org/product "Bitbucket")) repo for your JAMstack project (I'm using Gatsby here) and pull data directly from your folder structure.

Meaning they really embrace the JAMstack approach, whereby nearly everything and anything you do can be done directly from your git-flow.

You can edit markdown directly from the editor of your choice, push to a branch, merge to master and your changes are merged and automatically redeployed to almost your [static host of choice](https://forestry.io/docs/hosting/ "static host of choice").

NetlifyCMS also provides a yourwebsite.com/admin access point for you to edit your content without using markdown. 

Now I don't mind working with markdown and find myself being more and more comfortable with it the longer I'm a developer. It's an integral part of web software development.

However, it is not a nice writing experience. Mostly because you typically can't see how it will look while you write it.  

NetlifyCMS is open source and actually not tied directly to Netlify. You can deploy other places but my plan all along was to deploy to Netlify, so that's what I ended up trying first.

I admit I didn't really go down the configuration and tooling rabbit hole you may need to host elsewhere. Netlify offers a generous free hosting tier that I'll probably never exceed with this site. I've used them before and I didn't see any point in going down the path of messing around with other more complicated setups.

Forestry, on the other hand, is a web-based portal. It's free for up to 3 sites, with 3 contributors per site. In other words, perfect for a personal blog. Admittedly, they aren't really hosting much, just providing an interface for you to interact with your own Git Repo. 

It is not (near as I can tell) open-source but the developers behind the tool do contribute to open-source. And they are a Canadian company, which I always like to support when I can. Based out of PEI (_of all places..._), which is not exactly a "Tech Hub."

They have built an open-source tool called [TinaCMS](https://tinacms.org/). It's on my list of things to try soon, but it's not production-ready.

I ultimately decided on Forestry. It's a better writing experience, a better design and most importantly it was WAY easier to set up than NetlifyCMS. It took me almost an entire day to debug and launch a Gatsby starter with it, but only a couple of hours to do the same with Forestry.

The documentation is also extensive and very well written. Not that the NetlifyCMS documentation is bad, it's quite good for open-source, it just didn't make it as easy. You have to mess around with gatsby config files a lot to get it going.

The problem with open source tools is that you're completely on your own and most of the people working on them are volunteers. The development process tends to be slower overall. The best ones have a solid revenue stream (usually a cloud/hosting option) to fully support their development.