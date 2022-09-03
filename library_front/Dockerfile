# Build linux image and node
FROM ubuntu:20.04
RUN apt update && apt install -y nodejs && apt install -y npm

# Set working dir to /backend
WORKDIR /frontend

# Exposing port 8000
EXPOSE 3000

# Copying all contents in dir to workdir
COPY . .