# Hosting a static website on AWS S3 plus CI/CD pipeline with AWS

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
The following pictures follow the description.
'![](https://github.com/ciakdewitt/hostingwebsiteonawsS3/blob/9fd74486a207d83d048650fefd025ee2d67b4dc3/pictures/1.S3%20bucket.png)'
</p>
