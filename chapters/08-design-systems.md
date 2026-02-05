# Chapter 8: Design Systems & UI Architecture

**Last Updated:** February 5, 2026

---

## Overview

Design systems provide the foundation for consistent, scalable user interfaces. This chapter covers skills for creating and managing design systems, component libraries, and frontend architecture patterns.

### Skills Covered in This Chapter

| Skill | Source | Purpose |
|-------|--------|---------|
| `design-system-architect` | Unknown | Design system strategy |
| `component-library-expert` | Unknown | Component design patterns |
| `accessibility-expert` | Unknown | Accessibility implementation |
| `design-tokens` | Unknown | Token management |
| `storybook-expert` | Unknown | Component documentation |

---

## 8.1 Design System Architecture

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: design-system, ui, architecture

### Purpose

The `design-system-architect` skill provides guidance on building scalable design systems that ensure consistency across products.

### Design System Layers

```
┌─────────────────────────────────────────┐
│           Application Layer              │
│    (Product-specific components)         │
├─────────────────────────────────────────┤
│           Pattern Library                │
│    (Composed UI patterns)                │
├─────────────────────────────────────────┤
│          Component Library               │
│    (Reusable UI components)              │
├─────────────────────────────────────────┤
│           Design Tokens                  │
│    (Colors, spacing, typography)         │
├─────────────────────────────────────────┤
│          Design Principles               │
│    (Guidelines and standards)            │
└─────────────────────────────────────────┘
```

### 40 Copy-Paste Prompts

#### Strategy and Planning

```
1. "Use @design-system-architect to create a design system strategy for our organization"

2. "Apply @design-system-architect to audit our current component fragmentation"

3. "Use @design-system-architect to plan the design system adoption roadmap"

4. "Apply @design-system-architect to define governance for the design system"

5. "Use @design-system-architect to plan multi-brand support"

6. "Apply @design-system-architect to design theming architecture"

7. "Use @design-system-architect to create versioning strategy"

8. "Apply @design-system-architect to plan documentation approach"

9. "Use @design-system-architect to design contribution workflow"

10. "Apply @design-system-architect to create adoption metrics"
```

#### Token Design

```
11. "Use @design-system-architect to define the color token hierarchy"

12. "Apply @design-system-architect to create spacing scale tokens"

13. "Use @design-system-architect to design typography tokens"

14. "Apply @design-system-architect to create shadow tokens"

15. "Use @design-system-architect to design animation tokens"

16. "Apply @design-system-architect to create breakpoint tokens"

17. "Use @design-system-architect to design border and radius tokens"

18. "Apply @design-system-architect to create semantic tokens"

19. "Use @design-system-architect to design dark mode tokens"

20. "Apply @design-system-architect to create token naming conventions"
```

#### Component Architecture

```
21. "Use @design-system-architect to design the component API standards"

22. "Apply @design-system-architect to create component composition patterns"

23. "Use @design-system-architect to design prop interfaces"

24. "Apply @design-system-architect to create variant systems"

25. "Use @design-system-architect to design compound components"

26. "Apply @design-system-architect to create polymorphic components"

27. "Use @design-system-architect to design controlled vs uncontrolled patterns"

28. "Apply @design-system-architect to create accessibility patterns"

29. "Use @design-system-architect to design animation patterns"

30. "Apply @design-system-architect to create responsive patterns"
```

#### Distribution

```
31. "Use @design-system-architect to design the package structure"

32. "Apply @design-system-architect to create tree-shakable exports"

33. "Use @design-system-architect to design CSS delivery strategy"

34. "Apply @design-system-architect to create SSR compatibility"

35. "Use @design-system-architect to design versioning and changelog"

36. "Apply @design-system-architect to create migration scripts"

37. "Use @design-system-architect to design bundle size optimization"

38. "Apply @design-system-architect to create test utilities"

39. "Use @design-system-architect to design dev tooling"

40. "Apply @design-system-architect to create CDN distribution"
```

---

## 8.2 Component Library Design

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: components, ui, patterns

### Purpose

The `component-library-expert` skill provides patterns for building reusable, accessible components.

### Component Categories

| Category | Examples | Complexity |
|----------|----------|------------|
| **Primitives** | Button, Input, Text | Low |
| **Compound** | Select, Dropdown, Tabs | Medium |
| **Layout** | Grid, Stack, Container | Low |
| **Feedback** | Toast, Modal, Alert | Medium |
| **Navigation** | Menu, Breadcrumb, Pagination | Medium |
| **Data Display** | Table, Card, List | High |
| **Forms** | Form, Validation, Field | High |

