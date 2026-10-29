# WordPress + MySQL + Jenkins CI/CD on Docker 🐳

A modular, containerized continuous deployment pipeline that provisions a WordPress CMS, dedicated MySQL 8.0 instance, and a Jenkins automation server orchestrated via Docker Compose.

---

## 🏗️ Architecture

```
                      +-------------------+
                      |   Docker Engine   |
                      +---------+---------+
                                |
          +---------------------+---------------------+
          |                     |                     |
+---------v---------+ +---------v---------+ +---------v---------+
|     Jenkins CI    | |    WordPress CMS  | |     MySQL 8.0     |
|   (Automation)    | |     (Port 8080)   | |    (Port 3306)    |
+-------------------+ +-------------------+ +-------------------+
```

## 🚀 Quickstart

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Cesar2511-lin/wordpress-docker-jenkins.git
   cd wordpress-docker-jenkins
   ```

2. **Configure environment variables**:
   ```bash
   cp .env.example .env
   # Update passwords in .env with your credentials
   ```

3. **Deploy services**:
   ```bash
   docker compose up -d
   ```

4. **Access endpoints**:
   - WordPress: `http://localhost:8080`
   - MySQL: `localhost:3306`

---

## 🛡️ Security Best Practices
- Never commit active `.env` files to source control.
- Ensure volume mounts for persistent database storage (`mysql_data`).
- Network isolation across multi-tier service boundaries.
