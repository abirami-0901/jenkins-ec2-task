# Jenkins CI/CD Pipeline on AWS EC2

Automated CI/CD pipeline: a push to GitHub triggers a Jenkins build 
running on AWS EC2, which executes a shell script and emails the output.

## Tech Stack
AWS EC2, Jenkins, GitHub

## How It Works
1. Code is pushed to this GitHub repo.
2. A GitHub webhook notifies Jenkins.
3. Jenkins auto-triggers a build and runs `hello.sh`.
4. Build output is emailed via Jenkins Email Extension.

## Setup Summary
- EC2 (Ubuntu) instance with Jenkins installed, ports 22/8080 open
- Jenkins job linked to GitHub repo via SCM
- Build trigger: GitHub hook (webhook)
- Post-build action: Email notification (Gmail SMTP)
