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
  "balance": 100
}
```