# 🚀 AutoDeploy: Lightweight CI/CD with Bash, Docker & Kubernetes

AutoDeploy is a lightweight, no-frills CI/CD solution built entirely with Bash scripting. It automates the full deployment workflow — from detecting new commits in a Git repository to building Docker images and updating Kubernetes deployments — without relying on external CI/CD platforms like Jenkins, GitHub Actions, or GitLab CI.

---

## 🧰 Features

- 🔍 Watches a Git repository for new commits
- 🐳 Builds and pushes Docker images automatically
- ☸️ Updates Kubernetes deployments seamlessly
- ⚡ Lightweight and easy to customize
- 🧠 Great for learning core DevOps principles

---

## 📁 Project Structure

```

AutoDeploy-CI-CD/
├── watch\_repo.sh         # Watches the repo for changes
├── build\_and\_push.sh     # Builds & pushes Docker images
├── k8s\_update.sh         # Applies changes to Kubernetes
├── .env                  # Environment variables (Docker registry, repo URL, etc.)
└── README.md             # Project documentation

````

---

## 🔄 How It Works

1. **`watch_repo.sh`**  
   Continuously monitors a Git repository for new commits on a specific branch.

2. **`build_and_push.sh`**  
   Builds a Docker image for the application and pushes it to the configured Docker registry.

3. **`k8s_update.sh`**  
   Triggers a Kubernetes rollout restart for the target deployment to apply the new image.

---

## ⚙️ Setup & Configuration

### 1. Clone the repository

```bash
git clone https://github.com/mark-medhat1/AutoDeploy-CI-CD.git
cd AutoDeploy-CI-CD
````

### 2. Create `.env` file

Create a file named `.env` in the root directory and add the following environment variables:

```env
REPO_URL=https://github.com/your-user/your-repo.git
BRANCH=main
IMAGE_NAME=yourdockerhubusername/yourapp
DEPLOYMENT_NAME=your-k8s-deployment
NAMESPACE=default
```

> Replace these values with your actual Git, Docker, and Kubernetes config.

### 3. Make scripts executable

```bash
chmod +x *.sh
```

### 4. Start the CI/CD pipeline

```bash
./watch_repo.sh
```

> This will start watching for changes and run the full deployment process when a new commit is detected.

---

## 📌 Requirements

* Bash (Linux/macOS)
* Git
* Docker
* Kubernetes CLI (`kubectl`)
* Access to a Docker registry (e.g., Docker Hub)
* Access to a Kubernetes cluster (local or cloud)

---

## 🧪 Example Use Case

AutoDeploy is ideal for:

* 🧪 Learning CI/CD, Docker, and Kubernetes without heavy tools
* 🏗️ Small teams or side projects that need quick deployment pipelines
* 🛠️ Building your own DevOps tools from scratch
* 👨‍💻 Developers who want full control and visibility over automation logic

---

## 🙌 Contributions & Feedback

Pull requests, issues, and suggestions are always welcome!

---

**🔗 GitHub Repository:**
👉 [https://github.com/mark-medhat1/AutoDeploy-CI-CD](https://github.com/mark-medhat1/AutoDeploy-CI-CD)

---

**Built with ❤️ by Mark Medhat**
