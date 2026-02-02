---
name: backend-deployment-production-checklist
description: Production readiness, security headers, optimization.
---

# Backend Deployment Production Checklist

## When to use this skill
- Before production deploy
- Security audits
- Performance optimization
- Compliance checks

## Workflow
- [ ] Disable debug mode
- [ ] Enable error logging
- [ ] Set security headers
- [ ] Enable HTTPS
- [ ] Optimize autoloader
- [ ] Cache configuration

## Instructions

### Production Checklist
- [ ] CI_ENVIRONMENT = production
- [ ] Debug toolbar disabled
- [ ] Error display off
- [ ] Logging enabled
- [ ] HTTPS enforced
- [ ] CSRF protection enabled
- [ ] SQL injection protection
- [ ] Rate limiting
- [ ] Input validation
- [ ] Password hashing
- [ ] Secure sessions
- [ ] .env file secured
- [ ] Dependencies updated
- [ ] Database indexes
- [ ] Caching enabled

### Security Headers
```php
<?php

// Config/Filters.php
header('X-Frame-Options: DENY');
header('X-Content-Type-Options: nosniff');
header('X-XSS-Protection: 1; mode=block');
header('Strict-Transport-Security: max-age=31536000');
```

## Resources
- Use production .env
- Enable all security features
- Monitor errors and logs
- Regular security updates
