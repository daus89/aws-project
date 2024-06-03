# aws-project
1. Static Website Hosting
Objective:
Host a static website on AWS.
Tools/Services:
Amazon S3, Amazon Route 53, Amazon CloudFront.
Steps:
## 1.	Create an S3 Bucket:
•	Log in to the AWS Management Console.
•	Navigate to the S3 service.
•	Click "Create bucket."
•	Enter a unique bucket name and select a region.
•	Configure bucket settings and permissions to enable public access (this is necessary for static website hosting).
•	Click "Create bucket."
2.	Upload Website Files:
•	Select your newly created bucket.
•	Click "Upload" and select your static website files (HTML, CSS, JavaScript).
•	Click "Upload."
3.	Configure the S3 Bucket for Website Hosting:
•	In the bucket properties, navigate to "Static website hosting."
•	Select "Use this bucket to host a website."
•	Specify the index document (e.g., index.html) and the error document (e.g., error.html).
•	Save the configuration.
Steps to Ensure Public Access
4.	Check Block Public Access Settings:
•	Go to the S3 service in the AWS Management Console.
•	Select your bucket.
•	Go to the "Permissions" tab.
•	Look for "Block public access (bucket settings)".
•	Click "Edit".
•	Ensure all the "Block public access" settings are turned off (uncheck all boxes).
•	Save changes.

5.	Bucket ACL (Access Control List):
•	While in the "Permissions" tab, scroll down to "Bucket ACL".
•	Ensure the bucket ACL allows public read access.
•	Add the following grant to the ACL:
1.	Grantee: Everyone
2.	Permissions: List objects
6.	Object Permissions:
•	Go to the "Objects" tab.
•	Select all your objects (e.g., index.html, styles.css, script.js).
•	Click "Actions" > "Edit public access settings".
•	Ensure that "Public access" is set to allow for these objects.

7.	Set Up Route 53 for Custom Domain:
•	Navigate to the Route 53 service.
•	Click "Hosted zones" and "Create hosted zone."
•	Enter your domain name and create the zone.
•	Note the nameservers provided by Route 53.
•	Update your domain's DNS settings with these nameservers.
8.	Configure CloudFront:
•	Navigate to the CloudFront service.
•	Click "Create Distribution" and select "Web."
•	Enter the URL of your S3 bucket.
•	Configure settings (such as caching behavior) and create the distribution.
•	Note the CloudFront domain name and use it in your Route 53 settings to point your domain to the CloudFront distribution.
