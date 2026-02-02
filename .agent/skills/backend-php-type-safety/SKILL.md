---
name: backend-php-type-safety
description: Strict types, type declarations, and static analysis for type-safe PHP code.
---

# Backend PHP Type Safety

## When to use this skill
- Building type-safe applications
- Preventing type-related bugs
- Using static analysis tools
- Writing maintainable code

## Workflow
- [ ] Enable strict_types in all files
- [ ] Type hint all parameters
- [ ] Declare return types
- [ ] Use PHPStan or Psalm
- [ ] Avoid mixed types

## Instructions

### Strict Types
```php
<?php

declare(strict_types=1);

// Now type coercion is disabled
function add(int $a, int $b): int
{
    return $a + $b;
}

add(1, 2);    // OK
// add('1', '2'); // TypeError in strict mode
```

### Property Types
```php
<?php

declare(strict_types=1);

class User
{
    private int $id;
    private string $email;
    private ?string $phone = null;
    private array $roles = [];

    public function __construct(int $id, string $email)
    {
        $this->id = $id;
        $this->email = $email;
    }
}
```

### Return Type Declarations
```php
<?php

declare(strict_types=1);

class UserService
{
    public function getUser(int $id): ?User
    {
        $user = $this->repository->find($id);
        return $user; // Can be User or null
    }

    public function getAllUsers(): array
    {
        return $this->repository->findAll();
    }

    public function createUser(array $data): User
    {
        // Must return User, not null
        return $this->repository->create($data);
    }
}
```

### Generic Collections with PHPDoc
```php
<?php

declare(strict_types=1);

class UserRepository
{
    /**
     * @return array<User>
     */
    public function findAll(): array
    {
        // PHPStan knows this returns array of User objects
        return [];
    }

    /**
     * @param array<int> $ids
     * @return array<User>
     */
    public function findByIds(array $ids): array
    {
        return [];
    }
}
```

### Static Analysis (PHPStan)
```bash
# Install
composer require --dev phpstan/phpstan

# Run
vendor/bin/phpstan analyse app
```

```neon
# phpstan.neon
parameters:
    level: 8
    paths:
        - app
```

## Resources
- Always enable strict_types
- Type hint everything
- Use static analysis in CI/CD
- PHPStan level 8 for maximum safety
