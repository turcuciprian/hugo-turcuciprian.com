+++
date = "2015-08-27T06:56:31Z"
description = "Simple basics on using HuGO"
title = "Using huGO"

+++

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
