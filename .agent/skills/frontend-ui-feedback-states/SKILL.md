---
name: frontend-ui-feedback-states
description: Standardized guidelines and patterns for Frontend Ui Feedback States.
---

# Frontend Ui Feedback States

## When to use this skill
- Implementing loading states
- Handling errors gracefully
- Showing empty states
- Providing user feedback

## Workflow
- [ ] Identify all possible states
- [ ] Design for loading state
- [ ] Design for error state
- [ ] Design for empty state
- [ ] Design for success state

## Instructions

### State Pattern
```typescript
type DataState<T> = 
  | { status: 'idle' }
  | { status: 'loading' }
  | { status: 'success'; data: T }
  | { status: 'error'; error: Error };

function UserProfile() {
  const [state, setState] = useState<DataState<User>>({ status: 'idle' });

  if (state.status === 'loading') return <Skeleton />;
  if (state.status === 'error') return <ErrorMessage error={state.error} />;
  if (state.status === 'success') return <UserCard user={state.data} />;
  
  return null;
}
```

### Loading States
- Skeletons for content
- Spinners for actions
- Progress bars for uploads

### Empty States
- Clear message
- Illustration
- Call-to-action

## Resources
- Always handle all states
- Provide clear error messages
- Make loading states feel fast
