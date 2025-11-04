# <i class="fa fa-cogs"></i> User Management API Documentation

This API allows clients to manage user accounts, including creating, retrieving, updating, and deleting user profiles.

**Base URL**
`https://api.example.com/v1`

---

## <i class="fa fa-lock"></i> Authentication

All requests require an API key passed in the request header.

**Header**

```
Authorization: Bearer <your_api_key>
```

---

## <i class="fa fa-user"></i> 1. Get User by ID

**Endpoint**

```
GET /users/{id}
```

**Example Request**

```bash
curl -X GET "https://api.example.com/v1/users/101" \
-H "Authorization: Bearer abc123"
```

**Response**

```json
{
  "id": 101,
  "name": "Priyanka Sharma",
  "email": "priyanka@example.com",
  "role": "Admin"
}
```

**Example UI Preview**
![User Details](assets/user-details.png.jpg)

---

## <i class="fa fa-user-plus"></i> 2. Create a New User

**Endpoint**

```
POST /users
```

**Request Body**

```json
{
  "name": "Priyanka Sharma",
  "email": "priyanka@example.com",
  "role": "Admin"
}
```

**Response**

```json
{
  "id": 102,
  "message": "User created successfully"
}
```

**API Banner Example**
![API Banner](assets/api-banner.png.jpg)

---

## <i class="fa fa-exclamation-triangle"></i> 3. Error Codes

| Code | Meaning      | Example                    |
| ---- | ------------ | -------------------------- |
| 400  | Bad Request  | Missing required fields    |
| 401  | Unauthorized | Invalid or missing API key |
| 404  | Not Found    | User not found             |
| 500  | Server Error | Internal API failure       |

---

## <i class="fa fa-chart-line"></i> API Usage Stats Example

![API Usage Chart](assets/api-usage-chart.png.jpg)

---

## <i class="fa fa-check-circle"></i> Best Practices

* Use HTTPS for all requests.
* Cache responses where possible.
* Handle `429` (Rate Limit) errors gracefully.
* Keep your API keys secure.

---

## <i class="fa fa-book"></i> References

* [OpenAPI Specification](https://swagger.io/specification/)
* [Microsoft REST API Guidelines](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design)

---

<i class="fa fa-lightbulb"></i> **Note**
This page demonstrates visual, structured, and interactive API documentation following best practices and the [Microsoft Style Guide](https://learn.microsoft.com/en-us/style-guide/).
