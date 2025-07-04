# Borrowing System

### Borrow E-Books
```http
POST /api/borrow/borrow
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Request Body
```json
{
  "bookId": ["bookId1","bookId2","bookId3","bookId4","bookId5","bookId6"]
}
```
#### Response

- **Purchase Successful:**

```json
{
  "state": "success",
  "dueDate": "2025-03-20",
  "balance": 50.00
}
```

- **Insufficient Balance:**

```json
{
  "state": "insufficient balance",
  "newPayment": 2.5
}
```
- **Reached Borrowing Limit:**

```json
{
  "state": "Reach borrow limit"
}
```

- **Some Books Invalid/Out of Stock/Already Borrowed:**

```json
{
  "state": "Borrow failed.",
  "InvalidBookIds": ["bookId1","bookId2"],
  "LowStockBookIds": ["bookId3","bookId4"],
  "BorrowedBookIds": ["bookId5","bookId6"]
}
```

### Return E-Book
```http
POST /api/borrow/return/
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

### Renew E-Book
```http
POST /api/borrow/renew/
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

- **Renewal Successful:**

```json
{
  "state": "success",
  "newDueDate": "2025-04-03"
}
```

- **Insufficient Balance:**

```json
{
  "state": "insufficient balance",
  "newPayment": 2.5
}
```

### Get Recent Reading List
```http
POST /api/borrow/borrowlist/
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
      "borrowId": "borrowuuid1",
      "bookId": "bookId1",
      "borrowDate": "2025-01-01",
      "dueDate": "2025-02-01"
    }
  ]
}
```

### Get Borrowing History
```http
POST /api/borrow/history/
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
          "borrowId": "borrowuuid1",
          "bookId": "bookId1",
          "borrowDate": "2025-01-01",
          "dueDate": "2025-02-01",
          "returnDate": "2025-02-01",
          "status": "returned"
        }
    ]
}
```


