# Shopping Cart

### Add Book to Cart

```http
POST /api/cart/add
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

### View Cart

```http
POST /api/cart/get
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

### Remove Books from Cart

```http
POST /api/cart/remove
```

#### Request Headers
```http
Authorization: Bearer <JWT_TOKEN>
```

#### Request Body
```json
{
  "bookId": ["bookId1", "bookId2"]
}
```

#### Response
```json
{
  "state": "success"
}
```
