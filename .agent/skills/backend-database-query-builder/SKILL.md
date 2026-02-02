---
name: backend-database-query-builder
description: CodeIgniter query builder, joins, complex queries.
---

# Backend Database Query Builder

## When to use this skill
- Complex database queries
- Dynamic query construction
- JOIN operations
- Query optimization

## Workflow
- [ ] Use query builder for safety
- [ ] Avoid raw SQL when possible
- [ ] Use prepared statements
- [ ] Optimize with indexes
- [ ] Use get() vs first()

## Instructions

### Basic Queries
```php
<?php

$users = $this->db->table('users')
    ->where('status', 'active')
    ->orderBy('created_at', 'DESC')
    ->get()
    ->getResult();
```

### Joins
```php
<?php

$orders = $this->db->table('orders o')
    ->join('users u', 'u.id = o.user_id')
    ->join('products p', 'p.id = o.product_id')
    ->select('o.*, u.name as user_name, p.name as product_name')
    ->where('o.status', 'completed')
    ->get()
    ->getResult();
```

### Complex Conditions
```php
<?php

$this->db->table('users')
    ->groupStart()
        ->where('role', 'admin')
        ->orWhere('role', 'moderator')
    ->groupEnd()
    ->where('status', 'active')
    ->get();
```

## Resources
- Query builder prevents SQL injection
- Use whereIn() for multiple values
- Use groupBy() and having() for aggregates
