---
name: backend-codeigniter-routing
description: Route configuration, RESTful routes, URL structure.
---

# Backend CodeIgniter Routing

## When to use this skill
- Defining routes
- RESTful URLs
- Route groups
- API versioning

## Workflow
- [ ] Define in Config/Routes.php
- [ ] Use resource routes for REST
- [ ] Group related routes
- [ ] Version APIs
- [ ] Use route filters

## Instructions

### RESTful Routes
```php
<?php

// Config/Routes.php
$routes->resource('users', ['controller' => 'UserController']);
// GET    /users
// GET    /users/:id
// POST   /users
// PUT    /users/:id
// DELETE /users/:id
```

### API Versioning
```php
<?php

$routes->group('api/v1', ['namespace' => 'App\Controllers\API\V1'], function($routes) {
    $routes->resource('users');
    $routes->resource('orders');
});
```

### Route Filters
```php
<?php

$routes->group('api', ['filter' => 'auth'], function($routes) {
    $routes->get('profile', 'UserController::profile');
});
```

## Resources
- Use resource() for RESTful routes
- Group and version APIs
- Apply filters for middleware
