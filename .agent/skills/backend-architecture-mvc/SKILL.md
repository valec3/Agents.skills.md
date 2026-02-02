---
name: backend-architecture-mvc
description: MVC pattern in CodeIgniter, separation of concerns.
---

# Backend Architecture MVC

## When to use this skill
- Organizing CodeIgniter applications
- Separating concerns properly
- Building maintainable apps

## Workflow
- [ ] Controllers handle HTTP requests
- [ ] Models handle data logic
- [ ] Views handle presentation
- [ ] Keep controllers thin
- [ ] Business logic in services

## Instructions

### Controller (Thin)
```php
<?php

namespace App\Controllers;

use App\Services\UserService;

class UserController extends BaseController
{
    public function __construct(
        private readonly UserService $service
    ) {}

    public function index()
    {
        $users = $this->service->getAllUsers();
        return view('users/index', ['users' => $users]);
    }

    public function store()
    {
        $user = $this->service->createUser($this->request->getPost());
        return $this->respond($user);
    }
}
```

### Model (Data Access)
```php
<?php

namespace App\Models;

use CodeIgniter\Model;

class UserModel extends Model
{
    protected $table = 'users';
    protected $allowedFields = ['name', 'email'];
    protected $returnType = 'App\Entities\User';
}
```

### Service (Business Logic)
```php
<?php

namespace App\Services;

class UserService
{
    public function __construct(
        private UserModel $model
    ) {}

    public function getAllUsers()
    {
        return $this->model->findAll();
    }
}
```

## Resources
- Controllers: thin, route to services
- Models: database operations only
- Services: business logic
