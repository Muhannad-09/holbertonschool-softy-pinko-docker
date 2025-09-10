# Base image
FROM ubuntu:latest

# Update & upgrade, install Python3 and pip
RUN apt-get update && apt-get upgrade -y \
    && apt-get install -y python3 python3-pip \
    && rm -rf /var/lib/apt/lists/*

# Fix potential EXTERNALLY-MANAGED error
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy Flask app into the container
COPY ./api.py /app/api.py

# Default command to run Flask server
CMD ["python3", "/app/api.py"]
