# 🎮 Jalen's Gaming Hub — Static Website on AWS (S3 + CloudFront)

This project is my first full cloud-hosted website deployed on **Amazon S3** and globally distributed using **Amazon CloudFront**.  
It showcases my interests (gaming, IT, cloud, cybersecurity) while demonstrating cloud fundamentals and deployment skills.

---

## 🚀 Project Overview

I built a static gaming-style website and deployed it using:

- **Amazon S3** — for static website hosting  
- **Amazon CloudFront** — for global CDN distribution  
- **Bucket policies & permissions** — to enable public access  
- **Origin configuration & caching** — for performance  
- **Error handling & root object setup** — to avoid 403/404 errors  

This project helped me understand the AWS shared responsibility model, hosting patterns, static site architectures, and CDN behavior.

🌐 **Live Website:**  
👉 https://d3goy56kvdd2ht.cloudfront.net

---

## 🗂️ Architecture Diagram
---

## 🛠️ Technologies Used

- **AWS S3**
- **AWS CloudFront**
- **HTML / CSS**
- **S3 Static Website Hosting**
- **CloudFront Global Edge Distribution**
- **Bucket Policies**
- **CDN Caching Behavior**

---

## 📦 How I Deployed It

### 1️⃣ Created & Uploaded Website Files  
I built a gaming-themed `index.html` file and uploaded it into an S3 bucket configured for static website hosting.

### 2️⃣ Enabled Static Website Hosting  
I enabled S3's website mode, set the index document, and configured a public-read bucket policy to allow the site to load externally.

### 3️⃣ Built a CloudFront Distribution  
- Pointed CloudFront to the **S3 website endpoint**, not the REST endpoint  
- Set **Default Root Object = index.html** so CloudFront knows what to load  
- Enabled **Redirect HTTP to HTTPS** for secure access  
- Tuned caching and origin behaviors for performance  

### 4️⃣ Troubleshooting & Fixes  
During deployment, I solved multiple real-world issues:

- **403 Forbidden**  
  - Missing bucket policy for public read  
  - Fixed by adding correct S3 bucket policy

- **504 Gateway Timeout**  
  - Incorrect origin URL due to a typo  
  - Fixed by correcting the S3 website endpoint

- **Missing Root Object**  
  - CloudFront couldn't find a homepage  
  - Fixed by setting the Default Root Object to `index.html`

These issues strengthened my understanding of CDN behavior and AWS hosting patterns.

### 5️⃣ Verified Deployment  
Once CloudFront finished propagating globally, the site became accessible worldwide via the CloudFront domain.

---

## 📸 Screenshots  
*Add screenshots of your website + AWS console here if you'd like.*

---

## 🎯 What I Learned

- Hosting a static website using AWS S3  
- Understanding CloudFront distributions  
- Difference between REST vs Website S3 endpoints  
- Troubleshooting CloudFront 403, 404, and 504 errors  
- How AWS handles caching, behaviors, and propagation  
- AWS fundamentals around networking, edge locations, and content delivery  

---

## 🔮 Future Improvements

- Add more pages (About, Setup, Clips, Contact)  
- Add a custom domain using Route 53  
- Add JavaScript animations or dynamic content  
- Automate deployment using GitHub Actions  
- Add CI/CD workflows for cloud projects  

---

## 👨🏾‍💻 Author

**Jalen Hardman**  
Aspiring Cloud / IT Professional | Gamer | Builder  

GitHub: *(add your link here)*  
LinkedIn: *(add your link here)*
