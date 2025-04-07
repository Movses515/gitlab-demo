# 🔧 GitLab CI/CD: Static Website Deployment to EC2 via SSH

## 📌 Project Overview

This project demonstrates how to set up a CI/CD pipeline using GitLab and GitLab Runner (via Docker) to automatically deploy a static HTML/CSS/JS website to a remote AWS EC2 server using `scp`.

### Technologies Used:
- **GitLab CE** and **GitLab Runner** (Dockerized)
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
