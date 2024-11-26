# Presentation website
HTML code used by the static S3 presentation website.

## Presentation
A wordpress instance is hosted on an Ec2. The wordpress files are extracted, using the [simply-static](https://fr.wordpress.org/plugins/simply-static/) plugin.
The files are then auto-synced to the corresponding S3 bucket. 
A CloudFront distribution is used to deliver the static website 24/7, in two aws accounts :
* In **Dev** account, only whitelisted IPs can access the website,
* In **Prod** account, the website is public accessible.
