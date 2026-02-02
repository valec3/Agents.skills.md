---
name: backend-quality-debugging
description: Debugging tools, logging, error tracking.
---

# Backend Quality Debugging

## When to use this skill
- Troubleshooting bugs
- Production issues
- Performance problems
- Error tracking

## Workflow
- [ ] Enable debug mode (dev only)
- [ ] Use logging
- [ ] Check query execution
- [ ] Use Kint for variables
- [ ] Track errors

## Instructions

### Logging
```php
<?php

log_message('error', 'User not found: ' . $userId);
log_message('debug', 'Processing order: ' . $orderId);
log_message('info', 'Email sent to: ' . $email);
```

### Debug Toolbar
```php
<?php

// Config/Boot/development.php
Services::toolbar()->respond();
```

### Variable Debugging
```php
<?php

d($variable);    // Dump
dd($variable);   // Dump and die
```

### Query Debugging
```php
<?php

$db = \Config\Database::connect();
echo $db->getLastQuery();
```

## Resources
- Log errors and important events
- Use debug toolbar in dev
- Never show errors in production
