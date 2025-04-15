# DevOps Training - Day 3 🔐🛠️  
### IAM Roles, EC2 Practice, Docker Setup & Terraform Introduction

---

## 👥 AWS IAM - Identity and Access Management

IAM lets us manage users and their permissions in AWS.

### 📌 Steps to Create an IAM User:

1. Go to **IAM** from AWS Console.
2. Choose **Users → Add user**.
3. Set username and enable **programmatic access**.
4. Assign to a **group** or attach policies directly.
5. Save the **Access Key ID** and **Secret Access Key** securely.

✅ This user can now be used to run AWS CLI or Terraform commands.

---

## 🖥️ EC2 Launch Refresher

We practiced spinning up instances again and reviewed connecting via SSH.

### Recap:
- Launch Ubuntu EC2 (preferably `t2.medium`)
- Open ports: **22** for SSH, **80/443** for web servers
- Use `.pem` file to SSH into the instance

```bash
ssh -i "your-key.pem" ubuntu@<EC2-PUBLIC-IP>
