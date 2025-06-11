# 🚀 CI/CD Pipeline with Jenkins, GitHub & Docker on AWS EC2

This project demonstrates a complete CI/CD pipeline setup using **Jenkins**, **Docker**, and **GitHub** on an **AWS EC2 instance**. The pipeline pulls code from GitHub, builds a Docker image, and runs the container with each job execution.

---

## 📌 Tech Stack
- Jenkins
- Docker
- GitHub
- AWS EC2 (Ubuntu)
- Node.js + EJS (ToDo App)

---

## 🔧 Project Setup – Step-by-Step

### ✅ Step 1: Clone the Repository
```bash
git clone https://github.com/your-username/todo-ci-cd-app.git

✅ Step 2: Launch Jenkins & Docker on EC2
Install Jenkins on EC2 and start the service.

Install Docker and add ubuntu user to Docker group.
sudo apt update
sudo apt install jenkins docker.io -y

✅ Step 3: Install GitHub Plugin in Jenkins
Go to Jenkins → Manage Jenkins → Plugin Manager

Install: GitHub plugin, Docker plugin

✅ Step 4: Jenkins Job Setup
Create a new Freestyle Project

In Source Code Management, select Git

Paste your GitHub repo URL

Add credentials using SSH key

✅ Step 5: Generate SSH Key (on EC2)
ssh-keygen

Copy the public key to GitHub → Settings → SSH and GPG Keys

Copy the private key to Jenkins → Credentials → SSH Username with Private Key

✅ Step 6: Configure Build Steps in Jenkins Job
docker build -t todo-app .
docker container run -d --name container-todo-app -p 8000:8000 todo-app

✅ Step 7: Run the Jenkins Job
Hit "Build Now" in Jenkins

Access the app: http://<your-ec2-ip>:8000

🙏 Special Thanks
Shubham Londhe Sir for the continuous guidance and motivation throughout this project journey! 🙌
