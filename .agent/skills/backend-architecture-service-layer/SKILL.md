---
name: backend-architecture-service-layer
description: Service layer pattern, business logic organization.
---

# Backend Architecture Service Layer

## When to use this skill
- Complex business logic
- Reusable operations
- Keeping controllers thin
- Testing business logic

## Workflow
- [ ] Create service classes
- [ ] Inject dependencies
- [ ] Keep one responsibility per service
- [ ] Return DTOs or entities
-[ ] Handle business rules

## Instructions

### Service Class
```php
<?php

namespace App\Services;

use App\Models\OrderModel;
use App\Entities\Order;

class OrderService
{
    public function __construct(
        private OrderModel $orderModel,
        private PaymentService $paymentService,
        private EmailService $emailService
    ) {}

    public function createOrder(array $data): Order
    {
        $order = $this->orderModel->insert($data);
        $this->paymentService->process($order);
        $this->emailService->sendConfirmation($order);
        return $order;
    }
}
```

## Resources
- Services encapsulate business logic
- Inject all dependencies
- Keep services focused
