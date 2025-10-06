<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** Justine Jurel Valenzuela  
**Email:** valenzuela.justinejurel@gmail.com

---

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

In this project, I will demonstrate how to create and configure an Amazon S3 bucket to store and host static files for a simple website.

I’m doing this project to learn how Amazon S3 works, understand how to host a website using cloud storage, and gain hands-on experience managing cloud-based file storage.

### Tools and concepts

Services I used were Amazon S3 and AWS Management Console to create a bucket, upload files, and enable static website hosting.

Key concepts I learned include how to store and host files in S3, how ACL(Access Control List) and bucket policies work, and how to make a website publicly accessible through static website hosting.

### Project reflection

This project took me approximately 45 minutes to complete. The most challenging part was making the files public before the website could be displayed successfully. I checked the help section and watched the tutorial video to understand where I went wrong.

It was most rewarding to finally see my website go live after fixing the permissions and knowing that I had set up everything correctly from start to finish.

---

## How I Set Up an S3 Bucket

Creating an S3 bucket took me around 10 minutes

The Region I picked for my S3 bucket was Asia Pacific (Tokyo) because I’m currently residing in the Philippines, and Tokyo is the nearest AWS data center in the Asia Pacific region. Choosing a nearby region helps ensure faster access speeds and lower latency when uploading or retrieving files.

S3 bucket names are globally unique, which means that no two AWS users anywhere in the world can have buckets with the same name. Once you create a bucket name, it’s reserved for your account until you delete it; only then can someone else use that name.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### index.html and image assets

I uploaded two files to my S3 bucket - they were the index.html file and NextWork - Everyone should be in a job they love_files folder.

Both files are necessary for this project as index.html is the structure of the website, and the folder that I added is the images for the website

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

Website hosting means making my website viewable to the public so that anyone with the link can access and browse it online.

To enable website hosting on my S3 bucket, I opened the bucket properties, found the “Static website hosting” option, and turned it on. Then, I selected “Host a static website” and set the index document to “index.html” to make my site accessible online.

An Access Control List (ACL) is a feature in Amazon S3 that defines who can access your bucket and what actions they can perform, such as reading or writing files.

Yes, I enabled ACLs to have more control over permissions and to manage access to specific users or objects in my S3 bucket

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

Once static website is enabled, S3 produces a bucket endpoint URL, which is like a website URL that lets users to view my S3 bucket as a website.

When I first visited the bucket endpoint URL, I saw an error message: “403 Forbidden.” This happened because my bucket was public, but the files inside were still private, meaning they didn’t have the right permissions to be viewed publicly.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

To resolve this 403 Forbidden error, I updated my buckets object settings and make it publicly

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

An alternative to ACLs is bucket policies, which let you control who can delete, update, or add files in your bucket.

The benefit of bucket policies is that, while ACLs work for simple permissions, bucket policies are easier to manage and give you more control over access.

My bucket policy is preventing my objects or files from being deleted. I tested this by trying to delete the index.html file, but I received an error message saying “Failed to delete object.” The error details at the bottom showed the status “Access Denied,” which confirms that the policy is correctly blocking deletion actions.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-host-a-website-on-s3_sm2sm2sm)

---

---
