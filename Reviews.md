# 评论系统

### 添加评论
```http
POST /api/books/addreviews
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
  "commentID": "3fc5393d-9fcd-42b0-9801-bd2532bca309"
}
```

### 获取用户评论
```http
POST /api/users/reviews
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 响应

```json
{
  "comments": ["commentID1", "commentID2"]
}
```

### 获取书籍评论
```http
GET /api/books/{bookId}/reviews
```

#### 响应

```json
{
  "comments": ["commentID1", "commentID2"]
}
```

### 删除评论
```http
POST /api/books/delreviews
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 请求体
```json
{
  "commentID": "3fc5393d-9fcd-42b0-9801-bd2532bca309"
}
```

#### 响应

```json
{
  "state": "success",
}
```