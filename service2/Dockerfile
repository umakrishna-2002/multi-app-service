# filepath: service2/Dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY app.py .
RUN pip install flask
EXPOSE 8002
CMD ["python", "app.py"]