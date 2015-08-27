+++
date = "2015-08-28T00:44:07+03:00"
description = "How to install and use s3cmd walktrough"
title = "Installing and using s3cmd"
+++

### Download

Go to http://sourceforge.net/projects/s3tools/files/s3cmd/ , select the latest version folder and download the tar.gz file.
Unzip it with 
```
tar -zxvf <filename>
```
### Install
First make sure you have python setup tools installed. To install run:
```
sudo apt-get install python-setuptools
```
Then go inside your unpacked previously directory and run:
```
sudo python setup.py install
```
And that's it for installing. Now configuring and using:
### Configuring
To configure, run:
```
s3cmd --configure
```
* You will be prompted for Access key and Secret Key. These are crucial and you have to generate some. Go here: https://console.aws.amazon.com/iam/home?#security_credential to the Access Keys and press the Create New access Key button to create a new one. The copy and paste it in the comand line when you get prompted.
* Then you will be asked for region, just hit enter.
* Then Encryption password. Set what ever you want.
* Path to GPG program, just hit enter.
* Path to GPG program, just hit enter.
* Save the changes Press Y and hit enter.

### Pushing files to bucket

All you're left with now is to push files to your bucket. Here's how you do it: 

1. You go in the directory containing the files you want to push
2. You type:
```
s3cmd put * s3://bucket-name/path -r --continue-put
```
This checkes each file's md5 and file size and skips them if they are different.

* is for everything
-r is for recursive
--continue-put is only uploading files that don't exist or have the size or MD5 different on the server

For a faster run do
```
s3cmd sync ./  s3://bucket-name/path

```

That's all, fwew, go have some coffee
