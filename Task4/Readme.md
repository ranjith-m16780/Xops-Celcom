# XOps Microchallenge #4 – Terraform + Ansible Web App

## Overview
Provision an AWS EC2 instance with Terraform, then configure and deploy a web app using Ansible.

## Prerequisites
- AWS account & credentials
- Terraform installed
- Ansible installed
- SSH key pair for EC2

## Screenshots

<img width="1521" height="624" alt="Screenshot 2025-08-26 141352" src="https://github.com/user-attachments/assets/34620a33-6e37-42a9-ad1b-47791506f1f8" />

<img width="1910" height="986" alt="Screenshot 2025-08-26 141428" src="https://github.com/user-attachments/assets/59be83eb-5268-42e3-9d8c-b39b4dd774a0" />

## Steps


### 1. Provision EC2 with Terraform
```
terraform init
terraform apply
```
Note the public IP output.

### 2. Configure with Ansible
- Edit `inventory` and replace with your EC2 public IP and private key path.
- Run:
```
ansible-playbook -i inventory site.yml
```

### 3. Test Web App
- Open browser: `http://<EC2_PUBLIC_IP>`

### 4. Cleanup
```
terraform destroy
```
Terminate EC2 to avoid charges.

## Screenshots
Below are example screenshots placed in the `screenshots/` folder:

### EC2 WEBPAGE
![EC2 WEBPAGE](screenshots/ec2-webpage.png)

### Ansible Run Output
![Ansible Output](screenshots/ansible-output.png)

## Files
- `main.tf` – Terraform infra
- `inventory` – Ansible host file
- `site.yml` – Ansible playbook
- `index.html` – Web content
- `README.md` – Setup instructions
