# Jenkins CI/CD Pipeline

## Overview

This project demonstrates the fundamentals of Continuous Integration (CI) using Jenkins. It contains a simple Node.js application along with a Jenkins pipeline that automates the build process.

The purpose of this project is to understand how Jenkins can automatically fetch source code from GitHub, install project dependencies, run the application, and provide build results without requiring manual execution.

The application itself is intentionally simple so that the focus remains on learning the CI/CD workflow rather than developing a complex application.

---

# Technologies Used

- Jenkins
- Node.js
- Git
- GitHub
- npm
- Groovy (Jenkinsfile)

---

# Project Structure

```
jenkins-cicd-pipeline/

├── app.js
├── package.json
├── Jenkinsfile
├── README.md
└── .gitignore
```

---

# How the Project Works

The project follows a basic Continuous Integration workflow.

1. The source code is stored in a GitHub repository.
2. Jenkins accesses the repository and downloads the latest code.
3. Jenkins installs the project dependencies using npm.
4. Jenkins runs the Node.js application.
5. Jenkins displays the build result in its console output.

### Workflow

```
GitHub Repository
        │
        ▼
Jenkins Pipeline
        │
        ▼
Checkout Source Code
        │
        ▼
Install Dependencies
        │
        ▼
Run Node.js Application
        │
        ▼
Build Successful
```

---

# Jenkins Pipeline Stages

The pipeline contains the following stages:

### Checkout

Downloads the latest version of the project from the GitHub repository.

### Install Dependencies

Runs:

```bash
npm install
```

to install the required Node.js packages.

### Run Application

Runs:

```bash
node app.js
```

The application prints:

```
Hello from Jenkins!
```

to the Jenkins console.

### Build Complete

Displays a success message after the pipeline finishes executing.

---

# Prerequisites

Before running this project, make sure the following software is installed:

- Java (JDK 17 or later)
- Jenkins
- Node.js
- Git

---

# Installation

Clone the repository.

```bash
git clone https://github.com/yourusername/jenkins-cicd-pipeline.git
```

Move into the project folder.

```bash
cd jenkins-cicd-pipeline
```

Install dependencies.

```bash
npm install
```

---

# Running the Application Locally

Run the application using:

```bash
npm start
```

Expected output:

```
Hello from Jenkins!
```

---

# Running the Jenkins Pipeline

1. Install Jenkins.
2. Create a new Pipeline project.
3. Connect Jenkins to this GitHub repository.
4. Select **Pipeline script from SCM**.
5. Choose **Git** as the SCM.
6. Provide the repository URL.
7. Save the pipeline configuration.
8. Click **Build Now**.

If all stages complete successfully, Jenkins will display:

```
Finished: SUCCESS
```

---

# Jenkinsfile

The project includes a Jenkinsfile that defines the pipeline stages used to automate the build process.

Pipeline stages include:

- Checkout
- Install Dependencies
- Run Application
- Build Complete

---

# What I Learned

Working on this project helped me understand:

- The basics of Continuous Integration (CI)
- Creating Jenkins pipelines
- Writing a Jenkinsfile
- Connecting Jenkins with GitHub
- Automating project builds
- Installing project dependencies using npm
- Executing Node.js applications through Jenkins
- Reading Jenkins console output and build results

---

# Future Improvements

Possible enhancements include:

- Automatic builds triggered by GitHub webhooks
- Unit testing as part of the pipeline
- Docker image creation
- Automated deployment after a successful build
- Email notifications for build status

---

# Why I Built This Project

I built this project to learn the fundamentals of Continuous Integration using Jenkins. Instead of focusing on a feature-rich application, I wanted to understand how build automation works, how Jenkins pipelines are created, and how GitHub repositories can be integrated into an automated workflow. This project gave me practical experience with the basic concepts used in modern DevOps and Site Reliability Engineering practices.

---
