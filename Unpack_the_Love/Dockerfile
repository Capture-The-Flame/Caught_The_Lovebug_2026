# Use Ubuntu as base
FROM ubuntu:24.04

# Install Python, vim, pip, and virtualenv
RUN apt-get update && \
    apt-get install -y python3 python3-venv python3-pip vim && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /app

# Copy your script
COPY challenge.py .

# Create virtual environment and install dependencies inside it
RUN python3 -m venv /opt/venv
ENV PATH="/opt/venv/bin:$PATH"
RUN pip install --upgrade pip
RUN pip install cryptography

# Default command: bash shell
CMD ["bash"]
