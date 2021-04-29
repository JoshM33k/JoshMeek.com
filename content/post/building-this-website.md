---
title: "Dead-Simple Websites with Hugo and Netlify"
date: "2019-09-07"
draft: false
tags: ["development", "web", "Hugo", "Netlify"]
toc: false
---
This is a quick explanation of how this website is built, which will serve as a "living document" that will be updated as changes and additions are made.

I've been making websites for years. I used to be a fan of self-hosted [Wordpress](https://wordpress.org/) blogs, however Wordpress sites are increasingly the target of malicious attacks. A nefarious party can gain access to the backend of your site, deleting files, changing content, and even locking you out. Plus, Wordpress is _slow_, on an internet that [increasingly needs to go on a diet](https://blog.codinghorror.com/an-exercise-program-for-the-fat-web/).

So, after becoming frustrated with Wordpress and other "program-running-on-a-server" CMS solutions, I discovered static site generators. [Jekyll](https://jekyllrb.com/) being the most popular, these generators take [Markdown](https://daringfireball.net/projects/markdown/) text files and a little bit of html and css, and spit out static website files ready to be deployed. There's nothing web-accessible to log into, it's just html and css, which means the deployed sites are blazing fast and super-secure. Plus, you get the added benefit of writing your content in text files that get turned into beautiful webpages, automatically.

## Hugo

After trying out several static site generators, I settled on using [Hugo](https://gohugo.io/) for this website. Hugo is easy to install on Windows and is the fastest of all the generators I tried.

The easiest way to install Hugo on Windows is [using the package manager Chocolatey](https://gohugo.io/getting-started/installing/#chocolatey-windows).

I recommend reading the [Hugo Quick Start](https://gohugo.io/getting-started/quick-start/), it's really all you need to get started creating your site and running your Hugo server, which will watch for file changes and continually rebuild as you edit. With the server running, you can preview your site at localhost:1313/.

## Github

[Github](https://github.com/) is the easiest places to store your websites files. You'll want to make sure not to commit the /public folder in your Hugo directory by adding it to your .gitignore, as those are generated files, and our continuous deployment will re-generate these each time we push a new commit. For this particular site, I'm using the [Cupper theme](https://github.com/zwbetz-gh/cupper-hugo-theme). The theme is installed via a git submodule. In order to update the theme, from the root of this site, you simply run: {{< cmd >}}git submodule update --remote --merge{{< /cmd >}}

## Netlify

Github has the ability to turn your static website files into a working site using [Github Pages](https://pages.github.com/), but for this site I'm using [Netlify](https://www.netlify.com/). Netlify is *great* and I've only just begun to scratch the surface of what it offers. You can login to Netflify using your GitHub credentials. Once logged in, choose "New Site From Git" and choose your Github repository.

Once your site is created, you can configure the settings. In Build & Deploy, you can specify the build command. For a Hugo site, that just needs to be "Hugo". Everytime you push a new commit to GitHub, Netlify will build your site using your build command, and redeploy the generated static files, updating your website!

If you need further customization, you can add a file to the root of your git repository called [netlify.toml](https://www.netlify.com/docs/netlify-toml-reference/). Netlify will read this file, and customize their handling of your site. I added the netlify.toml file so that I could customize the version of Hugo being used to build my site; the theme I have chosen requires at least version .54.

## Maintaining the site

Yes, it's that simple to set up true continuous integration for your website using Hugo and Netlify. All my content is in plaintext markdown files, and are easily transportable to other formats as needed. I can write new posts anywhere, even on my phone. Then, adding a new post to my website is as simple as committing to my git repository, and Netlify picks up the commit and handles the entire build process.
