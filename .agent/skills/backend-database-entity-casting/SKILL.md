---
name: backend-database-entity-casting
description: Entity usage, type casting, data transformation.
---

# Backend Database Entity Casting

## When to use this skill
- Type-safe database entities
- Data transformation
- Computed properties
- Encapsulation

## Workflow
- [ ] Define entity class
- [ ] Set $casts property
- [ ] Create getters/setters
- [ ] Add computed properties
- [ ] Use in models

## Instructions

### Entity with Casting
```php
<?php

namespace App\Entities;

use CodeIgniter\Entity\Entity;

class User extends Entity
{
    protected $casts = [
        'id' => 'integer',
        'is_active' => 'boolean',
        'metadata' => 'json',
        'created_at' => 'datetime',
        'settings' => 'json-array'
    ];

    protected $dates = ['created_at', 'updated_at', 'deleted_at'];

    // Getter
    public function getFullName(): string
    {
        return $this->attributes['first_name'] . ' ' . $this->attributes['last_name'];
    }

    // Setter
    public function setPassword(string $password)
    {
        $this->attributes['password'] = password_hash($password, PASSWORD_DEFAULT);
        return $this;
    }

    // Computed property
    public function isAdmin(): bool
    {
        return $this->role === 'admin';
    }
}
```

### Usage
```php
<?php

$user = $userModel->find(1);
echo $user->full_name; // Calls getFullName()
$user->password = 'newpass'; // Calls setPassword()
if ($user->isAdmin()) { }
```

## Resources
- Casts auto-convert types
- Computed properties via getters
- Mutators via setters
