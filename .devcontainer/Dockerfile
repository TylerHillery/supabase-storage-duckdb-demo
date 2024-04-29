ARG PYTHON_VERSION=3.11

FROM python:${PYTHON_VERSION}
 
RUN apt-get update && \
    apt-get install -y \
    git \
    gcc \
    build-essential \
    libffi-dev \
    libssl-dev \
    curl \
    unzip \
    software-properties-common \
    python3-dev \
    libpq-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

ADD --chmod=755 https://astral.sh/uv/install.sh /install.sh
RUN /install.sh && rm /install.sh