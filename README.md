# 🐳 Containerization of a Two-Tier Application using Docker and Docker Compose

A comprehensive guide to containerizing a two-tier Django web application using Docker and Docker Compose, with integrated security through container image scanning.

## 📋 Project Overview

This project demonstrates the containerization of a Django Notes application with Nginx and MySQL, creating a scalable and secure deployment architecture using Docker. The setup includes proper security measures through container image scanning and follows DevOps best practices.

## 🏗️ Architecture

<img width="909" alt="Screenshot 2025-01-21 at 3 30 24 PM" src="https://github.com/user-attachments/assets/3bdc9275-fb8e-4d11-846b-1d1d4ebbe440" />


### The application uses a two-tier architecture:
- **Frontend/Backend Tier**: Django with Nginx as reverse proxy
- **Database Tier**: MySQL for data persistence

### Components:
- **Nginx**: Reverse proxy for improved security and performance
- **Django**: Python web framework handling application logic
- **MySQL**: Relational database for data storage
- **Docker Compose**: Container orchestration

## 🚀 Features

- **Containerized Architecture**: Complete isolation of application components
- **Docker Compose Integration**: Simplified multi-container management
- **Nginx Reverse Proxy**: Enhanced security and performance
- **Container Image Scanning**: Security vulnerability detection
- **Environment Configuration**: Separate development and production settings
- **Persistent Data Storage**: Volume mapping for database persistence
- **Health Monitoring**: Container health checks for all services

## 🛠️ Technical Stack

- **Web Framework**: Django
- **Web Server**: Nginx
- **Database**: MySQL
- **Containerization**: Docker
- **Container Orchestration**: Docker Compose
- **Security**: Docker Image Scanning
- **Python Version**: 3.9

## 📝 Prerequisites

- Docker Engine
- Docker Compose
- Git
- Python 3.9 (for local development)

## ⚙️ Environment Configuration

Create a `.env` file in the root directory:
```env
MYSQL_ROOT_PASSWORD=root
MYSQL_DATABASE=test_db
DJANGO_SECRET_KEY=your_secret_key
```

## 🚀 Quick Start

1. Clone the repository:
```bash
git clone https://github.com/gajjarvatsall/docker-django-notes-app.git
cd docker-django-notes-app
```

2. Build and start the containers:
```bash
docker-compose up --build -d
```

3. Access the application:
```
http://localhost
```

## 🔍 Container Health Monitoring

The setup includes health checks for all services:

```yaml
healthcheck:
  test: ["CMD", "curl", "-f", "http://localhost:8000/admin"]
  interval: 10s
  timeout: 5s
  retries: 5
```

## 🐛 Troubleshooting

Common issues and solutions:

1. **Database Connection Issues**:
   - Verify environment variables
   - Check database container logs
   - Ensure proper network configuration

2. **Nginx Configuration**:
   - Validate proxy settings
   - Check error logs
   - Verify port mappings

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📝 Blog 

Click Here - [Project Blog](https://www.linkedin.com/posts/gajjarvatsall_django-docker-devops-activity-7274305119041585152-GjhE?utm_source=share&utm_medium=member_desktop)


---
