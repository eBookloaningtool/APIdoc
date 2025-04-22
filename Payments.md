# 支付系统

### 充值余额

```http
POST /api/payments/topup
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 请求体
```json
{
  "amount": 100
}
```

#### 响应

```json
{
  "state": "success",
  "paymentId": "paymentUUID",
  "balance": 200
}
```

### 充值历史记录

```http
POST /api/payments/history
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 响应

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