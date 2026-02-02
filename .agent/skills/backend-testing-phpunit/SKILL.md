---
name: backend-testing-phpunit
description: Unit testing, test structure, mocking.
---

# Backend Testing PHPUnit

## When to use this skill
- Writing tests
- TDD development
- CI/CD pipelines
- Code quality

## Workflow
- [ ] Write tests for critical logic
- [ ] Test edge cases
- [ ] Mock dependencies
- [ ] Run before commits
- [ ] Maintain tests

## Instructions

### Test Class
```php
<?php

namespace Tests\Unit;

use CodeIgniter\Test\CIUnitTestCase;

class UserServiceTest extends CIUnitTestCase
{
    protected $service;

    protected function setUp(): void
    {
        parent::setUp();
        $this->service = new UserService();
    }

    public function testCreateUserWithValidData()
    {
        $data = ['name' => 'John', 'email' => 'john@example.com'];
        $user = $this->service->createUser($data);

        $this->assertInstanceOf(User::class, $user);
        $this->assertEquals('John', $user->name);
    }

    public function testCreateUserThrowsExceptionWithInvalidEmail()
    {
        $this->expectException(ValidationException::class);
        $this->service->createUser(['email' => 'invalid']);
    }
}
```

### Run Tests
```bash
vendor/bin/phpunit
```

## Resources
- Test business logic
- Mock external dependencies
- Use descriptive test names
