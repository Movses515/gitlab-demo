# 🔧 GitLab CI/CD: Static Website Deployment to EC2 via SSH

## 📌 Project Overview

This project demonstrates how to set up a CI/CD pipeline using GitLab and GitLab Runner (via Docker) to automatically deploy a static HTML/CSS/JS website to a remote AWS EC2 server using `scp`.

### Technologies Used:
- **GitLab CE** and **GitLab Runner** (Dockerized, via `docker-compose`)
- **GitLab CI/CD Pipelines**
- **Nginx** to serve the static content
- **AWS EC2** as the target server

---

## 🚀 CI/CD Pipeline Overview

The `.gitlab-ci.yml` file defines two stages:

| Stage    | Description                                            |
|----------|--------------------------------------------------------|
| `build`  | Placeholder step that simply echoes a message          |
| `deploy` | Copies all static site files to the remote server via SSH into `/usr/share/nginx/html` |

> The pipeline is triggered on pushes to the `main` branch.

---

## 🧪 Reviewer Instructions

### ✅ Next Steps to Test the Project:

1. 📬 **Contact the author** on Telegram to turn on the AWS EC2 instance, and I will provide you GitLab credentials:
   > **Telegram:** [@mos_7777](https://t.me/mos_7777)

2. Once the server is up, GitLab and GitLab Runner will start automatically (via existing `docker-compose.yaml`)

3. Pull this repository to your local PC, chnage git remote origin to point to GitLab repository.

5. Push any change to the repository's `main` branch. This will trigger the pipeline:
   - Stage 1: `build` — outputs a simple message, because it is simple static website, no need to be built
   - Stage 2: `deploy` — uploads files to `/usr/share/nginx/html` on the server

6. After deployment, open the website in your browser:
   ```
   http://34.235.192.193
   ```

---

## 📁 Project Structure

```
.
├── index.html
├── styles.css
├── js/
│   └── script.js
├── .gitlab-ci.yml
├── docker-compose.yml
└── README.md
```

---

## 👨‍💻 Author

Developed by Movses Martirosyan  
[@mos_7777 on Telegram](https://t.me/mos_7777)
