---
name: frontend-architecture-container-presentational
description: Standardized guidelines for separating smart (container) components from dumb (presentational) components. Use when building reusable, testable React components with clear separation of logic and UI.
---

# Frontend Architecture Container Presentational

## When to use this skill
- Building component libraries
- Need highly testable UI components
- Separating business logic from presentation
- Creating reusable design systems

## Workflow
- [ ] Identify which components handle logic vs display
- [ ] Create presentational components (pure UI)
- [ ] Create container components (logic + state)
- [ ] Connect containers to data sources
- [ ] Test presentational components in isolation

## Instructions

### Component Types

**Presentational Components**
- Focus on **how things look**
- Receive data via props
- No state management (usually)
- Highly reusable

**Container Components**
- Focus on **how things work**
- Manage state, side effects
- Connect to APIs, stores
- Render presentational components

### Example: User Profile

**Presentational Component**
```typescript
// components/UserProfile.tsx
interface UserProfileProps {
  name: string;
  email: string;
  avatarUrl: string;
  onEdit: () => void;
  isLoading?: boolean;
}

export function UserProfile({
  name,
  email,
  avatarUrl,
  onEdit,
  isLoading = false
}: UserProfileProps) {
  if (isLoading) {
    return <Skeleton />;
  }

  return (
    <div className="profile">
      <img src={avatarUrl} alt={name} />
      <h2>{name}</h2>
      <p>{email}</p>
      <button onClick={onEdit}>Edit Profile</button>
    </div>
  );
}
```

**Container Component**
```typescript
// containers/UserProfileContainer.tsx
import { UserProfile } from '../components/UserProfile';

export function UserProfileContainer({ userId }: { userId: string }) {
  const { data, isLoading } = useQuery(['user', userId], () => 
    fetchUser(userId)
  );
  const navigate = useNavigate();

  const handleEdit = () => {
    navigate(`/users/${userId}/edit`);
  };

  return (
    <UserProfile
      name={data?.name ?? ''}
      email={data?.email ?? ''}
      avatarUrl={data?.avatarUrl ?? ''}
      onEdit={handleEdit}
      isLoading={isLoading}
    />
  );
}
```

### Folder Structure

```
src/
├── components/           # Presentational
│   ├── Button.tsx
│   ├── Card.tsx
│   └── UserProfile.tsx
├── containers/           # Container
│   ├── UserProfileContainer.tsx
│   └── ProductListContainer.tsx
└── features/
    └── users/
        ├── components/   # Feature-specific presentational
        └── containers/   # Feature-specific containers
```

### Modern Alternative: Hooks

With hooks, you can extract logic without container components:

```typescript
// hooks/useUserProfile.ts
export function useUserProfile(userId: string) {
  const { data, isLoading } = useQuery(['user', userId], () => 
    fetchUser(userId)
  );
  const navigate = useNavigate();

  const handleEdit = () => {
    navigate(`/users/${userId}/edit`);
  };

  return {
    user: data,
    isLoading,
    handleEdit
  };
}

// components/UserProfile.tsx (Smart component with hook)
export function UserProfile({ userId }: { userId: string }) {
  const { user, isLoading, handleEdit } = useUserProfile(userId);

  if (isLoading) return <Skeleton />;
  if (!user) return null;

  return (
    <div className="profile">
      <img src={user.avatarUrl} alt={user.name} />
      <h2>{user.name}</h2>
      <button onClick={handleEdit}>Edit</button>
    </div>
  );
}
```

### When to Use Each

**Presentational Components:**
- Design system components
- Storybook documentation
- High reusability needed

**Container Components:**
- Legacy codebases
- Class components
- Complex orchestration

**Custom Hooks (Modern):**
- New React codebases
- Functional components
- Better composition

## Resources
- Presentational components are easy to test
- Containers handle complexity
- Hooks are the modern approach
