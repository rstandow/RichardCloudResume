---
title: "Cloud Resume Challenge"
date: 2022-08-29T14:29:22+07:00
featured: true
description: "MY AWS Cloud Resume Challenge"
tags: ["AWS","CSS","CloudFront","Load Balancer","EC2","S3","WAF"]
image: ""
link: ""
fact: ""
weight: 5
sitemap:
  priority : 0.8
---
As I lack proof of cloud skills working for others, I put this project together to showcase my skills. You may ask "What is Cloud Resume Challenge"? let me use a bit Prompt engineering and see what GPT3 says "As more and more businesses move to the cloud; they are looking for ways to leverage this new technology to improve their bottom line. One way they are doing this is by challenging their employees to create resumes that are stored in the cloud.
The cloud resume challenge is a way for businesses to encourage their employees to create resumes that are stored in the cloud. This way, if an employee leaves the company, their resume is still stored in the cloud and can be accessed by the new employer.
This challenge can be used to improve employee retention, as well as to help businesses save money on printing and storing paper resumes. It is also a way to encourage employees to keep their resumes up to date.
If you are a business owner or manager, you can encourage your employees to participate in the cloud resume challenge by offering a prize for the best resume. This can be a monetary prize, or it can be something like a free day off.
To get started, all you need to do is create a cloud storage account and give your employees access to it. Then, challenge them to create the best resume they can. The sky is the limit!"  Interesting that GPT3 used the approach looking at it from an employer’s point of view. 
<br>
I used this template from this site https://cloudresumechallenge.dev/docs/the-challenge/aws modified it a bit by adding more to it.  
**Here are the steps I took with a breakdown**  
1. Certification  
I have finished both the AWS training for Practitioners, and Solutions Architect I will wait until I am back in the US to take the test
2. HTML
3. CSS  
For section two and three I decided to learn a markdown complier called **Hugo** to challenge myself and see how well it generates CSS files. It has been a journey learning it and see what it can do.
4. Static Website  
This resume site is static site hosted on S3 container with its www counterpart S3 container pointing to the root S3 container. 
I also created dynamic site the root domain of this one https://www.hitechmadeez.com. This allowed me to practice using WordPress and keeping it secure and up to date and other AWS services S3 bucket for offsite image storage, VPC, Load Balancer, EC2, AMI Image, Snapshots, CloudFront, WAF. I also setup a mail server I had to setup SMTP relay since most cloud providers do not allow mail servers without special permission.
5. HTTPS  
This site is secured with CloudFront SSL cert the root domain www is CloudFront cache while dev. and other testing environments that I used a let’s encrypt and wildcard for mail and sub domains
6. DNS  
The lamp stack server has its internal DNS for name server for other sub domains. This and main site are hosted through Route53 
7. JavaScript  
I am familiar with JavaScript I would not say I am fluent in using it yet. It is on my list though. The visitor counter is making its API call using JavaScript.
8. Database  
This site using DynamoDB for counter and few other things  
WordPress site is on MySQL 
9. API
Using AWS Rest HTTP Gateway with a lambda trigger to increment the page counter.
10. Python
Not a whole lot of Python is used on this project except the lambda function that calls the DynamoDB.
11. Tests
All throughout this project I development dev environments and conducted test to ensure the code worked. I use CloudWatch for varies segments to monitor errors and downtime. 
12. Infrastructure as Code
This area I struggled a bit. As I am still learning all the services of AWS and how they interact with each other. I found it difficult to write code in Json or Yaml without exploring what service did what it wanted using the GUI.
13. Source Control
I am using Visual Studio and uploading to git for source control. I have the S3 buckets versioning. I even played with AWS Config, but the cost was bit much after a couple days as I was constantly making changes in several areas.
14. CI/CD (Back end)
Will have to work on some more features for the sites so I can package test and deploy 
15. CI/CD (Front end)
I will use GitHub with pipeline to push updates to this site
16. Blog post  
I created a resume and FAQ page so that people can download my resume and cover some FAQ questions people may have.
