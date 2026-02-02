---
name: backend-codeigniter-validation
description: Input validation, custom rules, error handling.
---

# Backend CodeIgniter Validation

## When to use this skill
- Validating user input
- Custom validation rules
- Form validation
- API request validation

## Workflow
- [ ] Define validation rules
- [ ] Use in controllers or models
- [ ] Create custom rules
- [ ] Return validation errors
- [ ] Localize error messages

## Instructions

### Controller Validation
```php
<?php

public function create()
{
    $rules = [
        'email' => 'required|valid_email|is_unique[users.email]',
        'password' => 'required|min_length[8]',
        'name' => 'required|min_length[3]'
    ];

    if (!$this->validate($rules)) {
        return $this->fail($this->validator->getErrors());
    }

    // Process valid data
}
```

### Custom Rule
```php
<?php

// Config/Validation.php
public function strong_password(string $password): bool
{
    return preg_match('/^(?=.*[a-z])(?=.*[A-Z])(?=.*\d).{8,}$/', $password);
}
```

## Resources
- Validate all user input
- Use built-in rules
- Create custom rules when needed
