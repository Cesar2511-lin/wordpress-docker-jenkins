# WordPress, MySQL, and Jenkins on Docker

Docker Compose configuration to run a local development environment with WordPress, MySQL 8.0, and a Jenkins automation server.

## Services

- `mysql`: Database service (MySQL 8.0) using environment variables from `.env`.
- `wordpress`: WordPress application connected to the MySQL service on port 8080.
- `jenkins`: Jenkins automation server on port 8081.

## Setup

1. Copy `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```
2. Set passwords in `.env`.
3. Start the containers:
   ```bash
   docker compose up -d
   ```

## Security

Do not commit `.env` with actual passwords to source control. The `.gitignore` file is configured to exclude local environment files.
