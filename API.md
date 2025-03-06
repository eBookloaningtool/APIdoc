# 电子书借阅系统 API 文档

## **概述**
**Base URL**: ``

---

## **🟢 1. 认证 & 用户管理**
### **1.1 用户注册**
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
  "userId": "12345"
}
```

### **1.2 用户登录**
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
  "userId": "12345"
}
```

### **1.3 获取用户信息**
```http
GET /api/users/{userId}
```
**响应**
```json
{
  "userId": "12345",
  "username": "user123",
  "email": "user@example.com",
  "borrowedBooks": ["bookId1", "bookId2"],
  "wishlist": ["bookId3"],
  "transactionHistory": ["order123"]
}
```

---

## **📖 2. 电子书管理**
### **2.1 获取所有书籍**
```http
GET /api/books
```
**响应**
```json
[
  {
    "bookId": "book123",
    "title": "JavaScript Basics",
    "author": "John Doe",
    "category": "Programming",
    "availableCopies": 5,
    "coverUrl": "https://example.com/book-cover.jpg",
    "description": "A beginner's guide to JavaScript.",
    "price": 5.99
  }
]
```

### **2.2 添加新书（管理员）**
```http
POST /api/books
```
**请求体**
```json
{
  "title": "New Book",
  "author": "Jane Doe",
  "category": "Science Fiction",
  "availableCopies": 10,
  "coverUrl": "https://example.com/new-book.jpg",
  "description": "A thrilling sci-fi adventure.",
  "price": 7.99
}
```

---

## **📚 3. 借阅系统**
### **3.1 借阅电子书**
```http
POST /api/borrow
```
**请求体**
```json
{
  "userId": "12345",
  "bookId": "book123"
}
```
**响应**
```json
{
  "message": "Book borrowed successfully",
  "dueDate": "2025-03-20"
}
```

### **3.2 取消借阅**
```http
DELETE /api/borrow/{bookId}
```
**响应**
```json
{
  "message": "Book returned successfully"
}
```

---

## **🌟 4. 愿望清单**
### **4.1 添加到愿望清单**
```http
POST /api/wishlist
```
**请求体**
```json
{
  "userId": "12345",
  "bookId": "book123"
}
```

### **4.2 获取愿望清单**
```http
GET /api/wishlist/{userId}
```

---

## **💬 5. 评论系统**
### **5.1 添加评论**
```http
POST /api/books/{bookId}/reviews
```
**请求体**
```json
{
  "userId": "12345",
  "rating": 5,
  "comment": "This book was amazing!"
}
```

---

## **📩 6. 邮件通知**
### **6.1 发送借阅提醒**
```http
POST /api/notifications/borrow
```
**请求体**
```json
{
  "userId": "12345",
  "bookTitle": "JavaScript Basics",
  "dueDate": "2025-03-20"
}
```

---

## **💰 7. 支付系统**
### **7.1 购买电子书**
```http
POST /api/payments/purchase
```
**请求体**
```json
{
  "userId": "12345",
  "bookId": "book123",
  "paymentMethod": "credit_card"
}
```

---

## **🛠️ 8. 管理员功能**
### **8.1 删除书籍**
```http
DELETE /api/books/{bookId}
```

---

## **📊 9. 数据分析**
### **9.1 获取热门书籍**
```http
GET /api/analytics/popular-books
```

---

## **🎯 10. 书籍推荐系统**
### **10.1 获取推荐书籍**
```http
GET /api/recommendations/{userId}
```

---

## **📢 11. 社交分享**
### **11.1 分享电子书**
```http
POST /api/social/share
```
**请求体**
```json
{
  "userId": "12345",
  "bookId": "book123",
  "platform": "facebook"
}
```
