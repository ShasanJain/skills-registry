---
name: postman-collection
description: Use when executing postman collection protocols within the engineering sector.
---

# Postman Collection: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Postman Collection. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Postman Collection

Export collection for easy testing:
```json
{
  "info": {
    "name": "My API",
    "schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json"
  },
  "item": [
    {
      "name": "Create User",
      "request": {
        "method": "POST",
        "url": "{{baseUrl}}/api/v1/users"
      }
    }
  ]
}
```

## Related Skills

- `@doc-coauthoring` - For collaborative documentation writing
- `@copywriting` - For clear, user-friendly descriptions
- `@test-driven-development` - For ensuring API behavior matches docs
- `@systematic-debugging` - For troubleshooting API issues

## Additional Resources

- [OpenAPI Specification](https://swagger.io/specification/)
- [REST API Best Practices](https://restfulapi.net/)
- [GraphQL Documentation](https://graphql.org/learn/)
- [API Design Patterns](https://www.apiguide.com/)
- [Postman Documentation](https://learning.postman.com/docs/)

---

**Pro Tip:** Keep your API documentation as close to your code as possible. Use tools that generate docs from code comments to ensure they stay in sync!