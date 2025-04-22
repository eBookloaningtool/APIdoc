# 电子书管理


### 获取书籍榜单
```http
GET /api/books/popular
```
**响应**
```json
{
    "bookId": ["bookId1", "bookId2", "bookId3", "bookId4", "bookId5"]
}
```


### 获取电子书详情
```http
GET /api/books/{bookId}
```
**响应**
```json
{
  "bookId": "book123",
  "title": "JavaScript Basics",
  "author": "John Doe",
  "description": "A beginner's guide to JavaScript.",
  "coverUrl": "https://example.com/book-cover.jpg",
  "category": "Programming",
  "availableCopies": 5,
  "totalCopies": 10,
  "price": 5.99,
  "rating": 5.0,
  "borrowTimes": 0
}
```

### 获取电子书内容
```http
POST /api/books/content
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

**响应**
```json
{
  "bookId": "book123",
  "contentURL": "https://example.com/book123.html"
}
```

### 搜索电子书
```http
GET /api/books/search?title=xxx&author=xxx&category=xxx
```
`title`、`author`、`category` **至少存在一个**。

**响应**
```json
{
  "state": "success",
  "bookId": ["bookId1", "bookId2", "bookId3", "bookId4", "bookId5"]
}
```
