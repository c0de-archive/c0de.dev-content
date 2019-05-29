Title: Hello World!
Date: 05/28/2019 20:15
Tags: pelican, blog, experimentation
Summary: The first true post of the blogging platform

## The birth of a new blog. 

Well. Here it is. Not much to look at, and I'll have to see if I can keep up the drive to post here.
This post will walk you through how I went about setting up this blog.

So I've been wanting to make a blog for a little while, and some of my friends have been experimenting with [Pelican](https://getpelican.com/).
Over Memorial Day weekend, I started pouring over the [documentation](https://docs.getpelican.com/en/stable/quickstart.html) and created a [repository](https://github.com/alopexc0de/c0de.dev-blog) for the configuration. This mostly contains the configuration needed to run the whole show.

All of the plugins, the theme, and the content are loaded in via git [submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules), mostly as an experiment as I don't work with them too often.
The blog configuration and theme are open source with the MIT license, so feel free to replicate this is you want. 

Currently the plugin configuration is a little sparse, so I will probably be refining that in the future. I'm able to encrypt blog posts, and have them able to be decrypted purely in client space; this is one of the main reasons that the content is in a private repository.
I spent a good long while searching for a proper theme, and ultimately settled on [mg](https://github.com/alopexc0de/pelican-mg). The version I linked is my fork, as I found that the most updated fork was quite outdated and had a few places that were in a different language.

## Cool and all, but how can I use this platform?

Basically this can be built on any system that supports python 3, and the heavy lifting is done by using a couple make files. To get started, clone the repo and follow the readme. You will have to change the submodule for the content.
When you want to update any content, it's basically just `cd pelican; make clean; make html`. Now the entire site should be stored in `output`. You can symlink this directory to your webserver root and *bam* instant blog.

To write new blog posts, simply update the content repo and pull down the changes in the blog. 
