---
name: backend-php-standards
description: PSR standards, coding conventions, and best practices for modern PHP development.
---

# Backend PHP Standards

## When to use this skill
- Starting new PHP projects
- Code reviews
- Establishing team standards
- Refactoring legacy code

## Workflow
- [ ] Follow PSR-12 coding style
- [ ] Use PSR-4 autoloading
- [ ] Enable strict types
- [ ] Type hint all parameters and returns
- [ ] Use meaningful variable names

## Instructions

### PSR-12 Coding Style
```php
<?php

declare(strict_types=1);

namespace App\Controllers;

use App\Services\UserService;

class UserController extends BaseController
{
    public function __construct(
        private readonly UserService $userService
    ) {}

    public function index(): string
    {
        $users = $this->userService->getAllUsers();
        return view('users/index', ['users' => $users]);
    }
}
```

### Strict Types
```php
<?php

declare(strict_types=1);

function calculateTotal(int $quantity, float $price): float
{
    return $quantity * $price;
}
```

### Naming Conventions
- **Classes**: PascalCase (`UserController`, `OrderService`)
- **Methods**: camelCase (`getUser()`, `createOrder()`)
- **Constants**: UPPER_SNAKE_CASE (`MAX_RETRIES`, `API_VERSION`)
- **Properties**: camelCase (`$userName`, `$isActive`)

## Resources
- PSR-1: Basic coding standard
- PSR-12: Extended coding style
- PSR-4: Autoloading standard
