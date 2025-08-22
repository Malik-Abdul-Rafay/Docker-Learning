# 🐳 Docker Quick Reference (Kali Linux)

Ye notes **Kali Linux** par Docker ke liye quick reference guide hain.  
Har command alag code block me hai taake GitHub par easy copy ho. Har command ke sath comment bhi hai jo explain karta hai ke ye command kya karti hai.  

---

## 📝 Basic Commands

```bash
docker --version        # Check installed Docker version
```

```bash
docker ps               # List currently running containers
```

```bash
docker ps -a            # List all containers, running and stopped
```

```bash
docker images           # List all downloaded Docker images
```

```bash
docker start <container_id> or <container_name>   # Start a running container by its ID or name
```
```bash
docker stop <container_id> or <container_name>   # Stop a running container by its ID or name
```

```bash
docker rm <container_id> or <container_name>   # Remove a container by its ID or name
```

```bash
docker rmi <image_id> or <image_name>        # Remove a Docker image by its ID or name
```

```bash
docker system prune -a       # Remove all unused containers, networks, images, and build cache
```

---

## 📦 Containers

```bash
docker run ubuntu    # Create & run a new container
```
➡️ Run an **Ubuntu container** but it will exit immediately because no process is running.

```bash
docker run -it ubuntu bash
```
➡️ Run container in background

```bash
docker run -d ubuntu
```
➡️ Run an **interactive Ubuntu container** and open a bash shell to run commands inside.

```bash
docker run --name myubuntu ubuntu
```
➡️ Port Blinding in **Container**.

```bash
docker run -p<host_port>:<conatiner_port> <image_name>
```


---

## ✅ Recommendations

- **For exploration:** `docker run -it ubuntu bash`
- **For background usage:** `docker run -dit --name myubuntu ubuntu`


---

## 🖼️ Images

```bash
docker pull ubuntu              # Download Ubuntu image from Docker Hub
```

```bash
docker build -t myapp .         # Build an image from a Dockerfile in current directory and tag it as 'myapp'
```

```bash
docker tag myapp myapp:v1       # Tag an existing image with a version or new name
```

---

## 💾 Volumes

```bash
docker volume create mydata        # Create a new Docker volume named 'mydata'
```

```bash
docker run -v mydata:/app ubuntu   # Mount volume 'mydata' inside a container at /app
```

---

## 🌐 Networking

```bash
docker network ls                  # List all Docker networks
```

```bash
docker network create mynetwork    # Create a new Docker network named 'mynetwork'
```

```bash
docker run --network=mynetwork ubuntu  # Run a container connected to a specific network
```

---

## 🛠️ Docker Compose (Optional)

```bash
docker-compose --version       # Check installed Docker Compose version
```

```bash
docker-compose up              # Start services defined in docker-compose.yml
```

```bash
docker-compose down            # Stop and remove services defined in docker-compose.yml
```

---

## 💡 Useful Tips

```bash
sudo usermod -aG docker $USER  # Add current user to docker group to run Docker without sudo
```

```bash
newgrp docker                  # Apply the new group membership without logging out
```

```bash
docker stats                   # Show real-time resource usage of running containers
```

---

## 🛠️ Troubleshooting

```bash
sudo usermod -aG docker $USER
newgrp docker                  # Fix 'permission denied while connecting to Docker daemon'
```

```bash
sudo systemctl start docker
sudo systemctl enable docker   # Ensure Docker service is running on system startup
```

---

## 📚 Resources
- [Docker Official Docs](https://docs.docker.com/)
- [Play with Docker](https://labs.play-with-docker.com/)
- [Docker Hub](https://hub.docker.com/)

---

✨ Ye **quick reference guide with comments** hai for Docker commands on Kali Linux.
