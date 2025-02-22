---
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# **Docker**

Containerization for Developers

---

# **What is Docker?**

- A platform for developing, shipping, and running applications in containers
- Ensures consistency across environments
- Lightweight and portable
- Automates application deployment

---

# **Why Use Docker?**

- Eliminates "works on my machine" issues
- Speeds up development and testing
- Enables microservices architecture
- Efficient resource utilization
- Simplifies CI/CD workflows

---

# **Installing Docker**

- Windows/macOS: [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- Linux:
```sh
sudo apt install docker.io  # Debian/Ubuntu
sudo dnf install docker     # Fedora
```
- Verify installation:
```sh
docker --version
```

---

# **Basic Docker Commands**

- `docker run <image>` → Run a container
- `docker ps` → List running containers
- `docker stop <container>` → Stop a container
- `docker rm <container>` → Remove a container
- `docker images` → List available images

---

# **Docker Images and Containers**

- **Image** → A blueprint for a container
- **Container** → A running instance of an image
- **Dockerfile** → Defines how to build an image
- **Registry** → A place to store images (Docker Hub, private registries)

---

# **Building a Docker Image**

- Create a `Dockerfile`:
```dockerfile
FROM node:16
WORKDIR /app
COPY . .
RUN npm install
CMD ["node", "index.js"]
```
- Build the image:
```sh
docker build -t my-app .
```
- Run the container:
```sh
docker run -p 3000:3000 my-app
```

---

# **Docker Networking**

- **Bridge** → Default network for containers
- **Host** → Uses host’s networking directly
- **None** → No networking
- **Custom networks** → Isolate groups of containers

Example:
```sh
docker network create my-network
docker run --network my-network my-app
```

---

# **Docker Volumes**

- Persist data between container restarts
- Create and mount a volume:
```sh
docker volume create my-data

docker run -v my-data:/app/data my-app
```
- List volumes:
```sh
docker volume ls
```

---

# **Docker Compose**

- Define multi-container applications
- Example `docker-compose.yml`:
```yaml
version: '3'
services:
  web:
    image: nginx
    ports:
      - "80:80"
  app:
    build: .
    depends_on:
      - db
  db:
    image: postgres
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: password
```
- Start services:
```sh
docker-compose up -d
```

---

# **Docker Best Practices**

- Keep images small and optimized
- Use `.dockerignore` to exclude unnecessary files
- Tag images properly
- Clean up unused containers and images:
```sh
docker system prune
```

---

# **Resources**

- [Docker Official Documentation](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/)
- [Play with Docker](https://labs.play-with-docker.com/)

---

# **Thank You!**

Happy Containerizing with Docker! 🚢
