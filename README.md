<picture><source media="(prefers-color-scheme: dark)" srcset="https://nextwork.ai/static/nextwork-logo-paper.svg" /><img src="https://nextwork.ai/static/nextwork-logo-leather.svg" alt="NextWork" width="300" /></picture>

# Host a Website on Amazon S3

**Project Link:** [View Project](https://nextwork.ai/projects/70e2d059-31ab-5f67-8c58-f5edbd451140)

**Author:** Stuart

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to host a static website using Amazon S3 (Simple Storage Service). The goal of this project is to gain hands-on experience with AWS cloud services and better understand how websites can be stored, configured, and hosted in the cloud.

### Tools and concepts

Services I used were S3 buckets, policies, objects, policies Key concepts I learnt include how to create buckets, website hosting, ACLS, bucket policies.

### Time, challenges, and wins

This project took me approximately 30 minutes to complete. The most challenging part was the JSON bucket policy. It was most rewarding to see the website working.


## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will create an Amazon S3 bucket to store the files needed for my website, such as HTML files, images, and other content. The S3 bucket will act as the storage location for my website files, allowing me to manage them and eventually make the website accessible online.

### How long it took to create the bucket

Creating an S3 bucket took me less than five minutes.

### Region selection

The Region I picked for my S3 bucket was North Virgina  because it was the closest region to me.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means no two Amazon S3 buckets can have the same name.

![How I Set Up an S3 Bucket](https://nextwork.ai/stuart/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_ba6d42ad)

## Upload Website Files to S3

### What I did in this step

In this step, I will download an HTML file, a zip file, and upload them into my S3 Bucket because our bucket is still empty.

### Files I uploaded

I uploaded two files to my S3 bucket - they were the index.html and NextWork - Everyone should be in a job they love\_files.

### How the files work together

Both files work together to make the website function properly. The index.html file serves as the main homepage and provides the structure and content of the website, while the other file supports how the website looks or functions. Both are needed to ensure the website displays correctly when hosted through Amazon S3.

![Upload Website Files to S3](https://nextwork.ai/stuart/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_a265af88)

## Static Website Hosting on S3

### What I did in this step

In this step, I will configure my S3 bucket for static website hosting and visit my public website link because we need to configure the website hosting to be able to publicly access the website.

### Understanding website hosting

Website hosting is the process of storing a website's files on a server so people can access it over the internet.

### How I enabled website hosting

To enable website hosting with my S3 bucket, I went into my bucket clicked properties and went all the way down to static website hosing and hit enable.

### Access Control Lists (ACLs)

An Access Control List (ACL) is a set of rules that controls who can access an AWS resource and what permissions they have. For this project, I enabled ACLs on my S3 bucket to allow more control over who can access the files stored inside it.

![Static Website Hosting on S3](https://nextwork.ai/stuart/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_c22c54c0)

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is http://nextwork-website-project-stuartdiperna.s3-website-us-east-1.amazonaws.com

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw 403 Forbidden error The reason for this error was the objects in my bucket are private by default.

![Bucket Endpoints](https://nextwork.ai/stuart/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_22ce4daf)

## Success!

### What I did in this step

In this step, I will make my website files in S3 publicly accessible so I can access my website live on the internet.

### How I resolved the 403 error

To resolve this 403 Forbidden error, I went to object in my bucket selected my two files clicked action and selected make file public.

### ✅ What were the key services and concepts you learnt in this project?

Services I used were S3 buckets, policies, objects, policies Key concepts I learnt include how to create buckets, website hosting, ACLS, bucket policies.

### ✅ How long did it take you to complete this project?

This project took me approximately 30 minutes to complete. The most challenging part was the JSON bucket policy. It was most rewarding to see the website working.

### ❤️ Thanks for doing this project!

I chose to do this project today because I want to become more comfortable with AWS and could services. Something that would make learning with NextWork even better is I do not know its pretty good.

![Success!](https://nextwork.ai/stuart/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_5d4474f9)

## Bucket Policies

### What I did in this extension

In this project extension I'm about to block people from deleting my index.html file. I'm doing this so that nobody can delete my file by accident or on purpose.

### Understanding bucket policies

An alternative to ACLs is a bucket policy, which is a JSON-based rule that controls access to an entire S3 bucket and the objects inside it. Bucket policies let you manage permissions for multiple users and objects in one place, while ACLs are useful for setting basic permissions on individual objects or buckets.

![Bucket Policies](https://nextwork.ai/stuart/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_sm2sm2sm)

### What my bucket policy does

My bucket policy prevent my index.html file from being deleted. I tested this by deleting the index file and saw a failed to delete objects error.
