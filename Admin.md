


### **8.1 删除书籍**
```http
DELETE /api/books/{bookId}
```

---

### **8.2 类别管理（增删改查）**
接口描述：管理员对电子书分类进行管理。

**添加分类**
```http
POST /admin/categories
```
**请求体**
```json
{
  "name": "Programming",
  "description": "Books about programming"
}
```
**响应**
```json
{
  "message": "分类操作成功",
  "data": {
    "categoryId": "cat7001",
    "name": "Programming"
  }
}
```

**获取分类列表**
```http
GET /admin/categories
```

**更新分类**
```http
PUT /admin/categories/{categoryId}
```

**删除分类**
```http
DELETE /admin/categories/{categoryId}
```

---

### **8.3 管理员获取用户列表**
```http
GET /admin/users
```
**请求参数**  
- `page`  
- `size`  
- `search`

**响应**
```json
{
  "code": 200,
  "data": [
    {
      "userId": "12345",
      "username": "user123",
      "email": "user@example.com",
      "role": "user"
    },
    {
      "userId": "67890",
      "username": "admin",
      "email": "admin@example.com",
      "role": "admin"
    }
  ],
  "total": 50
}
```


### **2.4 添加新书（管理员）**
```http
POST /admin/books
```
**请求体**
```json
{
  "title": "New Book",
  "author": "Jane Doe",
  "publisher": "Example Publisher",
  "isbn": "978-0987654321",
  "category": "Science Fiction",
  "availableCopies": 10,
  "totalCopies": 10,
  "coverUrl": "https://example.com/new-book.jpg",
  "description": "A thrilling sci-fi adventure.",
  "price": 7.99
}
```
**响应**
```json
{
  "message": "电子书添加成功",
  "data": {
    "bookId": "book999",
    "title": "New Book"
  }
}
```
