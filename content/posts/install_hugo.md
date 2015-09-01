+++
date = "2015-08-26T04:46:33+03:00"
description = "Installing the go Website Engine"
title = "Install HuGO"
+++

What's ironic is that I'm creating this page for Hugo to process and generate later. Here's how you install (in Ubuntu) Hugo.

Jump to step 3 if you're doing this from the terminal.
1. Go to :
```
https://gohugo.io/
```
Click "Install" and after it scrolls down click download.
2. Scroll down and select:

```
hugo_0.14_linux_amd64.tar.gz
```
Or whatever version is *_linux_amd64.tar.gz
3. To get this from the terminal:
You can either:
```
wget https://github.com/spf13/hugo/releases/download/v0.14/hugo_0.14_linux_amd64.tar.gz
```
or 
```
curl https://github.com/spf13/hugo/releases/download/v0.14/hugo_0.14_linux_amd64.tar.gz
```
This is of course depending on what you have installed/preffer.
4. Unzip:
```
tar -zxvf hugo_0.14_linux_amd64.tar.gz
```
5. Rename
```
cd hugo_0.14_linux_amd64/
mv hugo_0.14_linux_amd64 hugo
```
6. Move
```
mv hugo /usr/local/bin/
```

And there you have it. Now if you write anywhere: 
```
hugo version
```
You should get a hugo version and see it's working.
