---
name: frontend-ui-shadcn
description: Standardized guidelines and patterns for Frontend Ui Shadcn.
---

# Frontend Ui Shadcn

## When to use this skill
- Using shadcn/ui components
- Customizing shadcn components
- Building with shadcn design system

## Workflow
- [ ] Install shadcn/ui
- [ ] Add components via CLI
- [ ] Customize in components/ui
- [ ] Apply design tokens
- [ ] Compose reusable patterns

## Instructions

### Installation
```bash
npx shadcn-ui@latest init
npx shadcn-ui@latest add button
```

### Usage
```typescript
import { Button } from '@/components/ui/button';

<Button variant="default">Click me</Button>
<Button variant="destructive">Delete</Button>
<Button variant="outline">Cancel</Button>
```

### Customization
Components are in `components/ui/` - modify directly.

## Resources
- Components are yours to own
- Built on Radix UI primitives
- Fully customizable with Tailwind
