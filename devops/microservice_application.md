# Task 2: End-to-End Implementation of a Dockerized Microservices Application with Automated Backups

## Problem Statement

The objective of this task is to build a complete microservices-based application environment that supports reliable deployments, seamless orchestration, and automated database maintenance. The system must utilize Docker for containerization, include Nginx as a reverse proxy for routing, and implement automated backups for disaster recovery.

The solution should be infrastructure-agnostic and ready for production-like environments. This task emphasizes automation, persistence, modularity, and high availability.

---

## Objectives

### 1. Microservices Infrastructure & Dockerization

- Develop independent microservices using a framework of choice (e.g., Python, Node.js, Java).
- Write `Dockerfile` for each service to ensure consistent builds.
- Use `docker-compose.yml` to orchestrate containers for:
  - Microservices
  - Database
  - Nginx (reverse proxy)

---

### 2. Nginx Reverse Proxy Setup

- Deploy Nginx in its own container.
- Configure Nginx to:
  - Route requests to backend microservices.
  - Serve static content directly where applicable.
- Ensure scalable service routing through clear Nginx configuration blocks.

---

### 3. Database Integration & Persistence

- Deploy a relational database (PostgreSQL or MySQL) using Docker.
- Configure microservices to connect via Docker Compose service names and environment variables.
- Enable persistent data storage using Docker volumes:
  - `/var/lib/mysql` or `/var/lib/postgresql/data`
- Ensure secure connections and clear separation of concerns between services and the DB.

---

### 4. Automated Database Backups

- Create a cron job (inside a container or on host) that:
  - Executes `mysqldump` or `pg_dump` on a schedule (e.g., hourly).
  - Compresses the dump using `gzip` or `tar`.
  - Stores the file in a backup directory (e.g., `/backups`).
- Implement pruning logic to delete old backups and manage storage.

---

### 5. Basic CI/CD Integration

- Use Jenkins or GitLab CI to implement a basic pipeline:
  - Build Docker images on each commit.
  - Push images to a container registry.
  - Deploy the application using Docker Compose.
- Keep the CI/CD logic modular and easy to extend.

---

## Deliverables

- Dockerfiles for each microservice.
- A fully functional `docker-compose.yml` file.
- Nginx reverse proxy configuration with route mappings.
- PostgreSQL/MySQL container with data persistence.
- Working cron-based backup container or host job.
- Basic CI/CD setup (optional).
- Directory structure and source code.
- Screenshots or logs demonstrating successful:
  - Microservice operation
  - Proxy routing
  - Backup creation

---

## Approach

1. **Microservices Development:**
   - Build lightweight services with REST APIs or worker logic.
   - Maintain clean separation between services.

2. **Dockerization:**
   - Each microservice must have its own `Dockerfile`.
   - Ensure the base image, ports, and dependencies are well defined.

3. **Service Orchestration:**
   - Use Docker Compose for multi-container setup.
   - Define services, volumes, networks, and environment variables.

4. **Nginx Configuration:**
   - Set up an Nginx container with `nginx.conf` mounting as a volume.
   - Define upstream servers for routing requests.

5. **Database & Backup:**
   - Use Docker volumes for data durability.
   - Run backup scripts in a cron-enabled container or host.
   - Use timestamped filenames and rotate old backups.

6. **CI/CD (Optional):**
   - Automate image builds and deployments on new code commits.
   - Use Jenkinsfile or `.gitlab-ci.yml` as needed.

---

## Documentation Requirements

Include a comprehensive `README.md` with the following:

### Deployment Instructions

- Prerequisites: Docker, Docker Compose
- Setup Steps:
  ```bash
  git clone <repo>
  cd project
  docker-compose up --build
