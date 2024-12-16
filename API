## User Data

```json
{
  "users": [
    {
      "id": "usr_001",
      "name": "John Smith",
      "email": "john.smith@email.com",
      "created_at": "2024-11-15T08:30:00Z",
      "status": "active",
      "preferences": {
        "theme": "dark",
        "notifications": true
      }
    },
    {
      "id": "usr_002",
      "name": "Emma Wilson",
      "email": "emma.w@email.com",
      "created_at": "2024-11-16T14:20:00Z",
      "status": "inactive",
      "preferences": {
        "theme": "light",
        "notifications": false
      }
    }
  ]
}
```

## Product Data

```json
{
  "products": [
    {
      "product_id": "prod_001",
      "name": "Premium Widget",
      "price": 29.99,
      "category": "electronics",
      "inventory": 150,
      "specifications": {
        "weight": "250g",
        "dimensions": "10x5x3cm",
        "color": "silver"
      }
    },
    {
      "product_id": "prod_002",
      "name": "Super Gadget",
      "price": 49.99,
      "category": "electronics",
      "inventory": 75,
      "specifications": {
        "weight": "400g",
        "dimensions": "15x8x5cm",
        "color": "black"
      }
    }
  ]
}
```

## Order Data

```json
{
  "orders": [
    {
      "order_id": "ord_001",
      "user_id": "usr_001",
      "order_date": "2024-12-15T10:30:00Z",
      "status": "completed",
      "items": [
        {
          "product_id": "prod_001",
          "quantity": 2,
          "price": 59.98
        }
      ],
      "total": 59.98,
      "shipping_address": {
        "street": "123 Main St",
        "city": "Boston",
        "country": "USA",
        "postal_code": "02108"
      }
    }
  ]
}
```

## API Endpoints

```yaml
endpoints:
  - path: /api/v1/users
    method: GET
    description: Get all users
    response: users[]
    
  - path: /api/v1/products
    method: GET
    description: Get all products
    response: products[]
    
  - path: /api/v1/orders
    method: POST
    description: Create new order
    request: order
    response: order_id
```
