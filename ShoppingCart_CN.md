# 购物车

### 添加书籍到购物车

```http
POST /api/cart/add
```

#### 请求头
```http
Authorization: Bearer <JWT_TOKEN>
```

#### 请求体
```json
{
  "bookId": "book123"
}
```

#### 响应
```json
{
  "state": "success"
}
```

### 查看购物车

```http
POST /api/cart/get
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 响应

```json
{
  "bookId": ["bookId1", "bookId2"]
}
```

### 从购物车中移除书籍

```http
POST /api/cart/remove
```

#### 请求头
```http
Authorization: Bearer <JWT_TOKEN>
```

#### 请求体
```json
{
  "bookId": ["bookId1", "bookId2"]
}
```

#### 响应
```json
{
  "state": "success"
}
```
