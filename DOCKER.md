# QR Frontend - Docker Guide

## Docker Setup

This project includes Docker configurations for both **development** and **production** environments.

---

## 🚀 Quick Start

### Production Build

```bash
# Build and run production container
docker-compose up -d

# Access at http://localhost:3001
```

### Development with Hot Reload

```bash
# Build and run development container
docker-compose -f docker-compose.dev.yml up -d

# Access at http://localhost:5173
```

---

## 📦 Docker Files Overview

- **Dockerfile** - Multi-stage production build (React + Vite → Nginx)
- **Dockerfile.dev** - Development build with hot reload
- **nginx.conf** - Nginx configuration for production
- **docker-compose.yml** - Production orchestration
- **docker-compose.dev.yml** - Development orchestration
- **.dockerignore** - Files to exclude from Docker context

---

## 🛠️ Commands

### Production

```bash
# Build the image
docker-compose build

# Start the container
docker-compose up -d

# View logs
docker-compose logs -f frontend

# Stop the container
docker-compose down

# Rebuild and restart
docker-compose up -d --build
```

### Development

```bash
# Build the dev image
docker-compose -f docker-compose.dev.yml build

# Start the dev container
docker-compose -f docker-compose.dev.yml up -d

# View logs
docker-compose -f docker-compose.dev.yml logs -f frontend-dev

# Stop the dev container
docker-compose -f docker-compose.dev.yml down

# Rebuild
docker-compose -f docker-compose.dev.yml up -d --build
```

### Standalone Docker Commands

```bash
# Build production image
docker build -t qr-frontend:latest .

# Run production container
docker run -d -p 3001:80 --name qr-frontend qr-frontend:latest

# Build development image
docker build -f Dockerfile.dev -t qr-frontend:dev .

# Run development container
docker run -d -p 5173:5173 -v $(pwd)/src:/app/src --name qr-frontend-dev qr-frontend:dev
```

---

## 🌐 Ports

- **Production**: `3001` → mapped to container port `80`
- **Development**: `5173` → mapped to container port `5173`

---

## 🔧 Environment Variables

Create a `.env` file in the project root (if needed):

```env
VITE_API_URL=http://localhost:3000
VITE_APP_NAME=QR Microsite Builder
```

---

## 📊 Health Checks

### Production
- Endpoint: `http://localhost:3001/health`
- Nginx health check runs every 30 seconds

### Development
- Vite dev server automatically handles health

---

## 🏗️ Architecture

### Production (Multi-Stage Build)

1. **Stage 1 (Builder)**: 
   - Uses Node.js 18 Alpine
   - Installs dependencies
   - Builds the React app with Vite
   
2. **Stage 2 (Production)**:
   - Uses Nginx Alpine
   - Copies built static files
   - Serves via Nginx on port 80
   - Optimized for performance and size

### Development

- Uses Node.js 18 Alpine
- Mounts source code as volumes
- Hot reload enabled
- Runs Vite dev server

---

## 🔐 Security Features

- **Nginx Security Headers**:
  - X-Frame-Options: SAMEORIGIN
  - X-Content-Type-Options: nosniff
  - X-XSS-Protection: 1; mode=block
  - Referrer-Policy: no-referrer-when-downgrade

- **Gzip Compression**: Enabled for all text and JavaScript files
- **Client Max Body Size**: 20MB

---

## 🚢 Deployment

### Docker Hub

```bash
# Tag the image
docker tag qr-frontend:latest yourusername/qr-frontend:latest

# Push to Docker Hub
docker push yourusername/qr-frontend:latest
```

### AWS ECR

```bash
# Login to ECR
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin YOUR_ECR_URL

# Tag the image
docker tag qr-frontend:latest YOUR_ECR_URL/qr-frontend:latest

# Push to ECR
docker push YOUR_ECR_URL/qr-frontend:latest
```

---

## 🧹 Cleanup

```bash
# Remove all containers and images
docker-compose down --rmi all

# Remove volumes
docker-compose down -v

# Prune unused Docker resources
docker system prune -a
```

---

## 🐛 Troubleshooting

### Container won't start
```bash
# Check logs
docker-compose logs frontend

# Check container status
docker ps -a
```

### Port already in use
```bash
# Change port in docker-compose.yml
ports:
  - "8080:80"  # Use different host port
```

### Permission issues on Linux
```bash
# Fix file permissions
sudo chown -R $USER:$USER .
```

### Hot reload not working in development
```bash
# Ensure volumes are correctly mounted
docker-compose -f docker-compose.dev.yml down
docker-compose -f docker-compose.dev.yml up -d
```

---

## 📝 Notes

- Production build uses **multi-stage Docker** for optimal image size
- Development setup includes **hot reload** via volume mounting
- Nginx is configured to handle **React Router** (SPA routing)
- Health checks ensure container reliability
- Gzip compression reduces bandwidth usage

---

## 🔗 Integration with Backend

To connect with the backend services, update your `.env`:

```env
VITE_API_URL=http://backend:3000
```

Or modify the nginx.conf to add API proxy configuration (commented example included).

---

For more information, see the main [README.md](./README.md).
