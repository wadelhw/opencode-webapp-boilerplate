# API 设计规范

本文档定义了使用此脚手架时的 API 设计规范。

## RESTful 设计原则

- 使用名词复数形式：`/users`, `/posts`
- 使用 HTTP 方法表示操作：GET, POST, PUT, DELETE
- 使用嵌套表示关系：`/users/123/posts`

## 响应格式

### 成功响应

```json
{
  "data": { ... },
  "message": "Success"
}
```

### 错误响应

```json
{
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Invalid input"
  }
}
```

## 认证

- 使用 Bearer Token
- 在 header 中传递：`Authorization: Bearer <token>`

## 版本控制

- URL 版本：`/api/v1/users`
- 或 Header 版本：`Accept: application/vnd.api+json;version=1`
