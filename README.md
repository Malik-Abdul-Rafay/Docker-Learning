# 🐳 Docker Learning Notes (Kali Linux)

Ye repository meri **Docker Learning Journey on Kali Linux** ka summary hai.  
Isme maine installation steps, basic commands aur notes likhe hain jo Kali Linux par Docker seekhne ke liye helpful hain.  

---

## 📌 Table of Contents
1. [Docker Introduction](#-docker-introduction)
2. [Installation on Kali Linux](#-installation-on-kali-linux)
3. [Basic Commands](#-basic-commands)
4. [Containers](#-containers)
5. [Images](#-images)
6. [Volumes](#-volumes)
7. [Networking](#-networking)
8. [Docker Compose](#-docker-compose)
9. [Useful Tips](#-useful-tips)

---

## 🐳 Docker Introduction
- Docker ek **platform hai jo applications ko containers me run karta hai**.  
- **Container** lightweight isolated environment hai jo VM ki tarah behave karta hai.  
- Ye ensure karta hai ke ek hi app har jagah same tarah run ho.  

---

## ⚙️ Installation on Kali Linux

### Step 1: Update Kali
```bash
sudo apt update && sudo apt upgrade -y
