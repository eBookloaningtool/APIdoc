# 认证 & 用户管理

## 1.1 用户注册
```http
POST /api/auth/register
```
**请求体**
```json
{
  "username": "user123",
  "email": "user@example.com",
  "password": "securepassword"
}
```
**响应**
```json
{
  "message": "User registered successfully",
  "UUID": "3a0e3d23-5061-4602-a814-2bbc4447347e"
}
```

## **1.2 用户登录**
```http
POST /api/auth/login
```
**请求体**
```json
{
  "email": "user@example.com",
  "password": "securepassword"
}
```
**响应**
```json
{
  "token": "jwt_token_here",
  "UUID": "3a0e3d23-5061-4602-a814-2bbc4447347e"
}
```

## **1.3 注销登录**
```http
POST /api/auth/logout
```
**请求头**
```
Authorization: Bearer <token>
```
**响应**
```json
{
  "message": "success"
}
```





## **1.4 获取用户信息**
```http
GET /api/users/{userId}
```
**响应**
```json
{
  "UUID": "3a0e3d23-5061-4602-a814-2bbc4447347e",
  "username": "user123",
  "email": "user@example.com",
  "borrowedBooks": ["bookId1", "bookId2"],
  "wishlist": ["bookId3"],
  "transactionHistory": ["order123"]
}
```