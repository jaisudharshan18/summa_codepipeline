# 🚀 CI/CD Learning Project

A beginner-friendly demonstration repository for learning **Continuous Integration (CI)** and **Continuous Deployment (CD)** with YAML and GitHub Actions.

---

## 📁 Project Structure

```text
├── index.html                  # The webpage displaying the Hello World interface
├── ci-pipeline.yml             # Root copy of the CI/CD pipeline configuration
├── .github/
│   └── workflows/
│       └── ci.yml              # The active GitHub Actions workflow file
└── README.md                   # Step-by-step learning guide
```

---

## 🛠️ How this CI/CD Pipeline Works

The pipeline is defined in [`.github/workflows/ci.yml`](file:///c:/Users/jaisudharshan/OneDrive/Desktop/summa/.github/workflows/ci.yml) and performs two main phases:

### 1. **Continuous Integration (CI): `test-and-lint` Job**
- **Triggers**: When code is pushed or a PR is created on branch `main`.
- **Steps**:
  - Checks out the code.
  - Verifies that `index.html` exists.
  - Verifies that the greeting `"Hello"` is present.
  - If any check fails, the pipeline stops and alerts you!

### 2. **Continuous Deployment (CD): `deploy` Job**
- **Triggers**: Runs automatically after `test-and-lint` succeeds on branch `main`.
- **Steps**:
  - Bundles the site artifacts.
  - Deploys `index.html` to live **GitHub Pages** hosting.

---

## 🚀 How to Run It on GitHub

1. **Initialize Git & Push**:
   ```bash
   git init
   git add .
   git commit -m "feat: hello world index and CI/CD yaml pipeline"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo-name>.git
   git push -u origin main
   ```

2. **Enable GitHub Pages**:
   - Go to your repository on GitHub.
   - Click **Settings** ➔ **Pages**.
   - Under **Build and deployment** ➔ **Source**, select **GitHub Actions**.

3. **Watch the Pipeline**:
   - Click on the **Actions** tab in GitHub to watch your pipeline execute live!
