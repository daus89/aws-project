# aws-project
Static Website Hosting
Objective:
Host a static website on AWS.
Tools/Services:
Amazon S3, Amazon Route 53, Amazon CloudFront.
Steps:
1.	Create an S3 Bucket:
o	Log in to the AWS Management Console.
o	Navigate to the S3 service.
o	Click "Create bucket."
o	Enter a unique bucket name and select a region.
o	Configure bucket settings and permissions to enable public access (this is necessary for static website hosting).
o	Click "Create bucket."
2.	Upload Website Files:
o	Select your newly created bucket.
o	Click "Upload" and select your static website files (HTML, CSS, JavaScript).
o	Click "Upload."
3.	Configure the S3 Bucket for Website Hosting:
o	In the bucket properties, navigate to "Static website hosting."
o	Select "Use this bucket to host a website."
o	Specify the index document (e.g., index.html) and the error document (e.g., error.html).
o	Save the configuration.
4.	Set Up Route 53 for Custom Domain:
o	Navigate to the Route 53 service.
o	Click "Hosted zones" and "Create hosted zone."
o	Enter your domain name and create the zone.
o	Note the nameservers provided by Route 53.
o	Update your domain's DNS settings with these nameservers.
5.	Configure CloudFront:
o	Navigate to the CloudFront service.
o	Click "Create Distribution" and select "Web."
o	Enter the URL of your S3 bucket.
o	Configure settings (such as caching behavior) and create the distribution.
o	Note the CloudFront domain name and use it in your Route 53 settings to point your domain to the CloudFront distribution.