### 30 Copy-Paste Prompts

#### Core Components

```
41. "Use @component-library-expert to design a Button component with variants"

42. "Apply @component-library-expert to create an Input component with validation"

43. "Use @component-library-expert to design a Select component"

44. "Apply @component-library-expert to create a Modal component"

45. "Use @component-library-expert to design a Tabs component"

46. "Apply @component-library-expert to create a Dropdown component"

47. "Use @component-library-expert to design a Toast notification system"

48. "Apply @component-library-expert to create a Table component"

49. "Use @component-library-expert to design a Form component with validation"

50. "Apply @component-library-expert to create a Card component"
```

#### Advanced Patterns

```
51. "Use @component-library-expert to implement render props pattern"

52. "Apply @component-library-expert to create compound component pattern"

53. "Use @component-library-expert to implement slot-based composition"

54. "Apply @component-library-expert to create headless UI pattern"

55. "Use @component-library-expert to implement controlled pattern"

56. "Apply @component-library-expert to create polymorphic 'as' prop"

57. "Use @component-library-expert to implement context-based components"

58. "Apply @component-library-expert to create forwarded refs pattern"

59. "Use @component-library-expert to implement portal pattern"

60. "Apply @component-library-expert to create focus management"
```

#### Testing Components

```
61. "Use @component-library-expert to create component unit tests"

62. "Apply @component-library-expert to implement visual regression tests"

63. "Use @component-library-expert to create accessibility tests"

64. "Apply @component-library-expert to implement interaction tests"

65. "Use @component-library-expert to create snapshot tests"
```

---

## 8.3 Accessibility Implementation

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: a11y, accessibility, wcag

### Purpose

The `accessibility-expert` skill ensures components meet WCAG guidelines and are usable by everyone.

### WCAG Levels

| Level | Description | Coverage |
|-------|-------------|----------|
| **A** | Minimum accessibility | Essential |
| **AA** | Standard compliance | Recommended |
| **AAA** | Enhanced accessibility | Optimal |

### 20 Copy-Paste Prompts

```
66. "Use @accessibility-expert to audit this component for WCAG AA compliance"

67. "Apply @accessibility-expert to implement keyboard navigation"

68. "Use @accessibility-expert to create screen reader announcements"

69. "Apply @accessibility-expert to design focus indicators"

70. "Use @accessibility-expert to implement ARIA attributes"

71. "Apply @accessibility-expert to create accessible form errors"

72. "Use @accessibility-expert to design color contrast compliance"

73. "Apply @accessibility-expert to implement skip navigation"

74. "Use @accessibility-expert to create accessible modals"

75. "Apply @accessibility-expert to design accessible data tables"

76. "Use @accessibility-expert to implement reduced motion support"

77. "Apply @accessibility-expert to create accessible tooltips"

78. "Use @accessibility-expert to design accessible dropdown menus"

79. "Apply @accessibility-expert to implement live regions"

80. "Use @accessibility-expert to create focus trap for modals"
```

---

## 8.4 Design Tokens Management

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: tokens, css, theming

### Purpose

The `design-tokens` skill provides patterns for managing design decisions as data.

### Token Structure

```json
{
  "color": {
    "brand": {
      "primary": { "value": "#0066CC" },
      "secondary": { "value": "#FF6600" }
    },
    "semantic": {
      "success": { "value": "{color.green.500}" },
      "error": { "value": "{color.red.500}" },
      "warning": { "value": "{color.yellow.500}" }
    }
  },
  "spacing": {
    "xs": { "value": "4px" },
    "sm": { "value": "8px" },
    "md": { "value": "16px" },
    "lg": { "value": "24px" },
    "xl": { "value": "32px" }
  },
  "typography": {
    "heading": {
      "fontFamily": { "value": "Inter, sans-serif" },
      "fontWeight": { "value": "600" }
    }
  }
}
```

### 10 Copy-Paste Prompts

