# 📝 Daily Goals Tracker

A lightweight browser-based daily goals tracker that persists data using LocalStorage. The application is automatically deployed to an Amazon S3 static website whenever code is pushed to GitHub—implemented using AWS CodePipeline and CodeBuild.

## 🚀 Features

- Goals persist using browser **LocalStorage**
- Fully automated **CI/CD deployment** from GitHub to S3
- Zero backend — pure **static hosting**
- Fast, lightweight, cost-efficient setup

## 🛠️ AWS Services Used

1. **Amazon S3** – Static Website Hosting
2. **AWS CodePipeline** – Orchestrates CI/CD flow
3. **AWS CodeBuild** – Runs build stage
4. **IAM** – Secure access roles between services

## 🏗️ Architecture Overview

```
    Developer       (pushes code to GitHub)
        |
        V
 GitHub Repository  (HTML/CSS/JS source)
        |
        V
 AWS CodePipeline   (monitors GitHub and triggers deployment)
        |
        V
 AWS CodeBuild      (build stage; prepares artifacts using buildspec.yml)
        |
        V
 AWS CodePipeline   (uploads build artifacts to S3 bucket)
        |
        V
 Amazon S3          (Static Website Hosting)
        |
        V
 User's Browser     (loads site and stores goals via LocalStorage)
```

## 📦 Setup Instructions (High-Level)

- Commit & push code to GitHub
- Pipeline automatically triggers
- CodeBuild runs buildspec.yml
- Built files get deployed to S3
- Website available instantly

## 📄 Documentation

Full documentation PDF: [document.pdf](https://github.com/user-attachments/files/23980758/document.pdf)

## 📁 Code Repository

GitHub Repository: [GitHub Link](https://github.com/yokeshbaskaran/daily-goals-cicd-pipeline)

## 🌐 Live Website

![Image](https://github.com/user-attachments/assets/213b8da6-2508-44b1-9ccc-133a12ba70f2)
