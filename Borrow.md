# 借阅系统

### **3.1 借阅电子书**
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
```json
{
  "state": "success",
  "dueDate": "2025-03-20"
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

- **续订失败（例如续订次数超限或图书被预订）：**

```json
{
  "state": "reach limit"
}
