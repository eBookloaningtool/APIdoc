# Wishlist and Shopping Cart

### Add to Wishlist

```http
POST /api/wishlist/add
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Request Body
```json
{
  "bookId": "book123"
}
```

#### Response

```json
{
  "state": "success"
}
```

### Remove from Wishlist

```http
POST /api/wishlist/delete
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Request Body
```json
{
  "bookId": "bookId1"
}
```

#### Response

```json
{
  "state": "success"
}
```

### Get Wishlist
```http
POST /api/wishlist/get
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Response

```json
{
  "bookId": ["bookId1", "bookId2"]
}
```
