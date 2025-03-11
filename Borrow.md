### **3.1 借阅电子书**
```http
POST /api/borrow
```
**请求体**
```json
{
  "userId": "12345",
  "bookId": "book123"
}
```
**响应**
```json
{
  "message": "Book borrowed successfully",
  "dueDate": "2025-03-20"
}
```

### **3.2 取消借阅**
```http
DELETE /api/borrow/{bookId}
```
**响应**
```json
{
  "message": "Book returned successfully"
}
```
