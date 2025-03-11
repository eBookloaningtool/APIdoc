### **6.1 发送借阅提醒**
```http
POST /api/notifications/borrow
```
**请求体**
```json
{
  "userId": "12345",
  "bookTitle": "JavaScript Basics",
  "dueDate": "2025-03-20"
}
```