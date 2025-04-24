# 分类管理

### 获取所有分类

```http
GET /api/categories/getAll
```

#### 响应

```json
{
    "state": "Success",
    "categoriesList": [
        {
            "name": "Adventure",
            "description": "Stories featuring exciting journeys and exploration."
        },
        {
            "name": "Art (Photography/Film)",
            "description": "Books focused on art forms like photography and film."
        }
    ]
}
```
