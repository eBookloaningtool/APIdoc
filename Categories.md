# Category Management

### Get All Categories

```http
GET /api/categories/getAll
```

#### Response

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
