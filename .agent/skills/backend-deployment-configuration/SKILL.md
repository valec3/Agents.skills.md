---
name: backend-deployment-configuration
description: Environment config, .env management.
---

# Backend Deployment Configuration

## When to use this skill
- Environment setup
- Configuration management
- Deployment
- Security

## Workflow
- [ ] Use .env for config
- [ ] Never commit .env
- [ ] Separate dev/staging/prod
- [ ] Validate required vars
- [ ] Document configuration

## Instructions

### .env File
```bash
# .env
CI_ENVIRONMENT = production

database.default.hostname = localhost
database.default.database = myapp
database.default.username = dbuser
database.default.password = secret
database.default.DBDriver = MySQLi

JWT_SECRET = your-secret-key
API_KEY = external-api-key
```

### Usage
```php
<?php

$dbHost = env('database.default.hostname');
$jwtSecret = env('JWT_SECRET');
```

### Required Vars Check
```php
<?php

$required = ['JWT_SECRET', 'database.default.password'];
foreach ($required as $key) {
    if (!env($key)) {
        throw new \RuntimeException("Missing env var: {$key}");
    }
}
```

## Resources
- Use .env for all config
- Different .env per environment
- Never commit secrets
