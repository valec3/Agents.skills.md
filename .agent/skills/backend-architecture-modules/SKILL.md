---
name: backend-architecture-modules
description: Modular structure, namespace organization.
---

# Backend Architecture Modules

## When to use this skill
- Large applications
- Feature-based organization
- Team collaboration
- Reusable modules

## Workflow
- [ ] Organize by feature/module
- [ ] Use namespaces
- [ ] Define module boundaries
- [ ] Create module-specific folders
- [ ] Avoid cross-module dependencies

## Instructions

### Module Structure
```
app/
├── Modules/
│   ├── User/
│   │   ├── Controllers/
│   │   ├── Models/
│   │   ├── Services/
│   │   ├── Entities/
│   │   └── Config/
│   ├── Order/
│   └── Product/
```

### Module Registration
```php
<?php

// Config\Modules.php
$modules->discoverInNamespace = true;
$modules->aliases = [
    'User' => 'App\Modules\User',
    'Order' => 'App\Modules\Order',
];
```

## Resources
- Feature-based organization
- Clear module boundaries
- Independent deployment
