This project demonstrates a simple microservices architecture using Docker Compose. It consists of two backend services (one in Go and one in Python Flask) and an Nginx reverse proxy that routes traffic based on URL path prefixes.
.
├── docker-compose.yml
├── nginx/
│   ├── nginx.conf
│   └── Dockerfile
├── service_1/        # Go backend
│   ├── main.go
│   └── Dockerfile
├── service_2/        # Python Flask backend
│   ├── app.py
│   └── Dockerfile
└── README.md

