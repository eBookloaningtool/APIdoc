# Review System

### Add Review
```http
POST /api/reviews/add
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Request Body
```json
{
  "bookId": "book123",
  "rating": 5,
  "comment": "This book was amazing!"
}
```

#### Response

```json
{
  "state": "success",
  "commentId": "3fc5393d-9fcd-42b0-9801-bd2532bca309"
}
```

### Get User Reviews
```http
POST /api/reviews/user
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Response

```json
{
  "comments": ["commentId1", "commentId2"]
}
```

### Get Book Reviews
```http
GET /api/reviews/book?bookId=bookId1
```

#### Response

```json
{
  "comments": ["commentId1", "commentId2"]
}
```

### Get Review Content (username will be "Inactive user" if the user account is deleted)
```http
GET /api/reviews/content?commentId=3fc5393d-9fcd-42b0-9801-bd2532bca309
```

#### Response

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

### Delete Review
```http
POST /api/reviews/delete
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Request Body
```json
{
  "commentId": "3fc5393d-9fcd-42b0-9801-bd2532bca309"
}
```

#### Response

```json
{
  "state": "success"
}
```