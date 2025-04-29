# Use official Python slim image
FROM python:3.11-slim-bookworm

# Set working directory inside container
WORKDIR /app

# Install system dependencies
RUN apt-get update && apt-get install -y \
    gcc \
    g++ \
    make \
    libffi-dev \
    libatlas-base-dev \
    libjpeg-dev \
    zlib1g-dev \
    && rm -rf /var/lib/apt/lists/*

# Upgrade pip
RUN pip install --upgrade pip

# Install Python libraries directly
RUN pip install --no-cache-dir pandas scikit-learn matplotlib

# Copy all project files into the working directory
COPY . .

# Set the default command to run your app
CMD ["python", "apps.py"]
