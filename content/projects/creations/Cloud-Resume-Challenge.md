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
As I lack proof of cloud skills working for others I put this together to showcase my skills. You may ask "What is Cloud Resume Challenge"? let me use a bit Prompt engineering and see what GPT3 says "As more and more businesses move to the cloud, they are looking for ways to leverage this new technology to improve their bottom line. One way they are doing this is by challenging their employees to create resumes that are stored in the cloud.
The cloud resume challenge is a way for businesses to encourage their employees to create resumes that are stored in the cloud. This way, if an employee leaves the company, their resume is still stored in the cloud and can be accessed by the new employer.
This challenge can be used as a way to improve employee retention, as well as to help businesses save money on printing and storing paper resumes. It is also a way to encourage employees to keep their resumes up to date.
If you are a business owner or manager, you can encourage your employees to participate in the cloud resume challenge by offering a prize for the best resume. This can be a monetary prize, or it can be something like a free day off.
To get started, all you need to do is create a cloud storage account and give your employees access to it. Then, challenge them to create the best resume they can. The sky is the limit!" 
<br>
I used this template from this site https://cloudresumechallenge.dev/docs/the-challenge/aws modified it a bit by adding more to it.  
**Here are the steps I took with a breakdown**  
1. Certification  
I have finished both the AWS training for Practioner and Solutions Architech I will wait until I am back in the US to take the test
2. HTML
3. CSS  
For section two and three I decied to learn a markdown complier called **Hugo** to challenage myself and see how well it generates CSS files using combination of markdown and html
4. Static Website  
This resume site is static site hosted on S3 container 
I also created dynamic site the root domain of this one https://www.hitechmadeez.com. This allowed me to practice using Wordpress and keeping it secure and up to date and other AWS severics S3 bucket for offsite image storeage,VPC,Load Balancer,EC2,AMI Image,Snapshots,Cloudfront,WAF. I also setup a mail server I had to setup SMTP relay since most cloud providers do not allow mail servers without special premission.
5. HTTPS  
This site is secured with CloudFront SSL cert the root domain www is cloudfront cache while dev. and other testing envoirments that I used a lets encrypt and wildcard for mail and sub domains
6. DNS  
The lamp stack server has its internal DNS for namer server for other sub domains. This and main site is hosted through Route53 
7. Javascript  
I am familar wih javascript I would not say I am fluent in using it yet. It is on my list though
8. Database  
This site using DynamoDB for counter and few other things  
Worpress site is on mysql 
9. API
10. Python
11. Tests
12. Infrastructure as Code
13. Source Control
14. CI/CD (Back end)
15. CI/CD (Front end)
16. Blog post  
This page will serve as a ""blog""