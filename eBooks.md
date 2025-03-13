
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


### **2.2 获取电子书详情**
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

### **2.3 搜索电子书**
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
