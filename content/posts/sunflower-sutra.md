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

NetlifyCMS is open source and actually not tied directly to Netlify. It's what I ended up trying first.

I admit I didn't really go down the configuration and tooling rabbit hole though as Netlify does offer a generous free hosting tier that I'll probably never exceed with this site.

I'm using Netlify here but you c

## [**Setting up LFS in your git repo**](https://forestry.io/blog/versioning-large-files-with-git-lfs/#setting-up-lfs-in-your-git-repo)

Git LFS is easy to set up and works transparently on your repository. Once you configure Git LFS in your repo, you can continue to commit and push large files as you would normally.

1. Download and install the Git LFS extension [**from the Git LFS website**](https://git-lfs.github.com/).
2. Navigate to your repository and run `git lfs install`.
3. Run `git lfs track` followed by the file pattern you want. To track all PNG files for example, run `git lfs track "*.png"`
4. Commit the `.gitattributes` file as well as any existing files that are now tracked in LFS, and push the changes to your remote

That’s it! You’re now using Git LFS to handle your large binary files.

![](/content/images/elcarito-CRn-_80z4SE-unsplash.jpg)

The only water on the river mirrored the red sky, sun sank on top of final Frisco peaks, no fish in that stream, no hermit in those mounts, just ourselves rheumy-eyed and hung-over like old bums on the riverbank, tired and wily.

Look at the Sunflower, he said, there was a dead gray shadow against the sky, big as a man, sitting dry on top of a pile of ancient sawdust–

\--I rushed up enchanted–it was my first sunflower, memories of Blake–my visions–Harlem

# “the gray Sunflower poised against the sunset, crackly bleak and dusty with the smut and smog and smoke of olden locomotives in its eye”

and Hells of the Eastern rivers, bridges clanking Joes greasy Sandwiches, dead baby carriages, black treadless tires forgotten and unretreaded, the poem of the riverbank, condoms & pots, steel knives, nothing stainless, only the dank muck and the razor-sharp artifacts passing into the past–

and the gray Sunflower poised against the sunset, crackly bleak and dusty with the smut and smog and smoke of olden locomotives in its eye–

corolla of bleary spikes pushed down and broken like a battered crown, seeds fallen out of its face, soon-to-be-toothless mouth of sunny air, sunrays obliterated on its hairy head like a dried wire spiderweb,

leaves stuck out like arms out of the stem, gestures from the sawdust root, broke pieces of plaster fallen out of the black twigs, a dead fly in its ear,

Unholy battered old thing you were, my sunflower O my soul, I loved you then!

![](/content/images/francesco-mazzoli-0xh3QPqcfKM-unsplash.jpg)

The grime was no man’s grime but death and human locomotives,

all that dress of dust, that veil of darkened railroad skin, that smog of cheek, that eyelid of black mis’ry, that sooty hand or phallus or protuberance of artificial worse-than-dirt–industrial–modern–all that civilization spotting your crazy golden crown–

and those blear thoughts of death and dusty loveless eyes and ends and withered roots below, in the home-pile of sand and sawdust, rubber dollar bills, skin of machinery, the guts and innards of the weeping coughing car, the empty lonely tincans with their rusty tongues alack, what more could I name, the smoked ashes of some cock cigar, the cunts of wheelbarrows and the milky breasts of cars, wornout asses out of chairs & sphincters of dynamos–all these

entangled in your mummied roots–and you standing before me in the sunset, all your glory in your form!

A perfect beauty of a sunflower! a perfect excellent lovely sunflower existence! a sweet natural eye to the new hip moon, woke up alive and excited grasping in the sunset shadow sunrise golden monthly breeze!