---
name: frontend-data-api-layer
description: Standardized guidelines and patterns for Frontend Data Api Layer.
---

# Frontend Data Api Layer

## When to use this skill
- Abstracting API calls
- Centralizing API logic
- Type-safe API layer

## Workflow
- [ ] Create API client
- [ ] Define API methods
- [ ] Handle errors centrally
- [ ] Type request/response
- [ ] Add interceptors

## Instructions

### API Client
```typescript
// api/client.ts
import axios from 'axios';

export const apiClient = axios.create({
  baseURL: import.meta.env.VITE_API_URL,
  headers: {
    'Content-Type': 'application/json'
  }
});

apiClient.interceptors.request.use((config) => {
  const token = localStorage.getItem('token');
  if (token) config.headers.Authorization = `Bearer ${token}`;
  return config;
});
```

### API Methods
```typescript
// api/users.ts
export const usersApi = {
  getAll: () => apiClient.get<User[]>('/users'),
  getById: (id: string) => apiClient.get<User>(`/users/${id}`),
  create: (data: CreateUserDto) => apiClient.post<User>('/users', data),
  update: (id: string, data: UpdateUserDto) => 
    apiClient.put<User>(`/users/${id}`, data),
  delete: (id: string) => apiClient.delete(`/users/${id}`)
};
```

## Resources
- Centralize all API calls
- Type request/response
- Handle auth in interceptors
