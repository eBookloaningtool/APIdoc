# 愿望清单

### 添加到愿望清单

```http
POST /api/wishlist
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
POST /api/deletewishlist
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
POST /api/getwishlist
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 请求体
```json
{
}
```

#### 响应

```json
{
  "bookId": ["bookId1", "bookId2"]
}
```