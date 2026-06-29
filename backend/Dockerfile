FROM python:3.10-slim

WORKDIR /app

# system dependencies (important for numpy, chroma, uvicorn stability)
RUN apt-get update && apt-get install -y \
    build-essential \
    curl \
    && rm -rf /var/lib/apt/lists/*

# install dependencies first (better caching)
COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

# copy application code
COPY app ./app

# runtime directories
RUN mkdir -p /app/uploads /app/chroma_db

# environment
ENV PYTHONPATH=/app
ENV BASE_DIR=/app

EXPOSE 8000

# production-safe uvicorn config
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
