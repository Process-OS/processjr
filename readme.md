# Documentation Deployment

This repository supports running the documentation either inside a Docker container (recommended) or locally using Python.

---

## Option A: Running with Docker (Containerized)

### 1. Build the service
```bash
docker compose build processjr-docs
```

### 2. Start the service
```bash
docker compose up -d processjr-docs
```

### 3. Monitor status & logs
```bash
docker compose ps processjr-docs
docker compose logs -f processjr-docs
```

### 4. Stop the container when done
```bash
docker compose down
```

---

## Option B: Running Locally (Without Docker)

To run the documentation locally, you need Python 3.11+ installed.

### 1. Create and Activate Virtual Environment
```bash
# Create a virtual environment in the root directory
python3 -m venv .venv

# Activate it (Mac/Linux)
source .venv/bin/activate

# Activate it (Windows)
.venv\Scripts\activate
```

### 2. Install Dependencies
```bash
pip install mkdocs-material
```

### 3. Run Development Server
Navigate to the documentation directory and start the live-reload server:
```bash
cd documentation
../.venv/bin/mkdocs serve
```
*(The site will be accessible locally at http://127.0.0.1:8000/)*

### 4. Build Static Site
To compile the documentation into static HTML files (saved inside `documentation/site/`):
```bash
cd documentation
../.venv/bin/mkdocs build
```

