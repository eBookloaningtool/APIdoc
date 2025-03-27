# 电子书管理


### 获取书籍榜单
```http
GET /api/books/popular?category={category}
```
**响应**
```json
{
    "bookId": ["bookId1", "bookId2"]
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
  "publisher": "Example Publisher",
  "isbn": "978-1234567890",
  "description": "A beginner's guide to JavaScript.",
  "coverUrl": "https://example.com/book-cover.jpg",
  "category": "Programming",
  "availableCopies": 5,
  "totalCopies": 10,
  "price": 5.99
}
```

---

### 搜索电子书
```http
GET /api/books/search?q=javascript
```
**响应**
```json
{
  "code": 200,
  "data": [
    {
      "bookId": "book123",
      "title": "JavaScript Basics",
      "author": "John Doe"
    }
  ]
}
```
