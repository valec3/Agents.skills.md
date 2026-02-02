---
name: frontend-data-fetching-strategy
description: Standardized guidelines and patterns for Frontend Data Fetching Strategy.
---

# Frontend Data Fetching Strategy

## When to use this skill
- Choosing data fetching approach
- Optimizing data loading
- Improving perceived performance

## Workflow
- [ ] Choose CSR vs SSR vs SSG
- [ ] Implement data fetching pattern
- [ ] Add loading states
- [ ] Handle errors
- [ ] Optimize with caching

## Instructions

### Strategies

**Client-Side Rendering (CSR)**
```typescript
function Users() {
  const { data } = useQuery('users', fetchUsers);
  return <UserList users={data} />;
}
```

**Server-Side Rendering (SSR)**
```typescript
// Next.js
export async function getServerSideProps() {
  const users = await fetchUsers();
  return { props: { users } };
}

export default function Page({ users }) {
  return <UserList users={users} />;
}
```

**Static Site Generation (SSG)**
```typescript
// Next.js
export async function getStaticProps() {
  const users = await fetchUsers();
  return { props: { users }, revalidate: 60 };
}
```

## Resources
- CSR: Dynamic data, authenticated
- SSR: SEO, real-time data
- SSG: Static content, best performance
