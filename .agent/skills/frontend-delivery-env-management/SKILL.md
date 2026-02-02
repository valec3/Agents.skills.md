---
name: frontend-delivery-env-management
description: Standardized guidelines and patterns for Frontend Delivery Env Management.
---

# Frontend Delivery Env Management

## When to use this skill
- Managing environment variables
- Configuring for different environments
- Handling secrets

## Workflow
- [ ] Create .env files
- [ ] Use environment-specific configs
- [ ] Never commit secrets
- [ ] Validate env vars at startup
- [ ] Document required vars

## Instructions

### .env Files
```bash
# .env.local (not committed)
VITE_API_URL=http://localhost:3000

# .env.production
VITE_API_URL=https://api.example.com
```

### Usage
```typescript
const apiUrl = import.meta.env.VITE_API_URL;
```

### Validation
```typescript
const requiredEnvVars = ['VITE_API_URL'];
requiredEnvVars.forEach(key => {
  if (!import.meta.env[key]) {
    throw new Error(`Missing env var: ${key}`);
  }
});
```

## Resources
- Prefix with VITE_ or NEXT_PUBLIC_
- Never commit secrets
- Validate at startup
