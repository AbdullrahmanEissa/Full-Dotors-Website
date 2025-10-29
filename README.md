# 🩺 Dr. Maged Elshenawy – Official Landing Page

Welcome to the **official landing page** for **Dr. Maged Elshenawy**, Consultant of **Cardiology, Internal Medicine, Obesity, Diabetes, and Nutrition**.  
This site was designed with a **modern and elegant aesthetic**, reflecting professionalism, trust, and care.

The website provides patients with:
- A simple way to **register their information**
- Direct **contact via WhatsApp**
- The **clinic location** on Google Maps
- Clear details about the doctor’s expertise and medical services

---

## 🧱 Project Structure

```

project-root/
├── Dockerfile
├── README.md
└── site/
├── index.html
├── css/
├── images/
└── js/

````

- The `/site` directory contains all static files: HTML, CSS, JavaScript, and images.
- The Dockerfile creates a lightweight Nginx container to serve those files efficiently.

---

## 🐳 Dockerfile Overview

The website is packaged using **Nginx** on top of a secure, minimal **Alpine Linux** image.  
This ensures fast load times, tiny image size, and stability in production environments.

```dockerfile
# Dockerfile for Dr. Maged Elshenawy Landing Page
# Production-ready build using Nginx for EC2, Docker Hub, or any VPS hosting

FROM nginx:alpine

WORKDIR /usr/share/nginx/html
COPY ./site .

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
````

---

## 🚀 How to Deploy

### Option 1: Deploy on AWS EC2 (Recommended for Production)

1. **SSH into your EC2 Instance**

   ```bash
   ssh -i "your-key.pem" ec2-user@your-ec2-public-ip
   ```

2. **Install Docker**

   ```bash
   sudo apt update
   sudo apt install -y docker.io
   sudo systemctl start docker
   sudo systemctl enable docker
   ```

3. **Clone the Project**

   ```bash
   git clone https://github.com/yourusername/elshenawy-landing.git
   cd elshenawy-landing
   ```

4. **Build the Docker Image**

   ```bash
   sudo docker build -t elshenawy-landing .
   ```

5. **Run the Container**

   ```bash
   sudo docker run -d --name elshenawy -p 80:80 elshenawy-landing
   ```

6. **Visit your site**

   ```
   http://your-ec2-public-ip
   ```

   You should see the landing page live.

---

### Option 2: Deploy on GitHub Pages (Simple and Free)

GitHub Pages automatically serves static files — no server or Docker required.

1. Push your `site` folder to a new GitHub repository.

2. Rename the folder to match this structure:

   ```
   repository/
   ├── index.html
   ├── css/
   ├── js/
   ├── images/
   ```

3. Go to **Settings → Pages** and choose:

   * Source: `main` branch
   * Folder: `/ (root)`

4. GitHub Pages will deploy your site automatically at:

   ```
   https://yourusername.github.io/repository-name/
   ```

5. You can also connect a custom domain like:

   ```
   www.drmagedelshenawy.com
   ```

---

## 💬 Contact and Integration

* **WhatsApp:** [+20 10 6242 1416](https://wa.me/201062421416)
* **Google Maps:** [View Clinic Location](https://maps.app.goo.gl/9Q3WRE96K2iqrNfeA)
* **Facebook:** [Dr. Maged Elshenawy Page](https://www.facebook.com/profile.php?id=100085422890114)

All patient submissions through the contact form will be routed to WhatsApp for immediate communication.

---

## 🛡️ Why Nginx?

Nginx is a high-performance web server ideal for static sites because it:

* Uses minimal memory and CPU
* Handles thousands of connections efficiently
* Provides built-in caching and compression
* Is production-grade and battle-tested

---

## 🧰 Useful Commands

**Build the image**

```bash
docker build -t elshenawy-landing .
```

**Run the container**

```bash
docker run -d -p 8080:80 elshenawy-landing
```

**Stop and remove container**

```bash
docker stop elshenawy && docker rm elshenawy
```

**Remove image**

```bash
docker rmi elshenawy-landing
```

---

## 🌍 Future Enhancements

* SSL/HTTPS support (via Let’s Encrypt or AWS Certificate Manager)
* Contact form database integration
* Google Analytics tracking
* Multi-language support (Arabic/English)

---

## 🧑‍⚕️ About Dr. Maged Elshenawy

**Dr. Maged Elshenawy** is a consultant specializing in:

* Cardiology and Vascular Medicine
* Internal Medicine
* Obesity and Diabetes Management
* Clinical Nutrition

His practice combines medical expertise with a holistic, patient-centered approach to health.

---

## 🪶 License

© 2025 Dr. Maged Elshenawy.
All rights reserved.

Developed with ❤️ for patient care and medical excellence.

---

```

---
