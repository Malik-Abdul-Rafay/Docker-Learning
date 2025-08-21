# 🐳 Docker Learning Notes (Kali Linux)

Ye notes maine **Kali Linux** par Docker seekhte waqt banaye hain. Isme installation, basic commands, containers, images, volumes, networking, docker-compose aur troubleshooting sab ek hi page par hain.  

---

## ⚙️ Installation on Kali Linux
```bash
sudo apt update && sudo apt upgrade -y       # System update
sudo apt install docker.io -y                # Install Docker
sudo systemctl enable docker --now           # Enable & Start service
sudo systemctl status docker                 # Check service status
docker --version                             # Verify version
docker run hello-world                       # Test installation
```

---

## 📝 Basic Commands
```bash
docker ps              # Running containers
docker ps -a           # All containers (running + stopped)
docker images          # Images list
docker stop <id>       # Stop container
docker rm <id>         # Remove container
docker rmi <id>        # Remove image
docker system prune -a # Clean unused data
```

---

## 📦 Containers
```bash
docker run -it ubuntu bash     # Start ubuntu container with shell
docker exec -it <id> bash      # Enter existing container
docker logs <id>               # Show container logs
docker inspect <id>            # Show detailed info
```

---

## 🖼️ Images
```bash
docker pull ubuntu             # Download ubuntu image
docker build -t myapp .        # Build from Dockerfile
docker tag myapp myapp:v1      # Tag image
```

---

## 💾 Volumes
```bash
docker volume create mydata
docker run -v mydata:/app ubuntu
```

---

## 🌐 Networking
```bash
docker network ls
docker network create mynetwork
docker run --network=mynetwork ubuntu
```

---

## 🛠️ Docker Compose (Optional on Kali)
```bash
sudo apt install docker-compose -y
docker-compose --version
docker-compose up
docker-compose down
```

---

## 💡 Useful Tips
```bash
sudo usermod -aG docker $USER   # Run Docker without sudo
newgrp docker                   # Apply group changes
docker stats                    # Show resource usage
```

---

## 🛠️ Troubleshooting on Kali
```bash
# Fix permission denied
sudo usermod -aG docker $USER
newgrp docker

# Start service if not running
sudo systemctl start docker
sudo systemctl enable docker
```

---

## 📚 Resources
- [Docker Official Docs](https://docs.docker.com/)
- [Play with Docker](https://labs.play-with-docker.com/)
- [Docker Hub](https://hub.docker.com/)

---

✨ Ye ek hi page ka **quick reference guide** hai for Docker on Kali Linux.  
