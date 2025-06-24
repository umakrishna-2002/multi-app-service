This project demonstrates a simple microservices architecture using Docker Compose. It consists of two backend services (one in Go and one in Python Flask) and an Nginx reverse proxy that routes traffic based on URL path prefixes.
Setup Instructions:
- Clone the repository:
   ```
   git clone https://github.com/umakrishna-2002/multi-service-app.git
   cd multi-service-app
   ```
   
![image](https://github.com/user-attachments/assets/fb2c4799-58b9-4f9f-b7fb-913c85a98b20)

The Nginx server handles incoming requests and routes them based on the URL prefix:

/service1 → forwarded to Go backend (service_1)
![image](https://github.com/user-attachments/assets/2edc157a-ef35-4419-a258-aef50facbf78)

/service2 → forwarded to Python backend (service_2)
![image](https://github.com/user-attachments/assets/d942c4bc-b7b2-4193-b7d2-6d6c9dc79ace)

How Routing works?
All the services were accessible via localhost:8080 as the nginx act as reverse proxy and it forwards requests based on the URL path prefix:

/service1/* → forwarded to the Go backend on port 8001

/service2/* → forwarded to the Python Flask backend on port 8002


```
docker-compose up --build
```

To access the services 

```
http://localhost:8080/service1/ping
```
![image](https://github.com/user-attachments/assets/f2f44b62-1f65-4c51-ac2d-59e3fd475905)

```
http://localhost:8080/service1/hello
```

![image](https://github.com/user-attachments/assets/45a030a1-9550-4269-9d2d-f999fe80b35c)


```
http://localhost:8080/service2/ping
```
![image](https://github.com/user-attachments/assets/7048ad6c-1609-40c4-bd1f-6e6e0c1251e1)


```
http://localhost:8080/service2/hello
```
![image](https://github.com/user-attachments/assets/7d5f8fe3-3eae-470f-a5df-cc944572c8a0)


Therefore, Successfully implemented a working Docker-based microservices architecture with reverse proxy routing and unified access via a single port.
