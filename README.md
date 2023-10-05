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
Create another S3 bucket without add the 'www' before your website domain name.
<br>
After created these two buckets, we upload our website file in the www.mental-image.cloud
Once the upload is complete we need to enable the public settings for our bucket.
We can to these changes in the 'Permission': we scroll to the 'Block public access' and we want to disable this setting that is on by default.
<img src="pictures/3.S3 bucket.png" alt="3.S3Bucket">
</p>
