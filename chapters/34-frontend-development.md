# Chapter 34: Frontend Development

**Last Updated:** February 5, 2026

---

## Overview

Frontend development creates the user-facing layer of applications, combining visual design with interactive functionality. Modern frontend development requires expertise in frameworks, performance optimization, and user experience best practices.

This chapter covers essential frontend development skills for building modern, performant, and accessible web applications.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@react-expert` | React development | SPAs, component architecture |
| `@react-best-practices` | React best practices | Production quality |
| `@react-patterns` | React patterns | Design patterns |
| `@react-state-management` | React state | State management |
| `@react-ui-patterns` | React UI | UI patterns |
| `@react-modernization` | React upgrades | Legacy migration |
| `@vue-expert` | Vue.js development | Progressive apps, simpler apps |
| `@nextjs-expert` | Next.js development | SSR, full-stack React |
| `@nextjs-best-practices` | Next.js patterns | Best practices |
| `@nextjs-app-router-patterns` | App Router | Modern Next.js |
| `@nextjs-supabase-auth` | Auth patterns | Supabase + Next.js |
| `@angular` | Angular development | Enterprise SPAs |
| `@angular-best-practices` | Angular patterns | Best practices |
| `@angular-state-management` | Angular state | NgRx, signals |
| `@angular-ui-patterns` | Angular UI | UI components |
| `@angular-migration` | Angular upgrades | Version migration |
| `@css-expert` | CSS and styling | Layout, animations, responsive |
| `@tailwind-design-system` | Tailwind CSS | Utility-first CSS |
| `@tailwind-patterns` | Tailwind patterns | Common patterns |
| `@radix-ui-design-system` | Radix UI | Accessible components |
| `@remotion-best-practices` | Remotion | Video generation |
| `@scroll-experience` | Scroll effects | Scroll animations |
| `@canvas-design` | Canvas | Canvas graphics |

---

## 34.1 React Development with @react-expert

### Skill Introduction

The `@react-expert` skill provides expertise in React application development. It helps you build component-based applications with modern React patterns and best practices.

**When to use this skill:**
- Building single-page applications
- Component architecture design
- State management decisions
- React performance optimization

**Key strengths:**
- Deep React and hooks knowledge
- Experience with React ecosystem
- Understanding of rendering optimization

---

### React Development Prompts

#### Building a React Application

**Context:** You're building a new React application with modern best practices.

```text
@react-expert Design and implement a React application architecture:

Application:
- Dashboard application with multiple views
- Real-time data updates
- Complex forms with validation
- Data tables with sorting/filtering
- Charts and visualizations

Requirements:
- TypeScript throughout
- Modern state management (Zustand/Jotai/Redux Toolkit)
- Server state with TanStack Query
- Form handling with React Hook Form
- UI component library (Radix/Headless UI)
- Routing with React Router v6

Quality requirements:
- Component composition patterns
- Accessibility (WCAG 2.1 AA)
- Performance optimization
- Testing with Testing Library

Please provide:
1. Project structure
2. State management architecture
3. Component design patterns
4. Data fetching strategy
5. Form handling approach
6. Styling approach (CSS-in-JS, Tailwind, etc.)
7. Testing strategy
8. Build and deployment
```

**Expected Output:** React application architecture guide.

---

## 34.2 Vue.js Development with @vue-expert

### Skill Introduction

The `@vue-expert` skill provides expertise in Vue.js application development. It helps you build progressive applications with Vue's approachable and flexible framework.

**When to use this skill:**
- Building Vue.js applications
- Composition API patterns
- Vue ecosystem decisions
- Migration from Vue 2 to 3

**Key strengths:**
- Deep Vue 3 knowledge
- Experience with Composition API
- Understanding of Vue ecosystem

---

### Vue Development Prompts

#### Vue 3 Application Architecture

**Context:** You're building a new application with Vue 3.

```text
@vue-expert Design a Vue 3 application architecture:

Application:
- E-commerce storefront
- Product catalog with search
- Shopping cart functionality
- User authentication
- Order checkout flow

Requirements:
- Vue 3 with Composition API
- TypeScript integration
- Pinia for state management
- Vue Router for navigation
- API integration with error handling
- Form validation

Quality requirements:
- Composable patterns for reuse
- Component library consistency
- Performance optimization
- SSR with Nuxt 3 if appropriate

