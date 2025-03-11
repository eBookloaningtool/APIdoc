### **4.1 添加到愿望清单**
```http
POST /api/wishlist
```
**请求体**
```json
{
  "userId": "12345",
  "bookId": "book123"
}
```

### **4.2 获取愿望清单**
```http
GET /api/wishlist/{userId}
```
