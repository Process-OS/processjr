FROM python:3.11-alpine

WORKDIR /docs

# Install MkDocs Material and required dependencies
RUN pip install --no-cache-dir mkdocs-material

# Copy the documentation source
COPY . /docs

EXPOSE 8000

# Serve the site on all interfaces so it's accessible outside the container, respecting $PORT on Cloud Run
CMD ["sh", "-c", "mkdocs serve -a 0.0.0.0:${PORT:-8000}"]
