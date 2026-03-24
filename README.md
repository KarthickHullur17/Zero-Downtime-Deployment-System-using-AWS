# 🚀 Zero-Downtime Deployment System using AWS

This project demonstrates a **Blue-Green Deployment Architecture** using AWS services to achieve **zero downtime deployments** and **instant rollback capability**.

---

## 🧠 Project Overview

In modern applications, downtime during deployment can cause loss of users and revenue.  
This project solves that by implementing **traffic-based switching** instead of modifying live systems.

---

## 🏗️ Architecture

User → CloudFront → Blue / Green Environment

- **Blue Environment** → Current Live Version  
- **Green Environment** → New Version (Staging)  

Traffic is routed using Amazon CloudFront.

---

## ⚙️ Tech Stack

- AWS S3 (Static Website Hosting)
- AWS CloudFront (CDN)
- IAM (Access Control)

---

## 🔄 How It Works

1. Upload current version to **Blue S3 bucket**
2. Deploy new version to **Green S3 bucket**
3. CloudFront initially routes traffic to **Blue**
4. After testing, switch origin to **Green**
5. Invalidate cache to reflect changes instantly

---

## 🔁 Rollback Mechanism

If the new version fails:
- Switch CloudFront origin back to **Blue**
- Users instantly see the old version

---

## 🔥 Key Features

- Zero Downtime Deployment  
- Instant Traffic Switching  
- Easy Rollback  
- Global Content Delivery  
- High Availability  

---

## 📸 Architecture Diagram

(Add your diagram image here)

---

## 📚 Key Learnings

- Blue-Green Deployment Strategy  
- CDN-based Traffic Routing  
- Cache Invalidation in CloudFront  
- High Availability Design  

---

## 🚀 Future Improvements

- CI/CD Integration (GitHub Actions)  
- Multi-region Disaster Recovery  
- Private S3 with Origin Access Control (OAC)  

---

## 🧑‍💻 Author

Karthick S Hullur
