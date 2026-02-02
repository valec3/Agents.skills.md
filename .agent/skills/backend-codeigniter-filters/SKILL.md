---
name: backend-codeigniter-filters
description: Middleware/filters, authentication, CORS.
---

# Backend CodeIgniter Filters

## When to use this skill
- Authentication
- CORS
- Rate limiting
- Request/response modification

## Workflow
- [ ] Create filter class
- [ ] Register in Config/Filters.php
- [ ] Apply to routes
- [ ] Handle before/after
- [ ] Return responses or modify request

## Instructions

### Auth Filter
```php
<?php

namespace App\Filters;

use CodeIgniter\HTTP\RequestInterface;
use CodeIgniter\HTTP\ResponseInterface;
use CodeIgniter\Filters\FilterInterface;

class AuthFilter implements FilterInterface
{
    public function before(RequestInterface $request, $arguments = null)
    {
        $token = $request->getHeaderLine('Authorization');
        
        if (!$this->validateToken($token)) {
            return Services::response()
                ->setJSON(['error' => 'Unauthorized'])
                ->setStatusCode(401);
        }
    }

    public function after(RequestInterface $request, ResponseInterface $response, $arguments = null)
    {
        // Post-processing
    }
}
```

### CORS Filter
```php
<?php

class CorsFilter implements FilterInterface
{
    public function before(RequestInterface $request, $arguments = null)
    {
        header('Access-Control-Allow-Origin: *');
        header('Access-Control-Allow-Methods: GET, POST, PUT, DELETE');
        header('Access-Control-Allow-Headers: Content-Type, Authorization');

        if ($request->getMethod() === 'options') {
            exit;
        }
    }
}
```

## Resources
- before() runs before controller
- after() runs after controller
- Return response to short-circuit
