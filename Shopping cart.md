# 购物车 API

## 1. 添加书籍到购物车

```http
POST /api/cart/add
```

### 请求头
```http
Authorization: Bearer <JWT_TOKEN>
```

### 请求体
```json
{
  "bookId": "book123",
  "quantity": 1
}
```

### 响应
```json
{
  "state": "success",
  "message": "书籍已添加到购物车"
}
```

## 2. 查看购物车

```http
GET /api/cart
```

### 请求头
```http
Authorization: Bearer <JWT_TOKEN>
```

### 响应
```json
{
  "state": "success",
  "cartItems": [
    {
      "bookId": "book123",
      "title": "书籍标题",
      "quantity": 1,
      "price": 29.99
    },
    {
      "bookId": "book456",
      "title": "另一书籍",
      "quantity": 2,
      "price": 49.99
    }
  ]
}
```

## 3. 从购物车中移除书籍

```http
POST /api/cart/remove
```

### 请求头
```http
Authorization: Bearer <JWT_TOKEN>
```

### 请求体
```json
{
  "bookId": "book123"
}
```

### 响应
```json
{
  "state": "success",
  "message": "书籍已从购物车中移除"
}
```

## 4. 购物车结算

```http
POST /api/cart/checkout
```

### 请求头
```http
Authorization: Bearer <JWT_TOKEN>
```

### 请求体
```json
{
  "paymentMethod": "credit_card",
}
```

### 响应

- **结算成功：**
```json
{
  "state": "success",
  "orderId": "order789",
  "totalAmount": 129.97,
  "message": "订单已成功创建"
}
```

- **结算失败（例如库存不足或支付失败）：**
```json
{
  "state": "failed",
  "message": "库存不足或支付处理失败"
}

