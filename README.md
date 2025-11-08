# Pocket-Base

Pocket-Base is a lightweight, containerized base setup for rapid deployment and environment management.  
It provides a ready-to-use Docker configuration, structured folders for data, hooks, and migrations — helping you bootstrap projects quickly.

---

## 🧰 Features
- 🔹 Dockerized environment (ready to run)
- 🔹 Pre-configured folder structure:
    - `pb_data/` – persistent data
    - `pb_migrations/` – database / schema migrations
    - `pb_hooks/` – custom scripts & lifecycle hooks
- 🔹 GitHub Actions for CI/CD under `.github/workflows/`
- 🔹 Simple and extensible — suitable for any stack

---

## 🚀 Getting Started

### Prerequisites
- Docker & Docker Compose installed
- Basic knowledge of containers and environment variables

### Installation
```bash
git clone https://github.com/teknolojisirketi/pocket-base.git
cd pocket-base/docker
docker compose up -d

REST API:  http://localhost:8080/api/
pocketbase  | 
└─ Dashboard: http://localhost:8080/_/



# Stop containers
docker compose down

# View logs
docker compose logs -f

# Sh into container
 docker exec -it <POCKETBASE_CONTAINER_NAME> sh

