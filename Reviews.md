### **5.1 添加评论**
```http
POST /api/books/{bookId}/reviews
```
**请求体**
```json
{
  "userId": "12345",
  "rating": 5,
  "comment": "This book was amazing!"
}
```