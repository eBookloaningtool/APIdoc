# E-Book Management

### Get Popular Books (bookId sorted by borrowing count in descending order)
```http
GET /api/books/popular
```
**Response**
```json
{
    "state": "success",
    "bookId": ["bookId1", "bookId2", "bookId3", "bookId4", "bookId5"]
}
```

### Get E-Book Details
```http
GET /api/books/get?bookId=book123
```
**Response**
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

### Get E-Book Content
```http
POST /api/books/content
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Request Body

```json
{
  "bookId": "book123"
}
```

**Response**
```json
{
  "bookId": "book123",
  "contentURL": "https://example.com/book123.html"
}
```

### Search E-Books
```http
GET /api/books/search?title=xxx&author=xxx&category=xxx
```
At least one of `title`, `author`, or `category` must be provided.

**Response**
```json
{
  "state": "success",
  "bookId": ["bookId1", "bookId2", "bookId3", "bookId4", "bookId5"]
}
```
