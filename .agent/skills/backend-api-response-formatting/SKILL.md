---
name: backend-api-response-formatting
description: Consistent response structure, error handling.
---

# Backend API Response Formatting

## When to use this skill
- API development
- Consistent responses
- Error handling
- Client expectations

## Workflow
- [ ] Define response format
- [ ] Wrap data consistently
- [ ] Include metadata
- [ ] Standard error format
- [ ] Document responses

## Instructions

### Success Response
```php
<?php

return $this->respond([
    'success' => true,
    'data' => $users,
    'meta' => [
        'page' => 1,
        'per_page' => 10,
        'total' => 100
    ]
]);
```

### Error Response
```php
<?php

return $this->fail([
    'success' => false,
    'error' => [
        'code' => 'VALIDATION_ERROR',
        'message' => 'Invalid input',
        'details' => [
            'email' => ['Email is required']
        ]
    ]
], 400);
```

### Response Trait
```php
<?php

trait ApiResponseTrait
{
    protected function success($data, $message = null, $code = 200)
    {
        return $this->respond([
            'success' => true,
            'message' => $message,
            'data' => $data
        ], $code);
    }

    protected function error($message, $code = 400, $details = null)
    {
        return $this->fail([
            'success' => false,
            'error' => [
                'message' => $message,
                'details' => $details
            ]
        ], $code);
    }
}
```

## Resources
- Consistent structure
- Include success flag
- Standard error format
