# 支付系统

### 充值余额
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