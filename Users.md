# Authentication & User Management

## User Management

### User Registration

```http
POST /api/users/register
```

#### Request Body

```json
{
  "email": "user@example.com",
  "password": "securepassword",
  "name": "John Doe"
}
```

#### Response

```json
{
  "state": "success",
  "UUID": "3a0e3d23-5061-4602-a814-2bbc4447347e",
  "email": "user@example.com",
  "name": "John Doe",
  "createdat": "2025-03-28"
}
```

### Update User Information

```http
POST /api/users/update
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Request Body

```json
{
  "email": "new@example.com",
  "password": "NewPassword123",
  "name": "Updated Name"
}
```

#### Response

```json
{
  "state": "success",
  "UUID": "3a0e3d23-5061-4602-a814-2bbc4447347e",
  "email": "new@example.com",
  "name": "Updated Name"
}
```

### Get User Information

```http
POST /api/users/info
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Response

```json
{
  "UUID": "3a0e3d23-5061-4602-a814-2bbc4447347e",
  "name": "John Doe",
  "email": "user@example.com",
  "balance": 0,
  "createdat": "2025-03-28"
}
```

### Delete Account

```http
POST /api/users/delete
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Response

```json
{
  "state": "success"
}
```

## Login Management

### Login

```http
POST /api/auth/login
```

#### Request Body

```json
{
  "email": "user@example.com",
  "password": "securepassword"
}
```

#### Response

```json
{
  "state": "success",
  "token": "jwt_token_here",
  "expiresIn": 3600,
  "UUID": "3a0e3d23-5061-4602-a814-2bbc4447347e"
}
```

### Logout

```http
POST /api/auth/logout
```

#### Request Headers

```http
Authorization: Bearer <JWT_TOKEN>
```

#### Response

```json
{
  "state": "success"
}
```

### Forgot Password

```http
POST /api/auth/forget
```

#### Request Body

```json
{
  "email": "user@example.com"
}
```

#### Response

```json
{
  "state": "success"
}
```