# 评论系统

### 添加评论
```http
POST /api/reviews/add
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 请求体
```json
{
  "bookId": "book123",
  "rating": 5,
  "comment": "This book was amazing!"
}
```

#### 响应

```json
{
  "state": "success",
  "commentId": "3fc5393d-9fcd-42b0-9801-bd2532bca309"
}
```

### 获取用户评论
```http
POST /api/reviews/user
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 响应

```json
{
  "comments": ["commentId1", "commentId2"]
}
```

### 获取书籍评论
```http
GET /api/reviews/book?bookId=bookId1
```

#### 响应

```json
{
  "comments": ["commentId1", "commentId2"]
}
```

### 获取评论内容(用户注销则username为 Inactive user)
```http
GET /api/reviews/content?commentId=3fc5393d-9fcd-42b0-9801-bd2532bca309
```

#### 响应

```json
{
  "state": "success",
  "bookId": "00b599d9-9ff1-4513-ac8f-5d1abaf093a0",
  "uuid": "3a0e3d23-5061-4602-a814-2bbc4447347e",
  "username": "name",
  "rating": 5,
  "content": "This book was amazing!",
  "createDate": "2025-04-03"
}
```

### 删除评论
```http
POST /api/reviews/delete
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 请求体
```json
{
  "commentId": "3fc5393d-9fcd-42b0-9801-bd2532bca309"
}
```

#### 响应

```json
{
  "state": "success"
}
```