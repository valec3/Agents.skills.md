---
name: frontend-state-server-react-query
description: Standardized guidelines and patterns for Frontend State Server React Query.
---

# Frontend State Server React Query

## When to use this skill
- Fetching server data
- Managing cache
- Optimistic updates
- Background refetching

## Workflow
- [ ] Setup QueryClient
- [ ] Use useQuery for reads
- [ ] Use useMutation for writes
- [ ] Invalidate queries on mutations
- [ ] Configure stale/cache times

## Instructions

### Setup
```typescript
import { QueryClient, QueryClientProvider } from '@tanstack/react-query';

const queryClient = new QueryClient();

<QueryClientProvider client={queryClient}>
  <App />
</QueryClientProvider>
```

### Query
```typescript
function Users() {
  const { data, isLoading, error } = useQuery({
    queryKey: ['users'],
    queryFn: fetchUsers,
    staleTime: 5 * 60 * 1000 // 5 minutes
  });

  if (isLoading) return <div>Loading...</div>;
  if (error) return <div>Error</div>;
  
  return <UserList users={data} />;
}
```

### Mutation
```typescript
function CreateUser() {
  const queryClient = useQueryClient();

  const mutation = useMutation({
    mutationFn: createUser,
    onSuccess: () => {
      queryClient.invalidateQueries({ queryKey: ['users'] });
    }
  });

  return <button onClick={() => mutation.mutate({ name: 'John' })}>Create</button>;
}
```

## Resources
- useQuery for GET
- useMutation for POST/PUT/DELETE
- Invalidate or update cache after mutations
