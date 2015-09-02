+++
date = "2015-09-02T12:50:09+03:00"
description = "How to properly configure and use AWS-CLI"
title = "Configuring and using aws-cli"
+++

### Configuring
Run
```
aws configure
```
This will ask you for the following keys:
```
AWS Access Key ID [None]:
AWS Secret Access Key [None]:
Default region name [None]:
Default output format [None]: 
```

Create a new Access key and Secret Access key by going here https://console.aws.amazon.com/iam/home?#security_credential and selecting Access Keys, create new access key and use those credentials.


You have these regions and points:

```
US East (N. Virginia) -	us-east-1
US West (Oregon) - us-west-2
EU (Ireland)	eu-west-1
```
More you can find here: http://docs.aws.amazon.com/general/latest/gr/rande.html#as_region

For default autput format you can add text

### Using

After configuring, just go in your directory that you want to upload to the s3 bucket and do this command:

```
aws s3 sync . s3://bucket-name-goes-here
```

That should be it. If you want to delete files from the s3 bucket that where deleted locally when you sinc add --delete at the end of your command. Ex:

```
aws s3 sync . s3://bucket-name-goes-here --delete
```

