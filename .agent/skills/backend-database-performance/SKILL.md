---
name: backend-database-performance
description: Query optimization, indexing, N+1 prevention.
---

# Backend Database Performance

## When to use this skill
- Slow queries
- N+1 problems
- Large datasets
- Production optimization

## Workflow
- [ ] Profile queries
- [ ] Add indexes
- [ ] Prevent N+1
- [ ] Use eager loading
- [ ] Cache results

## Instructions

### N+1 Problem
```php
<?php

// ❌ Bad: N+1 queries
$users = $userModel->findAll();
foreach ($users as $user) {
    $user->orders; // Separate query per user
}

// ✅ Good: Single query with join
$users = $this->db->table('users u')
    ->select('u.*, GROUP_CONCAT(o.id) as order_ids')
    ->join('orders o', 'o.user_id = u.id', 'left')
    ->groupBy('u.id')
    ->get()
    ->getResult();
```

### Indexing
```php
<?php

$this->forge->addField([
    'email' => ['type' => 'VARCHAR', 'constraint' => 255]
]);
$this->forge->addKey('email'); // Index
$this->forge->addUniqueKey('email'); // Unique index
```

### Query Profiling
```php
<?php

$db = \Config\Database::connect();
$db->query("SELECT * FROM users WHERE status = 'active'");
$db->showLastQuery(); // See exact query
```

## Resources
- Index frequently queried columns
- Avoid SELECT *
- Use LIMIT for pagination
- Cache expensive queries
