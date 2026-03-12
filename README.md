# MinIO Storage Basic

Simple MinIO S3-Compatible Storage Template

This repository provides a **very simple template to run MinIO locally using Docker Compose**.  
It is intended to be used as a **template repository** for projects that need **S3-compatible object storage** during development.

The goal of this project is **simplicity**: a minimal setup that works out of the box and can be quickly reused in other projects.

---

# Purpose

This repository exists to make it easy to:

- Quickly start a **local S3-compatible storage**
- Use **MinIO with Docker Compose**
- Provide a **simple reusable template repository**
- Keep configuration **clean and minimal**

This is **not a full production setup**.  
It is a **basic template for development environments**.

---

# Features

- Minimal MinIO setup
- Docker Compose template
- Environment variable configuration
- Persistent storage directory
- Ready to be used as a **template repository**

---

# Project Structure

```
├── data
│   └── .gitignore
├── .env.example
├── docker-compose.example.yml
└── .gitignore
````

Description:

- `.env.example` - example environment configuration
- `docker-compose.example.yml` - example Docker Compose file
- `data/` - local object storage directory
- `.gitignore` - ignores runtime files

Runtime files such as `.env` and `docker-compose.yml` are **not committed to the repository**.

---

# Setup

Clone the repository:

```bash
git clone https://github.com/Tiago-Templates/MinIO-Storage-Basic.git
cd MinIO-Storage-Basic
````

Create the runtime files from the templates:

```bash
cp .env.example .env
cp docker-compose.example.yml docker-compose.yml
```

Edit `.env` if necessary.

---

# Run

Start the container:

```bash
docker compose up -d
```

Stop the container:

```bash
docker compose down
```

---

# Access

MinIO Console:

```
http://localhost:9001
```

S3 API:

```
http://localhost:9000
```

Credentials are defined in `.env`.

---

# Example Environment

Example application configuration:

```
STORAGE_ENDPOINT=http://localhost:9000
STORAGE_BUCKET=uploads
STORAGE_REGION=us-east-1
STORAGE_ACCESS_KEY=minioadmin
STORAGE_SECRET_KEY=minioadmin123
STORAGE_FORCE_PATH_STYLE=true
```

---

# When to Use This Template

This repository is useful when you need:

* Local S3 storage for development
* A quick MinIO setup
* A reusable storage template for projects
* A minimal object storage environment

---

# MinIO

MinIO is a high-performance object storage system compatible with the Amazon S3 API.

Website:

[https://min.io](https://min.io)

Documentation:

[https://min.io/docs](https://min.io/docs)

---

# License

MIT
