+++
date = "2015-08-26T01:23:01+03:00"
description = ""
title = "Install Amazon S3 AWS-cli"
+++
### What is AWS-cli?

AWS-CLI is a comand line tool that helps you manage your bucket from a command line. That's right! once configured you can push and delete your files from your S# bucket via command line.

### How do I install it?

Since this is built in python,weel, first you have to have python installed. To check that and see it's version

```
python --version
```

Then Download the installer:
```
curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"
```
if you don't have curl installed install it!

Then unzip the archive: 
```
unzip awscli-bundle.zip
```

To install just do:
```
sudo ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws
```

That is all, you now have aws-cli installed. Configuring and using it is another story for another post.
