# Host Your Resume on AWS EC2 with a CI/CD Setup Using GitHub Actions
This project includes a full CI/CD pipeline using GitHub Actions and AWS EC2.

Every time changes are pushed to the main branch:
1. The workflow is triggered automatically.
2. GitHub Actions checks out the code.
3. It securely connects to an AWS EC2 instance via SSH.
4. The server pulls the latest code EC2.
5. Moves files to root folder and restarts server (Nginx in this case).

The Resume site is live on http://ec2-54-172-144-183.compute-1.amazonaws.com/ (Instance currently not running)

📂 Workflow File
.github/workflows/github-actions-ec2.yml

🔐 Secrets Used
EC2_HOST: Public IP of the EC2 instance
USERNAME: Ubuntu
EC2_SSH_KEY: Private key for SSH access to the server

🛠 Tools Used
GitHub Actions
Docker
AWS EC2 (Ubuntu)
SSH
Bash scripting
