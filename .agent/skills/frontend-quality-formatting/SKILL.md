---
name: frontend-quality-formatting
description: Standardized guidelines and patterns for Frontend Quality Formatting.
---

# Frontend Quality Formatting

## When to use this skill
- Enforcing code style
- Setting up Prettier
- Configuring auto-formatting

## Workflow
- [ ] Install Prettier
- [ ] Create .prettierrc
- [ ] Add format script
- [ ] Set up editor integration
- [ ] Add to pre-commit

## Instructions

### Installation
```bash
npm install -D prettier
```

### Config
```json
// .prettierrc
{
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2,
  "trailingComma": "es5"
}
```

### Scripts
```json
{
  "scripts": {
    "format": "prettier --write "src/**/*.{ts,tsx}""
  }
}
```

## Resources
- Consistent code style
- Auto-format on save
- Combine with ESLint
