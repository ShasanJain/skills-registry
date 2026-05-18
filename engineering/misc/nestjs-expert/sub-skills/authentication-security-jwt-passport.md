---
name: authentication-security-jwt-passport
description: Use when executing authentication security jwt passport protocols within the engineering sector.
---

# Authentication Security Jwt Passport: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Authentication Security Jwt Passport. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Authentication & Security (JWT + Passport)

- [ ] JWT Strategy imports from 'passport-jwt' not 'passport-local'
- [ ] JwtModule secret matches JwtStrategy secretOrKey exactly
- [ ] Authorization headers follow 'Bearer [token]' format
- [ ] Token expiration times are appropriate for use case
- [ ] JWT_SECRET environment variable is properly configured