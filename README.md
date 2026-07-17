# Simple Container Lab

A beginner-friendly Docker project that demonstrates how to containerize a simple Node.js application using Docker. This project is designed to help learners understand the basic workflow of creating, building, running, and version-controlling a containerized application.

## 📖 Introduction

Containers make it easy to package an application together with all of its dependencies, ensuring that it runs consistently across different environments.

In this lab, you will:

- Create a simple Node.js application.
- Write a Dockerfile to define the container image.
- Build a Docker image.
- Run the application inside a Docker container.
- Initialize a Git repository.
- Push the project to GitHub.

---

## 📂 Project Structure

```
simple-container-lab/
│
├── app.js
├── Dockerfile
└── README.md
```

---

## 🛠 Prerequisites

Before starting, ensure you have the following installed:

- Git
- Docker Desktop (Windows/macOS) or Docker Engine (Linux)
- Node.js (optional for local testing)
- GitHub account

Verify your installations:

```bash
docker --version
git --version
```

---

## 🚀 Step 1: Create the Project Directory

Create a new folder and navigate into it.

```bash
mkdir -p ~/container-lab
cd ~/container-lab
```

---

## 🚀 Step 2: Create the Node.js Application

Create the application file.

```bash
touch app.js
```

Add the following code:

```javascript
console.log("Hello, DevOps!");
```

Or use:

```bash
echo 'console.log("Hello, DevOps!");' > app.js
```

---

## 🚀 Step 3: Create the Dockerfile

Create a Dockerfile.

```bash
touch Dockerfile
```

Add the following content:

```Dockerfile
FROM node:18-alpine

COPY app.js .

CMD ["node","app.js"]
```

Or create it using:

```bash
echo -e 'FROM node:18-alpine\nCOPY app.js .\nCMD ["node","app.js"]' > Dockerfile
```

---

## 🚀 Step 4: Build the Docker Image

Build the Docker image.

```bash
docker build -t simple-container-lab:1.0 .
```

Explanation:

- `docker build` builds the image.
- `-t` assigns a name and version tag.
- `.` tells Docker to use the current directory as the build context.

---

## 🚀 Step 5: Run the Container

Run the Docker container.

```bash
docker run --rm simple-container-lab:1.0
```

Expected output:

```
Hello, DevOps!
```

The `--rm` flag automatically removes the container after it exits.

---

## 🚀 Step 6: Initialize Git

Initialize the Git repository.

```bash
git init
```

---

## 🚀 Step 7: Stage the Files

```bash
git add .
```

---

## 🚀 Step 8: Commit the Project

```bash
git commit -m "feat: first container"
```

---

## 🚀 Step 9: Create a GitHub Repository

Create a repository named:

```
simple-container-lab
```

Do **not** initialize it with:

- README
- .gitignore
- License

---

## 🚀 Step 10: Connect to GitHub

Replace `YOUR_GITHUB_USERNAME` with your GitHub username.

```bash
GITHUB_USERNAME="YOUR_GITHUB_USERNAME"

git remote add origin https://github.com/${GITHUB_USERNAME}/simple-container-lab.git
```

---

## 🚀 Step 11: Rename the Default Branch

```bash
git branch -M main
```

---

## 🚀 Step 12: Push to GitHub

```bash
git push -u origin main
```

---

## ✅ Verify the Repository

Visit:

```
https://github.com/YOUR_GITHUB_USERNAME/simple-container-lab
```

You should see:

- app.js
- Dockerfile
- README.md

---

## 📌 Key Docker Commands Used

| Command | Description |
|----------|-------------|
| `docker build` | Builds a Docker image |
| `docker run` | Runs a Docker container |
| `--rm` | Removes the container after it stops |

---

## 📚 What I Learned

- Creating a simple Node.js application.
- Writing a Dockerfile.
- Building Docker images.
- Running containers.
- Using Git for version control.
- Publishing projects to GitHub.

---

## 👤 Author

**Ganiyat Adebayo**

GitHub: https://github.com/umuashraf1

---

## 📄 License

This project is open-source and available under the MIT License.