```
81. "Use @design-tokens to create a token structure for our design system"

82. "Apply @design-tokens to implement token transformation pipeline"

83. "Use @design-tokens to create CSS custom properties from tokens"

84. "Apply @design-tokens to generate TypeScript types for tokens"

85. "Use @design-tokens to implement token theming"

86. "Apply @design-tokens to create token documentation"

87. "Use @design-tokens to implement token synchronization with Figma"

88. "Apply @design-tokens to create token validation"

89. "Use @design-tokens to implement token versioning"

90. "Apply @design-tokens to create multi-platform token outputs"
```

---

## 8.5 Storybook Documentation

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: storybook, documentation, components

### Purpose

The `storybook-expert` skill provides guidance on documenting components with Storybook.

### 10 Copy-Paste Prompts

```
91. "Use @storybook-expert to configure Storybook for our design system"

92. "Apply @storybook-expert to create component stories with controls"

93. "Use @storybook-expert to implement MDX documentation"

94. "Apply @storybook-expert to create interaction tests"

95. "Use @storybook-expert to configure visual regression with Chromatic"

96. "Apply @storybook-expert to implement accessibility addon"

97. "Use @storybook-expert to create design tokens addon"

98. "Apply @storybook-expert to implement responsive viewports"

99. "Use @storybook-expert to create component playground"

100. "Apply @storybook-expert to implement theme switcher"
```

---

## Design System Component Template

```tsx
// Button.tsx
import { forwardRef } from 'react';
import { clsx } from 'clsx';
import styles from './Button.module.css';

export interface ButtonProps extends React.ButtonHTMLAttributes<HTMLButtonElement> {
  /** Visual variant of the button */
  variant?: 'primary' | 'secondary' | 'ghost';
  /** Size of the button */
  size?: 'sm' | 'md' | 'lg';
  /** Whether the button is in loading state */
  loading?: boolean;
  /** Full width button */
  fullWidth?: boolean;
}

export const Button = forwardRef<HTMLButtonElement, ButtonProps>(
  (
    {
      variant = 'primary',
      size = 'md',
      loading = false,
      fullWidth = false,
      disabled,
      className,
      children,
      ...props
    },
    ref
  ) => {
    return (
      <button
        ref={ref}
        className={clsx(
          styles.button,
          styles[variant],
          styles[size],
          fullWidth && styles.fullWidth,
          loading && styles.loading,
          className
        )}
        disabled={disabled || loading}
        aria-busy={loading}
        {...props}
      >
        {loading && <span className={styles.spinner} aria-hidden />}
        <span className={clsx(loading && styles.hiddenText)}>{children}</span>
      </button>
    );
  }
);

Button.displayName = 'Button';
```

---

## Best Practices

### 1. Component API Design

```tsx
// ✅ Good: Clear, typed props with defaults
interface ButtonProps {
  variant?: 'primary' | 'secondary';
  size?: 'sm' | 'md' | 'lg';
  disabled?: boolean;
}

// ❌ Bad: Unclear, stringly-typed
interface ButtonProps {
  type?: string;
  big?: boolean;
}
```

### 2. Token Usage

```css
/* ✅ Good: Use tokens */
.button {
  padding: var(--spacing-md);
  color: var(--color-text-primary);
  border-radius: var(--radius-md);
}

/* ❌ Bad: Hardcoded values */
.button {
  padding: 16px;
  color: #333333;
  border-radius: 8px;
}
```

### 3. Accessibility First

- Always include focus styles
- Use semantic HTML elements
- Support keyboard navigation
- Test with screen readers

### 4. Documentation

Every component needs:
- Purpose description
- Prop documentation
- Usage examples
- Accessibility notes

---

## Reflection Points for Chapter 8

1. **What's the current state of UI consistency in your organization?**
   - Component fragmentation?
   - Duplicate implementations?

2. **How do you handle theming and customization?**
   - Multi-brand support?
   - Dark mode?

3. **What's your accessibility compliance level?**
   - WCAG targets?
   - Testing strategy?

4. **How do you document components?**
   - Storybook?
   - Living documentation?

---

## Summary

This chapter covered design systems and UI architecture:

- **@design-system-architect**: Strategy and structure
- **@component-library-expert**: Component patterns
- **@accessibility-expert**: WCAG compliance
- **@design-tokens**: Token management
- **@storybook-expert**: Documentation

**Key Takeaway**: A well-designed design system is an investment that pays dividends in consistency, quality, and developer productivity.

---

**Next Chapter**: [Chapter 9: Workflow & Automation Architecture →](chapter-09-workflow-automation.md)
