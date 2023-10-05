# Hosting a static website on AWS S3 and CI/CD pipeline with AWS

<p>In this project I would like to walk through the complete pipeline to deploy a static website on AWS using on AWS S3, CloudFront, ACM, Route53.<br>
The last part of the project will be dedicated to the setup of a CI/CD pipeline. <br>
<br>Before guiding you in the development of the project I have previously designed a simple HTML portfolio website for a friend of mine.
Why using CloudFront?
</p>

<h1>1. Create a S3 Bucket </h1>
<p>In the S3 console we will create two different buckets: first will be with the 'www'. the second will be without the 'www'; the reason is because. <br>
In the bucket name we insert the actual name of the website with the 'www' followed by the '.cloud' (example). <br>
We wont disable the 'Block all public access' for now and we leave the 'default encryption' as it is.<br>
We hit the 'Create Bucket' button at the end of the page.<br>
The following pictures follow the description. <br>
<img src="pictures/1.S3 bucket.png" alt="1.S3Bucket">
<img src="pictures/2.S3 bucket.png" alt="2.S3Bucket"> <br>
<br>
Create another S3 bucket without add the 'www' before your website domain name.
After created these two buckets, we upload our website file in the www.mental-image.cloud
Once the upload is complete we need to enable the public settings for our bucket.
<br>We can do these changes in the 'Permission' tab: we scroll to the 'Block public access' and we want to disable this setting that is on by default.<br>
<br><img src="pictures/3.S3 bucket.png" alt="3.S3Bucket">
<br> Then we need to set up a policy bucket in the policy tab.<br>
The added policy is an AWS S3 bucket policy. It allows public read access to objects in the specified bucket.<br> 
The policy grants the s3:GetObject permission to all AWS accounts and requires that any requests for these objects must be authenticated. The policy uses the wildcard character (*) to allow access to all objects in the bucket.
<br>
<img src="pictures/4.S3 bucket.png" alt="4.S3Bucket">
<br>
The last modification we want to do on this S3 bucket is to enable 'Static Website Hosting' on the 'Permission' panel; for the 'Hosting Type' we set 'Host a static website' and last but not least we set as default page our index.html file.
<br>Once we completed all these steps our website is about ready to be public, but if we search on the browser our domain we can't still see a thing.
<br>That's why we now need to redirect on the other S3 bucket.
<br>So on the other S3 bucket we created we go to the 'Properties' tab and scroll to the bottom until we find once again the 'Static website hosting' to edit. Instead of choosing 'Hosting a static website' we want to choose 'Redirect request for an object' and the 'Host name' field we want to add the name of our other bucket 'www.mental-image.cloud' and for now we set the protocol as 'Http' and we hit 'save changes'.
<br><img src="pictures/5.S3 bucket.png" alt="5.S3Bucket">
</p>
