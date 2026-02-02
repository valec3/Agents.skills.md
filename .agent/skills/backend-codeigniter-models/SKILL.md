---
name: backend-codeigniter-models
description: Model patterns, entity usage, query builder.
---

# Backend CodeIgniter Models

## When to use this skill
- Database operations
- Using entities
- Query builder
- Data validation

## Workflow
- [ ] Extend CodeIgniter\Model
- [ ] Define table and fields
- [ ] Use entities for type safety
- [ ] Enable validation
- [ ] Use callbacks

## Instructions

### Model with Entity
```php
<?php

namespace App\Models;

use CodeIgniter\Model;

class UserModel extends Model
{
    protected $table = 'users';
    protected $primaryKey = 'id';
    protected $returnType = 'App\Entities\User';
    protected $allowedFields = ['name', 'email', 'password'];
    protected $useTimestamps = true;
    protected $validationRules = [
        'email' => 'required|valid_email|is_unique[users.email]',
        'password' => 'required|min_length[8]'
    ];

    protected $beforeInsert = ['hashPassword'];

    protected function hashPassword(array $data)
    {
        if (isset($data['data']['password'])) {
            $data['data']['password'] = password_hash($data['data']['password'], PASSWORD_DEFAULT);
        }
        return $data;
    }
}
```

### Entity
```php
<?php

namespace App\Entities;

use CodeIgniter\Entity\Entity;

class User extends Entity
{
    protected $casts = [
        'id' => 'integer',
        'is_active' => 'boolean',
        'created_at' => 'datetime'
    ];

    public function setPassword(string $password)
    {
        $this->attributes['password'] = password_hash($password, PASSWORD_DEFAULT);
        return $this;
    }
}
```

## Resources
- Use entities for type safety
- Enable validation in model
- Use callbacks for data transformation
