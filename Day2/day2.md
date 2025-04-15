# DevOps Training - Day 2 ☁️  
### Working with AWS EC2 and Basic Linux Operations

---

## 🚀 Getting Started with EC2 (Elastic Compute Cloud)

Today, we explored how to create and connect to virtual machines (instances) on AWS using EC2. This is your first step into hands-on cloud infrastructure.

### 🧩 Steps to Launch an EC2 Instance:

1. **Log in to AWS Console**
2. Navigate to **EC2 Dashboard**
3. Click **Launch Instance**
4. Select the following:
   - **OS**: Amazon Linux 2 / Ubuntu (based on need)
   - **Instance Type**: `t2.micro` or `t2.medium`
5. Configure storage and security group
6. Create a **new key pair** or use existing
7. Launch the instance 🚀

---

## 🔐 Connecting to EC2 Instance (Linux-based)

To access your instance:

### On Windows:
- Use **PuTTY**
  - Convert `.pem` to `.ppk` via **PuTTYgen**
  - Enter public IP in **Host Name**
  - Auth → Load your `.ppk` file
  - Click **Open**

### On Linux/Mac:
```bash
chmod 400 your-key.pem
ssh -i "your-key.pem" ec2-user@<public-ip>
