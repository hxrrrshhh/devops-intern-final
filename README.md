# 🚀 DevOps Intern Final Project

**Name:** Harsh Sharma  
**Date:** 16-12-2025  

---

## 🌟 Project Overview
This project demonstrates a **complete DevOps workflow** including Git & GitHub setup, Linux scripting, Docker containerization, CI/CD with GitHub Actions, Nomad deployment, and Monitoring setup with Loki. It simulates a realistic DevOps pipeline from development to deployment and monitoring.

---

## 📂 Project Structure
- `hello.py`                  → Python test script  
- `Dockerfile`                → Docker container definition  
- `scripts/sysinfo.sh`        → Linux shell script for system info  
- `.github/workflows/ci.yml`  → GitHub Actions CI workflow  
- `nomad/hello.nomad`         → Nomad job specification  
- `monitoring/loki_setup.txt` → Loki setup instructions  
- `README.md`                 → Project documentation  

---

## 🛠 Step-by-Step Setup & Execution

### Part 0: Basic Requirements (One-Time Setup)
1. Create a **GitHub account** and verify email.  
2. Install **Git** and verify installation.  
3. Install **Python 3.x** and ensure it's added to PATH.  
4. Install **Docker Desktop** and verify installation.  
5. Download and setup **Nomad**, ensure it is accessible system-wide.  
6. Install **VS Code**.

---

### Part 1: Git & GitHub Setup
1. Create a **new repository** (public, with README) on GitHub.  
2. Clone the repository locally.  
3. Create `hello.py` with a simple Python script.  
4. Commit and push changes to GitHub.

---

### Part 2: Linux & Scripting
1. Create a `scripts` directory.  
2. Add `sysinfo.sh` to retrieve system information.  
3. Make the script executable and run it.  
4. Commit and push the script to GitHub.

---

### Part 3: Docker
1. Create a `Dockerfile` for the Python application.  
2. Build a Docker image and run the container to test.  
3. Commit and push the Dockerfile to GitHub.

---

### Part 4: CI/CD with GitHub Actions
1. Create `.github/workflows` directory.  
2. Add a CI workflow file to run the Python script on every push.  
3. Commit and push the workflow to GitHub.  
4. Verify pipeline execution in GitHub Actions tab.

---

### Part 5: Nomad Deployment
1. Create a Nomad job specification file.  
2. Define the job to deploy the Docker container.  
3. Commit and push the Nomad configuration to GitHub.

---

### Part 6: Monitoring with Loki
1. Setup Loki using Docker for log aggregation.  
2. Document steps in `monitoring/loki_setup.txt`.  
3. Commit and push monitoring documentation to GitHub.

---

### Part 7: Running Everything
1. Build and run the Docker container.  
2. Push changes to trigger the CI/CD pipeline.  
3. Deploy the Nomad job.  
4. Start Loki container and monitor logs.

---

## ✅ Final Checklist
- [x] GitHub repository created  
- [x] `hello.py` script  
- [x] `scripts/sysinfo.sh`  
- [x] `Dockerfile`  
- [x] GitHub Actions workflow  
- [x] Nomad job specification  
- [x] Loki setup documentation  

---

✨ **Project Completed Successfully!**
