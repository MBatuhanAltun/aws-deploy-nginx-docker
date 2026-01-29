# AWS Deploy with Docker + Nginx

Small Python web app (Flask) running in Docker, served by Nginx, deployed on AWS EC2 with GitHub Actions.

## Architecture (simple)
- Flask app runs on port 8080
- Nginx listens on port 80 and forwards to the app
- EC2 runs both containers

## How to run locally
```bash
docker-compose up --build
```

## Health check
```
GET /health
```

## CI/CD
On every push to main, GitHub Actions deploys to EC2 using SSH.

## Summary 
I built a small Flask app, containerized it with Docker, put Nginx in front, and deployed it to AWS EC2. I added CI/CD with GitHub Actions, basic health checks and logs, and set cost and security controls.
