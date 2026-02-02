---
name: frontend-state-strategy
description: Standardized guidelines and patterns for Frontend State Strategy.
---

# Frontend State Strategy

## When to use this skill
- Choosing state management solution
- Architecting state in applications
- Refactoring state management

## Workflow
- [ ] Identify state types (local, global, server)
- [ ] Choose appropriate tool for each type
- [ ] Avoid prop drilling
- [ ] Colocate state with usage
- [ ] Keep state minimal

## Instructions

### State Types
1. **Local State**: useState, useReducer
2. **Global State**: Context, Zustand, Redux
3. **Server State**: React Query, SWR
4. **URL State**: useSearchParams, router

### Decision Tree
```
Is it server data? → React Query
Is it global UI state? → Zustand/Context
Is it local to component? → useState
Is it derived? → useMemo
```

### Example
```typescript
// Local
const [count, setCount] = useState(0);

// Global
const theme = useThemeStore(state => state.theme);

// Server
const { data: user } = useQuery('user', fetchUser);

// URL
const [searchParams] = useSearchParams();
```

## Resources
- Prefer local state
- Server state separate from client state
- Use Context sparingly
