# 🚀 AWS S3 Static Website Hosting & Versioning Guide

### 📌 Overview

- This guide explains how to use Amazon S3 (Simple Storage Service) to:
---

- Create an S3 bucket

- Upload files

- Host a static website

- Configure public access securely

- Enable and verify bucket versioning

- This setup is commonly used for static websites, portfolios, backups, and learning AWS fundamentals.
---

## 🧠 What is Amazon S3?

- Amazon S3 is a highly scalable, secure, and durable object storage service provided by AWS.
- It allows you to store and retrieve any amount of data from anywhere on the web.

- Common Use Cases:

- Static website hosting

- File storage and backups

- Media hosting

- Version-controlled object storage
---

## 🛠️ Prerequisites

- An active AWS account

- Basic knowledge of AWS Management Console

- A static website file (e.g., index.html)
---

## 🪣 Step 1: Create an S3 Bucket

- Open AWS Management Console

- Search for S3

- Click Create bucket

- Bucket type:

- Select General purpose

- Bucket name (must be globally unique): kurrebucket711


- Keep remaining settings as default

- Click Create bucket
---

## 📂 Step 2: Upload Files to the Bucket

- Open the bucket: kurrebucket711

- Click Upload

- Click Add files

- Select your file (example: index.html)

- Click Upload

- After upload:

- Click the file to verify it opens correctly
---

## 🌐 Step 3: Enable Static Website Hosting

- Go to Bucket → Properties

- Scroll down to Static website hosting

- Click Edit

- Enable Static website hosting

- Enter: Index document: index.html


- Click Save changes
---

## 🔓 Step 4: Configure Public Access
### Disable Block Public Access

- Go to Permissions

- Open Block public access (bucket settings)

- Click Edit

- Uncheck: Block all public access


- Click Save changes

- Confirm the action
---

## Add Bucket Policy

- Go to Permissions → Bucket policy

- Click Edit

- Paste the policy below
(Replace the bucket name if required)
```js
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::kurrebucket711/*"
    }
  ]
}
```

- Click Save changes
---

## ✅ Step 5: Access the Static Website

- Go to Properties

- Scroll to Static website hosting

- Copy the Bucket website endpoint

- Paste the URL into your browser

### 🎉 Your static website is now live and accessible publicly!
---

## 🔁 Step 6: Enable Bucket Versioning

- Go to Bucket → Properties

- Open Bucket versioning

- Click Edit

- Select Enable

- Click Save changes
---

## 📑 Step 7: Verify Versioning

- Go to Objects

- Enable Show versions

- Initially: Version may appear as null

- Upload the same file (index.html) again

- You will now see: A new Version ID

- Previous versions retained

## ✅ This confirms bucket versioning is working correctly.
---

## 📌 Conclusion
- Application Load Balancer automatically traffic distribute 
- High Availability aur Fault Tolerance m

 
---

  ## 👨‍💻 Author

**Kumlesh Kurre**
💼 IT Support & Network Engineer

⭐ If you find this guide helpful, don’t forget to star ⭐ the GitHub repository!

**Purpose:** AWS Learning & Practice 🚀
