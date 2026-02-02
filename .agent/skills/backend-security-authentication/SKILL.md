---
name: backend-security-authentication
description: JWT, session management, password hashing.
---

# Backend Security Authentication

## When to use this skill
- User login/registration
- API authentication
- Session management
- Password security

## Workflow
- [ ] Hash passwords properly
- [ ] Generate secure tokens
- [ ] Validate credentials
- [ ] Implement logout
- [ ] Refresh tokens

## Instructions

### Password Hashing
```php
<?php

// Hash
$hash = password_hash($password, PASSWORD_DEFAULT);

// Verify
if (password_verify($inputPassword, $user->password)) {
    // Correct
}
```

### JWT Authentication
```php
<?php

use Firebase\JWT\JWT;

class AuthService
{
    public function generateToken(User $user): string
    {
        $payload = [
            'iss' => 'myapp',
            'sub' => $user->id,
            'iat' => time(),
            'exp' => time() + 3600
        ];

        return JWT::encode($payload, env('JWT_SECRET'), 'HS256');
    }

    public function validateToken(string $token): ?object
    {
        try {
            return JWT::decode($token, new Key(env('JWT_SECRET'), 'HS256'));
        } catch (\Exception $e) {
            return null;
        }
    }
}
```

## Resources
- Never store plain passwords
- Use strong JWT secrets
- Implement token refresh
