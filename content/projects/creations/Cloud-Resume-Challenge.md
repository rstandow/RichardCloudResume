---
title: "Cloud Resume Challenge"
date: 2022-08-29T14:29:22+07:00
featured: true
description: "MY AWS Cloud Resume Challenge"
tags: ["AWS","CSS","CloudFront","Load Balancer","EC2","S3","WAF","Lambda","Rest API"]
image: "img/NetworkDiagram1.webp"
link: "https://richard.hitechmadeez.com/projects/creations/cloud-resume-challenge.html"
fact: ""
weight: 5
sitemap:
  priority : 0.8
---
  
  
{{< figure src="/img/NetworkDiagram.webp" alt="Network Diagram" >}}

As I lack proof of cloud skills working for others, I put this project together to showcase my skills. You may ask "What is Cloud Resume Challenge"? let me use a bit of Prompt engineering and see what GPT3 says "As more and more businesses move to the cloud; they are looking for ways to leverage this new technology to improve their bottom line. One way they are doing this is by challenging their employees to create resumes that are stored in the cloud.
The cloud resume challenge is a way for businesses to encourage their employees to create resumes that are stored in the cloud. This way, if an employee leaves the company, their resume is still stored in the cloud and can be accessed by the new employer.
This challenge can be used to improve employee retention, as well as to help businesses save money on printing and storing paper resumes. It is also a way to encourage employees to keep their resumes up to date.
If you are a business owner or manager, you can encourage your employees to participate in the cloud resume challenge by offering a prize for the best resume. This can be a monetary prize, or it can be something like a free day off.
To get started, all you need to do is create a cloud storage account and give your employees access to it. Then, challenge them to create the best resume they can. The sky's the limit!"  Interesting that GPT3 used the approach of looking at it from an employers point of view. 
<br>
I used this template from this site https://cloudresumechallenge.dev/docs/the-challenge/aws modified it a bit, by adding more to it and over the time I will add more functionality to this page and hitechmadeez.com.  
  
**Here are the steps I took with a breakdown**  
<br>  
1. Certification  
I have finished both the AWS training for Practitioners, and Solutions Architect. I will wait until I am back in the US to take the test, which should be Nov or Dec 22.
2. HTML
3. CSS  
For section two and three I decided to learn a markdown compiler called **Hugo** to challenge myself and see how well it generates CSS files. It has been a journey learning Hugo and seeing what it can do.
4. Static Website  
This resume site is a static site hosted on S3 container with its www counterpart also on S3 container pointing to the root S3 container also kept as failover if needed. 
I also created a dynamic site, the root domain of this one https://www.hitechmadeez.com that uses Wordpress. This allowed me to practice using WordPress and keeping it secure and up to date and other AWS services S3 bucket for offsite image storage, VPC, Load Balancer, EC2, AMI Image, Snapshots, CloudFront, WAF. I also set up a mail server. I had to set up an SMTP relay since most cloud providers do not allow mail servers without special permission.
5. HTTPS  
This site is secured with CloudFront SSL cert the root domain www is CloudFront cache while dev. and other testing environments that I used a lets encrypt and wildcard for mail and sub domains
6. DNS  
The lamp stack server has its internal DNS for name servers for other sub domains. This and main site are hosted through Route53 
7. JavaScript  
I have a basic understanding of the syntax of JavaScript. I would not say I am fluent in using it yet. It is on my list of to do though. The visitor counter is making its API call using JavaScript that sends a get through a lambda function that increments the count in DynamoDB.Returns the database value. 
8. Database  
This site using DynamoDB for counter and few other things  
WordPress site is on MySQL 
9. API
Using AWS Rest HTTP Gateway with a lambda trigger to increment the page counter.  
I will be honest java is my weak area I have all the connections working its just the display format. When it renders the result it clears all the formatting here and I am trying to figure out why. With moving back to the US I am super busy. So I have just made a call with another API  
Visits to this page
{{< pagecounter >}}  
Here is my Java that makes the AWS call that is displaying incorrectly. [Git Repo With Page Counter](https://github.com/rstandow/pagecounterAWS.git)
10. Python
Not a whole lot of Python is used on this project except the lambda function that calls the DynamoDB.I do plan on adding more later.
11. Tests
All throughout this project I developed dev environments and conducted tests to ensure the code worked. I use CloudWatch for various segments to monitor errors and downtime.I am using CloudFront Health check and another outside party to monitor this site and others I am hosting for friends and family. 
12. Infrastructure as Code
This area I struggled a bit. As I am still learning all the services of AWS and how they interact with each other. I found it difficult to write code in Json or Yaml without exploring what service did what it wanted using the GUI.
13. Source Control
I am using Visual Studio and uploading to git for source control. I have the S3 buckets versioning. I even played with AWS Config service, though I had too many rules after a couple days I turned this off as I was constantly making changes in several areas.
14. CI/CD (Back end)
I am running github workflow to push from local computer to github then to S3 bucket
15. CI/CD (Front end)
I will use GitHub with pipeline to push updates to this site
16. Blog post  
I created a resume and FAQ page so that people can download my [Resume or CV]({{< ref "/blog/resume FAQ.html" >}} "Resume or CV") and cover some FAQ questions you may have.  


  
  
     **Thankyou for visiting**
