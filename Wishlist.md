# 愿望清单和购物车

### 添加到愿望清单

```http
POST /api/wishlist/add
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

### 取消愿望清单

```http
POST /api/wishlist/delete
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

### 获取愿望清单
```http
POST /api/wishlist/get
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