# 借阅系统

### **3.1 借阅电子书**
```http
POST /api/borrow
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 请求体
```json
{
  "bookId": "book123"
}
```
#### 响应
```json
{
  "state": "success",
  "dueDate": "2025-03-20"
}
```

### 取消借阅
```http
POST /api/return/
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 请求体

```json
{
  "bookId": "book123"
}
```

#### 响应

```json
{
  "state": "success"
}
```
