---
date: 2015-08-27T06:56:31Z
description: "Simple basics on using HuGO"
title: "Using huGO"
categories: ["Hugo","Blog","tutorial"]
tags: ["Hugo","Go","tutorial"]
---

###Creating a site

All you need to create a site is to go in the folder you want to create your site and write:
```
hugo new site site-name
```
instead of "site-name" you can use "/path/to/site". The site name is going to be a directory. When ever you want to run HuGO commands for that site you need to be in the site root folder.

###Configuring a bit

Once you ran the above command, all the site files will be generated. Now we need to configure it. Let's say we want the domain of this to be your-website.com. To make HuGO generate for that particular website.website.
To do this we need to edit config.toml that is in the root of the site.
here you have to have this variable:
```
baseurl = "http://your-site.com/"
```
You can also set a site title:
```
title = "Your Site title"
```
You can set the theme:
```
theme = "cactus"
```
The theme name has to be the directory name in the root of the hugo site/themes/

To download all the available themes for hugo run in the themes directory:
```
git remote add origin https://github.com/spf13/hugoThemes.git
git pull origin master
```
And voila, you have all the themes in the themes directory


You can set other parameters:
```
[params]
  description = "Site description goes here"
  author = "Your full name"
  cover = "images/cover.jpeg"
  logo = "images/logo.jpeg"
  githubName = "whatever"
  twitterName = "whatever"
  facebookName = "whatever"
```
The images you place in content/images and they will be added to the theme in the compiled version of the theme in the images folder.
### Create a Post

To create a post just type:
```
hugo new posts/your-post-name.cmd
```
and then go to content/posts/your-post-name.md and edit that.

In there you will have:
```
+++
date = "2015-08-26T01:23:01+03:00"
description = "Your post description goes here"
title = "Your post title goes here"
draft = true
+++

Your post content goes here. Use markup language to style it
```

### Create a page:
Just like post you do:
```
hugo new page/your-page-name.cmd
```
And that's a page not a post.

This is pretty much it, the basics. More to come soon!
