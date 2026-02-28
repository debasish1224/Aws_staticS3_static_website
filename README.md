# AWS S3 Static Website Hosting

## 📌 Project Overview

This project demonstrates hosting a static website using Amazon S3 and deploying it using AWS CLI with IAM-based programmatic access.

The website is publicly accessible via the S3 static website endpoint.

---

## 🏗 Architecture

User → Amazon S3 Bucket → Static Website Endpoint

---

## 🚀 Services Used

- Amazon S3
- IAM (Identity and Access Management)
- AWS CLI
- HTML / CSS

All services are part of Amazon Web Services (AWS).

---

## ⚙️ Implementation Steps

### 1️⃣ Created S3 Bucket
- Configured bucket in `ap-south-1` region
- Disabled block public access (for static hosting)
- Added bucket policy for public read access

### 2️⃣ Enabled Static Website Hosting
- Enabled static hosting in bucket properties
- Set `index.html` as default document

### 3️⃣ Configured IAM User
- Created IAM user with programmatic access
- Attached `AmazonS3FullAccess` policy
- Generated Access Key and Secret Key

### 4️⃣ Installed & Configured AWS CLI

```bash
aws --version
aws configure

5️⃣ Deployed Website Using CLI
aws s3 ls
aws s3 sync . s3://debasish-static-website-2026

🌐 Live Website -> http://debasish-static-website-2026.s3-website.ap-south-1.amazonaws.com/

[AWS CLI Version] -> <img width="496" height="120" alt="aws_configure" src="https://github.com/user-attachments/assets/0ab7b288-82b1-4904-887a-d9791a3ade32" />

[S3 Sync Output] -><img width="1412" height="91" alt="aws_sync" src="https://github.com/user-attachments/assets/fd938293-f523-4c92-8f15-69772cd5d06e" />

[Website Live] -> <img width="1782" height="717" alt="browser" src="https://github.com/user-attachments/assets/445b9ae8-a3fe-492c-bf1f-2a5949e7f239" />
