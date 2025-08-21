# 🐳 Docker Quick Reference (Kali Linux)

Ye notes **Kali Linux** par Docker ke liye quick reference guide hain.  
Har command alag code block me hai taake GitHub par easy copy ho.  

---

## 📝 Basic Commands

```bash
docker --version
```

```bash
docker ps
```

```bash
docker ps -a
```

```bash
docker images
```

```bash
docker stop <container_id>
```

```bash
docker rm <container_id>
```

```bash
docker rmi <image_id>
```

```bash
docker system prune -a
```

---

## 📦 Containers

```bash
docker run -it ubuntu bash
```

```bash
docker exec -it <container_id> bash
```

```bash
docker logs <container_id>
```

```bash
docker inspect <container_id>
```

---

## 🖼️ Images

```bash
docker pull ubuntu
```

```bash
docker build -t myapp .
```

```bash
docker tag myapp myapp:v1
```

---

## 💾 Volumes

```bash
docker volume create mydata
```

```bash
docker run -v mydata:/app ubuntu
```

---

## 🌐 Networking

```bash
docker network ls
```

```bash
docker network create mynetwork
```

```bash
docker run --network=mynetwork ubuntu
```

---

## 🛠️ Docker Compose (Optional)

```bash
docker-compose --version
```

```bash
docker-compose up
```

```bash
docker-compose down
```

---

## 💡 Useful Tips

```bash
sudo usermod -aG docker $USER
```

```bash
newgrp docker
```

```bash
docker stats
```

---

## 🛠️ Troubleshooting

```bash
sudo usermod -aG docker $USER
newgrp docker
```

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

---

## 📚 Resources
- [Docker Official Docs](https://docs.docker.com/)
- [Play with Docker](https://labs.play-with-docker.com/)
- [Docker Hub](https://hub.docker.com/)

---

✨ Ye **quick reference guide** hai for Docker commands on Kali Linux.
