# DevOps Intern Final Project

# Name: Harsh Sharma

# Date: 16-12-2025

# Project Overview:
This project demonstrates a complete DevOps workflow including Git & GitHub setup, Linux scripting, Docker containerization, CI/CD using GitHub Actions, Nomad deployment, and Monitoring setup with Loki.

# Project Structure:

- hello.py                # Python test script
- Dockerfile              # Docker container definition
- scripts/sysinfo.sh      # Linux shell script for system info
- .github/workflows/ci.yml  # GitHub Actions CI workflow
- nomad/hello.nomad       # Nomad job specification
- monitoring/loki_setup.txt  # Loki setup instructions
- README.md

# Step-by-Step Setup & Execution:

Part 0: Basic Requirements (One-Time Setup)
1. GitHub account: Create an account and verify email.
2. Git: Install from git-scm.com and verify git --version.
3. Python: Install Python 3.x from python.org, tick “Add to PATH”, verify python --version.
4. Docker Desktop: Install from docker.com and verify docker --version.
5. Nomad: Download from hashicorp.com, extract, move nomad.exe to C:\Windows\System32, verify nomad version.
6. VS Code: Install from code.visualstudio.com.

Part 1: Git & GitHub Setup
1. Create a repository: devops-intern-final (public, with README).
2. Clone repository locally: cd Desktop, git clone https://github.com/YOUR_USERNAME/devops-intern-final.git, cd devops-intern-final.
3. Create hello.py: print("Hello, DevOps!")
4. Push changes: git add ., git commit -m "Added hello.py", git push

Part 2: Linux & Scripting
1. mkdir scripts
2. Create scripts/sysinfo.sh:
   #!/bin/bash
   echo "User: $(whoami)"
   echo "Date: $(date)"
   df -h
3. chmod +x scripts/sysinfo.sh, ./scripts/sysinfo.sh
4. Push changes: git add ., git commit -m "Added sysinfo script", git push

Part 3: Docker
1. Create Dockerfile:
   FROM python:3.10-slim
   WORKDIR /app
   COPY hello.py .
   CMD ["python", "hello.py"]
2. docker build -t hello-devops .
3. docker run hello-devops
4. Push Dockerfile

Part 4: CI/CD with GitHub Actions
1. mkdir -p .github/workflows
2. Create .github/workflows/ci.yml:
   name: CI Pipeline
   on: [push]
   jobs:
     run-python:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - name: Run hello.py
           run: python hello.py
3. Push workflow, check GitHub Actions tab

Part 5: Nomad Deployment
1. Create nomad/hello.nomad:
   job "hello-devops" {
     datacenters = ["dc1"]
     type = "service"
     group "hello" {
       task "hello" {
         driver = "docker"
         config {
           image = "hello-devops"
         }
         resources {
           cpu = 100
           memory = 128
         }
       }
     }
   }
2. Push Nomad job

Part 6: Monitoring with Loki
1. Create monitoring/loki_setup.txt:
   Started Loki using Docker:
   docker run -d -p 3100:3100 grafana/loki:2.9.0
   Viewed logs using: docker logs <container_id>
2. Push monitoring documentation

Part 7: Running Everything
- Docker: docker build -t hello-devops ., docker run hello-devops
- CI/CD: Push to GitHub → check Actions tab
- Nomad: nomad job run nomad/hello.nomad
- Monitoring: docker run -d -p 3100:3100 grafana/loki:2.9.0, docker logs <container_id>

# Final Checklist:
- GitHub repo
- hello.py
- scripts/sysinfo.sh
- Dockerfile
- GitHub Actions workflow
- Nomad job
- Loki setup documentation

