---
date: 2020-08-17T15:00:00Z
hero_image: "/content/images/sarah-dorweiler-9Z1KRIfpBTM-unsplash.jpg"
title: Configuring Forestry with Netlify
author: Darren Beattie

---
Using the Gatsby Forestry Starter was a world different from trying to set up a Gatsby Netlify CMS I had played with.

That said, there are still some things a non-technical person will struggle with. The biggest one I can think of is image management.

Forestry gives you multiple options for image management and I might move this to Cloudinary or an S3 bucket as some point but in the meantime (< a dozen posts?) I opted to just GitHub instead.

Git as a protocol, however, does not handle binary information like images particularly well so you need to take it a step further by setting up a protocol called LFS and making some tweaks to your repo.

The following is lifted straight from the [Forestry support site](https://forestry.io/blog/versioning-large-files-with-git-lfs/#setting-up-lfs-in-your-git-repo) but with some minor tweaks based on my experience deploying to Netlify with an Apple computer.

1. Download and install the Git LFS extension [**from the Git LFS website **](https://git-lfs.github.com/)(or on a Mac with Homebrew installed you can simply run `brew install git-lfs`)
2. Navigate to your repo and run `git lfs install`.
3. Run `git lfs track` followed by the file pattern you want. To track all JPG files, for example, run `git lfs track "*.jpg"`(list all that you feel will be relevant but for speed, Google generally likes if you use jpg) 
4. Commit the `.gitattributes` file as well as any existing files that are now tracked in LFS, and push the changes to your remote.
5. **Note:** If you're using Netlify to deploy with git lfs, you'll need to go into the **Settings > Build & deploy > Environment** of the deployed site and enter a new environment variable for your builds:

* Key = `GIT_LFS_ENABLED` 
* Value = `true`

That’s it! You’re now using Git LFS to handle your large binary files directly in GitHub.