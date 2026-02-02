---
name: frontend-delivery-build-tools
description: Standardized guidelines and patterns for Frontend Delivery Build Tools.
---

# Frontend Delivery Build Tools

## When to use this skill
- Configuring build process
- Optimizing bundle size
- Setting up Vite/Webpack

## Workflow
- [ ] Choose build tool (Vite recommended)
- [ ] Configure for production
- [ ] Optimize bundle size
- [ ] Enable code splitting
- [ ] Analyze bundle

## Instructions

### Vite Config
```typescript
// vite.config.ts
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()],
  build: {
    rollupOptions: {
      output: {
        manualChunks: {
          vendor: ['react', 'react-dom'],
          ui: ['@radix-ui/react-dialog']
        }
      }
    }
  }
});
```

### Bundle Analysis
```bash
npm install -D rollup-plugin-visualizer
```

## Resources
- Use Vite for modern apps
- Code split by route
- Analyze bundle regularly
