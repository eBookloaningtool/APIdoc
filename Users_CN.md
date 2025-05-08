# 认证 & 用户管理

## 用户管理

### 用户注册

```http
POST /api/users/register
```

#### 请求体

```json
{
  "email": "user@example.com",
  "password": "securepassword",
  "name": "John Doe"
}
```

#### 响应

```json
{
  "state": "success",
  "UUID": "3a0e3d23-5061-4602-a814-2bbc4447347e",
  "email": "user@example.com",
  "name": "John Doe",
  "createdat": "2025-03-28"
}
```

### 用户信息更新

```http
POST /api/users/update
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 请求体

```json
{
  "email": "new@example.com",
  "password": "NewPassword123",
  "name": "Updated Name"
}
```

#### 响应

```json
{
  "state": "success",
  "UUID": "3a0e3d23-5061-4602-a814-2bbc4447347e",
  "email": "new@example.com",
  "name": "Updated Name"
}
```

### 获取用户信息

```http
POST /api/users/info
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 响应

```json
{
  "UUID": "3a0e3d23-5061-4602-a814-2bbc4447347e",
  "name": "John Doe",
  "email": "user@example.com",
  "balance": 0,
  "createdat": "2025-03-28"
}
```

### 删除账号

```http
POST /api/users/delete
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 响应

```json
{
  "state": "success"
}
```

## 登录管理

### 登录

```http
POST /api/auth/login
```

#### 请求体

```json
{
  "email": "user@example.com",
  "password": "securepassword"
}
```

#### 响应

```json
{
  "state": "success",
  "token": "jwt_token_here",
  "expiresIn": 3600,
  "UUID": "3a0e3d23-5061-4602-a814-2bbc4447347e"
}
```

### 注销

```http
POST /api/auth/logout
```

#### 请求头

```http
Authorization: Bearer <JWT_TOKEN>
```

#### 响应

```json
{
  "state": "success"
}
```

### 忘记密码

```http
POST /api/auth/forget
```

#### 请求体

```json
{
  "email": "user@example.com"
}
```

#### 响应

```json
{
  "state": "success"
}
```