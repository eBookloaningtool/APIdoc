# Payment System

### Top Up Balance

```http
POST /api/payments/topup
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Request Body
```json
{
  "amount": 100
}
```

#### Response

```json
{
  "state": "success",
  "paymentId": "paymentUUID",
  "balance": 200
}
```

### Payment History

```http
POST /api/payments/history
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Response

```json
{
  "state": "success",
  "data": [
    {
    "paymentId": "paymentUUID1",
    "date": "2025-04-21",
    "amount": 10
    },
    {
    "paymentId": "paymentUUID2",
    "date": "2025-04-22",
    "amount": 11
    }
  ]
}
```