Please provide:
1. Project structure
2. Composable patterns
3. State management design
4. Routing architecture
5. API integration patterns
6. Error handling strategy
7. Testing approach
8. Build configuration
```

**Expected Output:** Vue 3 application architecture.

---

## 34.3 Next.js Development with @nextjs-expert

### Skill Introduction

The `@nextjs-expert` skill provides expertise in Next.js, the React framework for production. It helps you build full-stack applications with server-side rendering, API routes, and optimal performance.

**When to use this skill:**
- Server-side rendered applications
- Full-stack React applications
- Static site generation
- App Router architecture

**Key strengths:**
- Deep Next.js knowledge
- Experience with App Router
- Understanding of rendering strategies

---

### Next.js Development Prompts

#### Building Next.js Application

**Context:** You're building a production application with Next.js 14+.

```text
@nextjs-expert Design a Next.js application with App Router:

Application:
- SaaS landing page with marketing content
- Authentication and user dashboard
- API for mobile clients
- Admin panel for content management
- Subscription and billing

Requirements:
- Next.js 14 with App Router
- Server Components by default
- Server Actions for mutations
- Database with Prisma
- Authentication (NextAuth.js)
- Edge runtime where appropriate

Quality requirements:
- SEO optimization
- Core Web Vitals performance
- Incremental Static Regeneration
- Proper caching strategies

Please provide:
1. Route structure and organization
2. Server vs Client component decisions
3. Data fetching patterns
4. Server Actions implementation
5. Authentication architecture
6. Database integration
7. Middleware usage
8. Deployment (Vercel, self-hosted)
```

**Expected Output:** Next.js application architecture.

---

## 34.4 CSS and Styling with @css-expert

### Skill Introduction

The `@css-expert` skill provides expertise in CSS and styling approaches. It helps you create beautiful, responsive, and maintainable styles for web applications.

**When to use this skill:**
- Complex layouts and positioning
- Responsive design
- CSS animations and transitions
- Design system implementation

**Key strengths:**
- Deep CSS knowledge
- Experience with modern layout
- Understanding of CSS architecture

---

### CSS Styling Prompts

#### Implementing Design System

**Context:** You're implementing a design system with CSS.

```text
@css-expert Implement a CSS design system for our application:

Design requirements:
- Clean, modern aesthetic
- Dark and light mode support
- Responsive across all devices
- Smooth animations and transitions
- Consistent spacing and typography

Components to style:
- Buttons (primary, secondary, ghost)
- Form inputs (text, select, checkbox, radio)
- Cards and containers
- Navigation and menus
- Modal dialogs
- Toast notifications

Technical requirements:
- CSS custom properties for theming
- Utility classes for common patterns
- BEM or similar methodology
- Performance optimization
- Accessible contrast ratios

Please provide:
1. CSS architecture approach
2. Design tokens (colors, spacing, typography)
3. Theme switching implementation
4. Component style patterns
5. Responsive breakpoints
6. Animation patterns
7. Dark mode implementation
8. Performance considerations
```

**Expected Output:** CSS design system implementation.

---

## Best Practices Summary

### Component Design
1. **Composition:** Small, composable components
2. **Single Responsibility:** One purpose per component
3. **Props Interface:** Clear, typed props
4. **Accessibility:** ARIA and keyboard support
5. **Documentation:** Storybook or similar

### Performance
1. **Code Splitting:** Lazy load routes/components
2. **Bundle Size:** Monitor and optimize
3. **Rendering:** Avoid unnecessary re-renders
4. **Image Optimization:** Lazy loading, formats
5. **Core Web Vitals:** LCP, FID, CLS targets

### State Management
1. **Server State:** React Query/SWR for API data
2. **Local State:** Minimal, colocated
3. **Global State:** Only when necessary
4. **Form State:** Dedicated libraries
5. **URL State:** Use router for navigation state

---

## Reflection Points

1. **Framework Choice:** When React vs Vue vs other?
2. **SSR vs SPA:** How do you decide?
3. **Styling Approach:** CSS-in-JS vs Tailwind vs vanilla?
4. **Component Libraries:** Build vs buy?

---

**Next Chapter:** [Chapter 35: Mobile Development →](chapter-35-mobile-development.md)
