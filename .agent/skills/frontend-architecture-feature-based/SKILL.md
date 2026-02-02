---
name: frontend-architecture-feature-based
description: Standardized guidelines for organizing React applications using feature-based architecture. Use when structuring new projects, organizing large codebases, or implementing domain-driven folder structures.
---

# Frontend Architecture Feature Based

## When to use this skill
- Starting a new React/frontend project
- Refactoring a monolithic structure
- Organizing code by business features
- Implementing domain-driven design in frontend

## Workflow
- [ ] Identify business features/domains
- [ ] Create feature folders with clear boundaries
- [ ] Colocate related code (components, hooks, tests, styles)
- [ ] Define public API for each feature
- [ ] Avoid cross-feature dependencies

## Instructions

### Folder Structure

```
src/
├── features/
│   ├── auth/
│   │   ├── components/
│   │   │   ├── LoginForm.tsx
│   │   │   └── RegisterForm.tsx
│   │   ├── hooks/
│   │   │   └── useAuth.ts
│   │   ├── api/
│   │   │   └── authApi.ts
│   │   ├── types/
│   │   │   └── auth.types.ts
│   │   └── index.ts  # Public API
│   ├── products/
│   │   ├── components/
│   │   ├── hooks/
│   │   └── index.ts
│   └── cart/
├── shared/
│   ├── components/  # Shared UI
│   ├── hooks/
│   └── utils/
└── app/
    ├── App.tsx
    └── routes.tsx
```

### Key Principles

**1. Feature Colocation**
Keep all code related to a feature together:
```typescript
// features/products/index.ts (Public API)
export { ProductList } from './components/ProductList';
export { useProducts } from './hooks/useProducts';
export type { Product } from './types/product.types';
```

**2. Import Rules**
- Features can import from `shared/`
- Features CANNOT import from other features
- Use the public API (index.ts) only

**3. Shared Code**
Only extract to `shared/` when:
- Used by 3+ features
- Truly generic (not business logic)

## Resources
- Check existing skills for patterns
