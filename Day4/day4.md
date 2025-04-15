# 🚀 DevOps Training - Day 4  
### Understanding Docker Internals, Environments & Image Deployment

---

## 🔍 Why Docker?

Docker allows us to **containerize applications**, making them portable and efficient. It solves the *"works on my machine"* issue by packaging code along with its dependencies.

---

## 🧱 Key Concepts

### 🧩 Environments in a Software Lifecycle:

1. **Development (Dev)** – Where code is written and tested by developers.
2. **Testing (QA)** – QA engineers validate the application.
3. **UAT (User Acceptance Testing)** – Final approval from stakeholders or clients.
4. **Production (Prod)** – Live deployment, accessible by real users.

---

## 🐳 What is a Container?

A container is a **lightweight runtime** environment for running applications. Unlike virtual machines, containers share the host OS kernel, making them much faster and more efficient.

---

## 🧰 Docker Architecture Components:

| Component         | Purpose                                          |
|------------------|--------------------------------------------------|
| Docker Engine     | The main service that manages containers         |
| Docker Image      | A snapshot containing everything needed to run   |
| Docker Container  | A running instance of an image                   |
| Dockerfile        | Blueprint for building Docker images             |

---

## ⚙️ Dockerfile: Writing Your Own Image Blueprint

Here’s an example of a basic `Dockerfile`:

```Dockerfile
FROM ubuntu
RUN apt update -y && apt install nginx -y
CMD ["nginx", "-g", "daemon off;"]
