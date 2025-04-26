# 🌐 S3 Static Website Sample

This repository contains a **simple example** of files to create and test a **static website** hosted on **Amazon S3**.

## 📄 Project Structure

- `index.html` — Main page that displays a "Hello World" message and shows the visitor's IP address dynamically.
- `error.html` — Custom error page displayed when a user navigates to a non-existent page.

## 🚀 Purpose

This project was created as a **sample** to:
- Test S3 static website hosting capabilities.
- Demonstrate basic public access setup for S3 buckets.
- Verify how custom error handling and dynamic content (via JavaScript) can work in a simple static website.

## 🛠 How to Use

1. Create an S3 bucket.
2. Upload `index.html` and `error.html` to your bucket.
3. Configure the bucket for **static website hosting**.
4. Set up public permissions to allow read access.
5. Access your website using the S3 website endpoint URL.

## 📚 Useful Commands (AWS CLI)

```bash
# Create a bucket (example for non-us-east-1 regions)
aws s3api create-bucket --bucket your-bucket-name --region your-region --create-bucket-configuration LocationConstraint=your-region

# Enable static website hosting
aws s3 website s3://your-bucket-name/ --index-document index.html --error-document error.html

# Upload files
aws s3 cp ./ s3://your-bucket-name/ --recursive
