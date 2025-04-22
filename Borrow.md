# 借阅系统

### 借阅电子书
```http
POST /api/borrow/borrow
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

- **购买成功：**

```json
{
  "state": "success",
  "dueDate": "2025-03-20",
  "balance": 50.00
}
```

- **余额不足：**

```json
{
  "state": "insufficient balance",
  "newPayment": 2.5
}
```

### 取消借阅
```http
POST /api/borrow/return/
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

### 续借
```http
POST /api/borrow/renew/
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

- **续订成功：**

```json
{
  "state": "success",
  "newDueDate": "2025-04-03"
}
```

- **余额不足：**

```json
{
  "state": "insufficient balance",
  "newPayment": 2.5
}
```