# Dockerized Web App Deployment on AWS EC2 🚀

A simple Flask-based web app that is Dockerized and deployed on an AWS EC2 instance with basic automation using cloud-init and shell scripts.

---

## 📁 Repository Contents

- `flash-app`
   - `app.py`: Flask application
   - `Dockerfile`: Docker setup for the app
- `docs`: Folder containing a PDF file with output screenshots for the assignment
- `deploy.sh`: Shell script to automate setup on EC2
- `README.md`: Documentation (you are here)

---

## 🌐 Live Demo

Once deployed, the app runs on:

```bash
http://<your-ec2-public-ip>:5000
```

🚧 Setup Instructions

🔹 1. Clone the Repo
```
git clone https://github.com/your-username/dockerized-webapp-aws-deploy.git
cd dockerized-webapp-aws-deploy
```

🔹 2. Run App Locally with Docker
```
docker build -t flask-app .
docker run -p 5000:5000 flask-app
```


Visit: http://localhost:5000

🔹 3. Launch and Configure EC2

- Launch a t2.micro EC2 instance

- OS: Amazon Linux 2 or Ubuntu

- Open ports: 22, 5000 in the security group

- SSH into EC2:
```
ssh -i your-key.pem ec2-user@your-ec2-ip
```

- Install Docker and run the app:
```
sudo yum update -y
sudo yum install docker git -y
sudo service docker start
sudo usermod -aG docker ec2-user
exit
# Reconnect SSH
git clone https://github.com/your-username/dockerized-webapp-aws-deploy.git
cd dockerized-webapp-aws-deploy
docker build -t flask-app .
docker run -p 5000:5000 flask-app
```

## 📸 Screenshots

All required screenshots are available in the following PDF:

📄 [View Screenshot PDF](docs/DevOps-Intern-Assignment_Screenshots_Jagruti-Chaudhari.pdf)


Contents:

- App running locally in Docker

- EC2 dashboard

- SSH terminal session

- App running via public IP


✍️ Author

Jagruti Chaudhari  
DevOps Intern Assignment — 2025  
GitHub: @jagruti768  

📜 License

This project is open-source and free to use.
