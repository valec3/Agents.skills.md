---
name: frontend-seo-react
description: Standardized guidelines and patterns for Frontend Seo React.
---

# Frontend Seo React

## When to use this skill
- Optimizing for search engines
- Adding meta tags
- Structured data
- Server-side rendering for SEO

## Workflow
- [ ] Add meta tags
- [ ] Use react-helmet or Next.js Head
- [ ] Implement structured data
- [ ] Ensure proper heading hierarchy
- [ ] Create sitemap

## Instructions

### Meta Tags (Next.js)
```typescript
import Head from 'next/head';

<Head>
  <title>Page Title</title>
  <meta name="description" content="Page description" />
  <meta property="og:title" content="Social Title" />
  <meta property="og:description" content="Social description" />
  <meta property="og:image" content="/og-image.jpg" />
</Head>
```

### Structured Data
```typescript
<script type="application/ld+json">
  {JSON.stringify({
    "@context": "https://schema.org",
    "@type": "Article",
    "headline": "Title",
    "author": { "@type": "Person", "name": "Author" }
  })}
</script>
```

## Resources
- Use SSR for public pages
- Add Open Graph tags
- Implement structured data
- Create XML sitemap
