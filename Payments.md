### **7.1 购买电子书**
```http
POST /api/payments/purchase
```
**请求体**
```json
{
  "userId": "12345",
  "bookId": "book123",
  "paymentMethod": "credit_card"
}
```