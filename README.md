# Lab 01 – Spring Boot Microservices

```
lab01-microservices/
├── product-service/   (port 8081)
├── order-service/     (port 8082)
└── frontend/index.html
```

## Chạy (cần JDK 17+ và Maven)
Terminal 1: `cd product-service && mvn spring-boot:run`
Terminal 2: `cd order-service && mvn spring-boot:run`
Frontend: chuột phải `frontend/index.html` → **Open with Live Server**.

## Kiểm thử
- http://localhost:8081/api/products
- http://localhost:8081/api/products/1  → `{"id":1,"name":"Mouse","price":150000}`
- http://localhost:8082/api/orders
- http://localhost:8082/api/orders/product/1  → cùng JSON như trên
- http://localhost:8082/api/orders/product/9999 → 404

## Git / GitHub
```
git init
git add .
git commit -m "Lab01: Create Product Service and Order Service"
git branch -M main
git remote add origin https://github.com/USERNAME/lab01-microservices.git
git push -u origin main
```
Sau khi thêm frontend:
```
git status
git add .
git commit -m "Lab01 - Add Frontend and REST API integration"
git push origin main
```
