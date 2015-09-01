+++
date = "2015-08-26T02:01:23+03:00"
description = ""
title = "Installing go (golang) on Ubuntu"
tags = [ "linux", "console", "go", "install","terminal" ]
categories = [ "Tutorial","Go" ]
+++

Installing go can be done multiple ways. After installing it via apt-get and trying to install the binary from github, I gave up, downloaded the source and did a much faster and easier install.After a long trial and error and trying to understand why everything I do works and doesn't, I got to a place where I Do these steps exactly and you should be fine.

### Here's how I did it:

I went to:
```
https://golang.org
```
I clicked the Download Go Button that took me to this link:
```
https://golang.org/dl/
```
From the Linux button I clicked to download:
```
https://storage.googleapis.com/golang/go1.5.linux-amd64.tar.gz
```
You can also go in the terminal and to download it you do
```
wget https://storage.googleapis.com/golang/go1.5.linux-amd64.tar.gz
```
or
```
curl https://storage.googleapis.com/golang/go1.5.linux-amd64.tar.gz
```
When it finishes downloading, go inside the terminal to that path where you downloaded or if you downloaded via the terminal don't GO anywhere, you are where you're supposed to be, and do (to unpack) a
```
tar -zxvf go1.5.linux-amd64.tar.gz
```
In my case the file name is go1.5.linux-amd64.tar.gz, It may change in time so be sure to change it accordingly, don't just copy and paste.


great! Now copy (or move, I moved) the extracted directory in /usr/local/bin

You can have it anywhere but let's just move it here.

Don't forget to sudo:
```
sudo go/ /usr/local/bin
```

Update your enviroment variables, so that when you write "go" it loads the go app from where it sits.
```
export GOROOT=/usr/local/bin/go
export PATH=$PATH:/usr/local/bin/go/bin
```

That is all, now if you just write in the terminal:
```
go version
```

That is all, you have all the weapons you need, now GO!

