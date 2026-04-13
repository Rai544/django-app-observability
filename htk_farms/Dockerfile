FROM python:3.13-slim

WORKDIR /app

# Install system dependencies for pycairo
RUN apt-get update && apt-get install -y \
    libcairo2-dev \
    pkg-config \
    python3-dev \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# Copy requirements
COPY requirements.txt .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy project
COPY . .

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
