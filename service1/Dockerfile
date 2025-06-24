# Start from the official Golang image for building
FROM golang:1.22-alpine AS builder

WORKDIR /app

# Copy the Go source code
COPY main.go .

# Build the Go binary
RUN go build -o service1 main.go

# Use a minimal image for running
FROM alpine:latest

WORKDIR /app

# Copy the binary from the builder stage
COPY --from=builder /app/service1 .

# Expose the service port
EXPOSE 8001

# Run the service
CMD ["./service1"]