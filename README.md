# 🚀 Production-Grade DevSecOps CI/CD Pipeline

This repository demonstrates how to set up a full DevSecOps CI/CD pipeline using Jenkins, SonarQube, Docker, and security tools like Trivy and OWASP Dependency-Check.

---

## 👤 Author

**Vaibhav Upare**  
📍 Maharashtra, India  
📞 +91-7083460474

**🔗 Social Links:**
- [LinkedIn](http://linkedin.com/in/vaibhav-upare)
- [GitHub](https://github.com/vaibhav0342)
- [Instagram](https://instagram.com/27vaibhav10/?igshid=NGVhN2U2NjQ0Yg==&utm_source=qr)

**📘 Resources:**
- [Hands-On Notes](https://vaibhav0342.github.io/DevOps-Cloud-Solutions)

**📺 YouTube Channels:**
- [DevOps Learn Easy](https://www.youtube.com/c/gestDevOpsLearnEasy)
- [DevOps Digest](https://www.youtube.com/@DevOps_Digest)

---

## ✅ Infrastructure Requirements

| Component        | Specification                 |
|------------------|-------------------------------|
| Build Server     | EC2 - t2.micro, 15 GB storage |
| SonarQube Server | EC2 - t2.medium, 4 GB RAM     |

---

## 🔧 Jenkins Plugin Requirements

- Parameterized Trigger Plugin  
- GitLab Plugin  
- Docker Pipeline  
- Pipeline: AWS Steps  
- SonarQube Scanner  
- Quality Gates Plugin  

---

## 🛠️ Build Server Setup

$ sudo ./setup.sh
📊 SonarQube Setup

$ sudo apt update
$ sudo apt install -y docker.io
$ sudo usermod -a -G docker ubuntu
$ sudo docker run -d --name sonar -p 9000:9000 sonarqube:lts-community

🔐 Jenkins Credentials to Configure
SonarQube Token – Add as Secret Text

DockerHub – Username/Password

GitLab – Username/Password or SSH Key

Build Server SSH – Username + Private Key

🧪 Enable SonarQube Webhook
Navigate to:
SonarQube → Project Settings → Webhooks

Add this webhook:

http://<JENKINS_URL>:8080/sonarqube-webhook/
Feel free to fork, modify, and contribute. Happy DevSecOps 🚀

