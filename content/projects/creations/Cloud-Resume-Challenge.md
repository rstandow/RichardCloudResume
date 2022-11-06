---
title: "Cloud Resume Challenge"
date: 2022-08-29T14:29:22+07:00
featured: true
description: "MY AWS Cloud Resume Challenge"
tags: ["AWS","CSS","CloudFront","Load Balancer","EC2","S3","WAF","Lambda","Rest API"]
image: "img/NetworkDiagram.webp"
link: "https://richard.hitechmadeez.com/projects/creations/cloud-resume-challenge.html"
fact: ""
weight: 5
sitemap:
  priority : 0.8
---
  
  
{{< figure src="/img/NetworkDiagram.webp" alt="Network Diagram" >}}

# What is a Cloud Resume?  

> The Cloud Resume Challenge is a multiple step resume project which helps build and demonstrate skills fundamental to pursuing a career as an Cloud Engineer. The project was first published by Forrest Brazeal. who works at A Cloud Guru, a cloud education company. [Linkdin]( https://www.linkedin.com/pulse/cloud-resume-challenge-abraham-musa#:~:text=The%20Cloud%20Resume%20Challenge%20is,Guru%2C%20a%20cloud%20education%20company) 

<br>
I used this template from this site https://cloudresumechallenge.dev/docs/the-challenge/aws modified it a bit, by adding more to it and over the time I will add more functionality to this page and hitechmadeez.com.  
  
**Here are the steps I took with a complete breakdown**  
<br>  
1. Certification  
I have finished the AWS training for Practitioners, and Solutions Architect. I just moved back to the States Nov 6th still getting from Thailand. I plan on taking the certifactions in a month or two.
2. HTML
3. CSS  
For section two and three I decided to learn a markdown compiler called **Hugo** to challenge myself and see how well it generates CSS files. It has been a journey learning Hugo and seeing what it can do. I am still working on image processing for this static site. This has been a bit more tricker than I thought it would be.
4. Static Website  
This resume site is a static site hosted on two serpeate S3 Containers. Non www is main container and the www. container for redirect and also serving as backup if needed.  
I created a dynamic site, the root domain of this one https://www.hitechmadeez.com that uses WordPress. I had setup an entire cloud network based on the diagram in AWS but the cost of running EC2 and license and coming back to live in the US, I turned off most of the services.I moved the hitechmadeez.com to cheap cloud hosting provider still working on it. You can see more information on what I did here [HiTechMadeEZ Project]({{< ref "/projects/creations/hitechmadeez-website.md" >}} "HiTechMadeEZ Project")
5. HTTPS  
This site is secured with CloudFront SSL certificate issued from AWS.
6. DNS  
I was using route 53 and may move back over. Right now I am using the DNS provided by my new hosting company and setup a CDN using Litespeed CDN. I have the pageingihts score at 99 mobile and 100 Desktop. I may move back to route 53 when I have the funds to pay for other cloud projects I have planned.
7. JavaScript  
This is my weak area I am having displaying issues with my counter. 
8. Database  
This site using DynamoDB for counter and few other things  
WordPress site is on MySQL 
9. API
Using AWS Rest HTTP Gateway with a lambda trigger to increment the page counter.  
I will be honest java is my weak area I have all the connections working its just the display format. When it renders the result, it clears all the formatting here and I am trying to figure out why. With moving back to the US, I am super busy. So, I have just made a call with another API  
Visits to this page
{{< pagecounter >}}  
Here is my Java that makes the AWS call that is displaying incorrectly. [Git Repo With Page Counter](https://github.com/rstandow/pagecounterAWS.git)
10. Python
Not a whole lot of Python is used on this project except the lambda function that calls the DynamoDB. I do plan on adding more later.
11. Tests
All throughout this project I developed dev environments and conducted tests to ensure the code worked. I use CloudWatch for various segments to monitor errors and downtime. I am using CloudFront Health check and another outside party to monitor this site.
12. Infrastructure as Code
I am still learning all the services of AWS and how they interact with each other. I found it difficult to write code in Json or Yaml without exploring what service did what and found it easier to use GUI to get an idea on how they worked together.
13. Source Control
I am using Visual Studio and uploading to git for source control. I have the S3 buckets versioning turned on. I even played with AWS Config service, though I had too many rules after a couple days I turned this off as I was constantly making changes in several areas.
14. CI/CD (Back end)
I am running GitHub workflow to push from local computer to GitHub then to S3 bucket
15. CI/CD (Front end)
I will use GitHub with pipeline to push updates to this site
16. Blog post  
I created a resume and FAQ page so that people can download my [Resume or CV]({{< ref "/blog/resume FAQ.html" >}} "Resume or CV") and cover some FAQ questions you may have.  


  
  
     **Thankyou for visiting**

