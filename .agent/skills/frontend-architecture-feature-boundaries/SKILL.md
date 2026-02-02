---
name: frontend-architecture-feature-boundaries
description: Standardized guidelines for defining and enforcing boundaries between features to prevent tight coupling. Use when scaling applications, preventing circular dependencies, and maintaining module independence.
---

# Frontend Architecture Feature Boundaries

## When to use this skill
- Preventing spaghetti code in large apps
- Enforcing module independence
- Enabling parallel team development
- Preparing for potential micro-frontend migration

## Workflow
- [ ] Define clear feature boundaries
- [ ] Create public APIs for each feature
- [ ] Enforce import rules (linting)
- [ ] Use shared kernel for common code
- [ ] Document feature dependencies

## Instructions

### Boundary Rules

**Rule 1: No Direct Cross-Feature Imports**
```typescript
// ❌ BAD: Direct import from another feature
import { ProductCard } from '../../products/components/ProductCard';

// ✅ GOOD: Import from public API
import { ProductCard } from '@features/products';
```

**Rule 2: Public API Pattern**
```typescript
// features/products/index.ts (Public API)
// Only export what other features need
export { ProductCard } from './components/ProductCard';
export { useProducts } from './hooks/useProducts';
export type { Product } from './types';

// DON'T export internal helpers
// ❌ export { internal Helper } from './utils';
```

**Rule 3: Shared Kernel**
```
src/
├── features/
│   ├── products/
│   ├── cart/
│   └── checkout/
├── shared/              # Shared Kernel
│   ├── types/
│   │   └── common.types.ts
│   ├── components/
│   │   └── Button.tsx
│   └── utils/
└── core/               # Framework code
```

### Enforcing with ESLint

```javascript
// .eslintrc.js
module.exports = {
  rules: {
    'import/no-restricted-paths': ['error', {
      zones: [
        {
          target: './src/features/products',
          from: './src/features/cart',
          message: 'Products cannot import from Cart'
        },
        {
          target: './src/features/*',
          from: './src/features/*',
          except: ['./index.ts'],
          message: 'Must use public API (index.ts)'
        }
      ]
    }]
  }
};
```

### Feature Communication Patterns

**1. Events (Decoupled)**
```typescript
// features/cart/index.ts
export const cartEvents = {
  itemAdded: (productId: string) => {
    window.dispatchEvent(new CustomEvent('cart:item-added', {
      detail: { productId }
    }));
  }
};

// features/analytics/index.ts
window.addEventListener('cart:item-added', (e) => {
  trackEvent('cart_add', e.detail);
});
```

**2. Shared State (Zustand)**
```typescript
// shared/store/cartStore.ts
export const useCartStore = create<CartState>((set) => ({
  items: [],
  addItem: (item) => set((state) => ({
    items: [...state.items, item]
  }))
}));

// Any feature can use the store
import { useCartStore } from '@shared/store/cartStore';
```

**3. Context/Props (Direct)**
```typescript
// Only when features have parent-child relationship
<CheckoutFeature cartItems={cartItems} />
```

### Dependency Graph

```
┌─────────────┐
│   Shared    │
│   Kernel    │
└──────┬──────┘
       │
   ┌───┴───┬───────┬────────┐
   │       │       │        │
┌──▼───┐ ┌─▼────┐ ┌▼─────┐ ┌▼──────┐
│ Auth │ │ Cart │ │ Shop │ │ Admin │
└──────┘ └──────┘ └──────┘ └───────┘
   ↑       ↑       ↑        ↑
   └───────┴───────┴────────┘
         No cycles!
```

### Module Independence Checklist

- [ ] Feature can be deleted without breaking others
- [ ] Feature can be developed/tested in isolation
- [ ] Feature has clear, documented public API
- [ ] No circular dependencies
- [ ] Shared code is truly generic

## Resources
- Use barrel exports (index.ts) for public APIs
- Lint rules prevent boundary violations
- Events for loose coupling
