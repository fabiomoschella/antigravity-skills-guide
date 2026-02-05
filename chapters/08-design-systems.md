# Chapter 8: Design Systems & UI Architecture

**Last Updated:** February 5, 2026

---

## Overview

Design systems provide the foundation for consistent, scalable user interfaces. This chapter covers skills for creating and managing design systems, component libraries, and frontend architecture patterns to ensure your team builds faster with better consistency.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@design-system-architect` | Strategy & Structure | Planning, token architecture |
| `@component-library-expert` | Component Patterns | Reusable UI components |
| `@accessibility-expert` | WCAG Compliance | Inclusive design |
| `@design-tokens` | Token Management | Theming, multi-platform UI |
| `@storybook-expert` | Documentation | Component catalogs |

---

## 8.1 Design System Strategy with @design-system-architect

### Skill Introduction

The `@design-system-architect` skill provides high-level guidance on planning and scaling design systems. It focuses on governance, adoption strategies, and multi-brand architecture.

**When to use this skill:**
- Starting a new design system from scratch
- Auditing an existing system for scalability issues
- Planning multi-brand or multi-theme support
- Defining contribution workflows for teams
- Measuring design system adoption and ROI

**Key strengths:**
- Architectural strategy (Monolith vs Distributed)
- Governance models
- Adoption metrics
- Token architecture planning

---

### Design Strategy Prompts

#### Planning a Multi-Brand System

**Context:** You are creating a design system for a media company with 5 different publication brands.

```text
@design-system-architect Design a multi-brand architecture for our media company:

Scenario:
- 5 Brands (News, Sports, Lifestyle, Tech, Finance)
- Shared core functionality (Auth, Comments, Ads)
- Distinct visual identities (Typography, Color, Spacing)

Please provide:
1. Token Architecture strategy (Global tokens vs Brand aliases).
2. Component composition approach (Base components vs Branded wrappers).
3. Theme switching mechanism recommendation.
4. Folder structure for the monorepo.
```

**Expected Output:** A detailed architectural plan for managing multiple brands efficiently.

---

#### Defining Governance

**Context:** Your system is growing, and everyone is adding inconsistent components.

```text
@design-system-architect Create a Governance Model for our "Aurora" design system:

Team size: 20 Developers, 5 Designers.
Current state: Chaos. Duplicate components everywhere.

Please provide:
1. A Decision Tree for "When to create a new component".
2. The Contribution Workflow (Proposal -> Design Review -> Code Review).
3. Roles and Responsibilities (Who approves changes?).
4. Versioning Strategy (SemVer for UI components).
```

**Expected Output:** A governance playbook to maintain system integrity.

---

## 8.2 Component Library Design with @component-library-expert

### Skill Introduction

The `@component-library-expert` skill specializes in building robust, reusable React/Vue/Web Components. It enforces best practices like component composition, controlled vs uncontrolled state, and prop interface design.

**When to use this skill:**
- Designing the API for a complex component (e.g., Data Table)
- Refactoring huge "God Components" into smaller pieces
- Implementing compound component patterns
- Optimizing component performance
- Ensuring type safety with TypeScript

**Key strengths:**
- Component API design
- Composition patterns
- Performance optimization
- TypeScript integration

---

### Component Design Prompts

#### Designing a Compound Component

**Context:** You are building a flexible `Select` dropdown component.

```text
@component-library-expert Design the API for a "Compound Component" Select dropdown:

Goal: Maximum flexibility for consumers.
Requirements: Support labels, icons, groups, and search.

Proposed API structure (please critique and improve):
<Select>
  <Select.Trigger />
  <Select.Content>
    <Select.Item />
  </Select.Content>
</Select>

Please provide:
1. The refined API design using the Compound Pattern.
2. How to share state between children (Context API usage).
3. TypeScript interface definitions for the props.
```

**Expected Output:** A robust component API design with implementation details.

---

## 8.3 Accessibility with @accessibility-expert

### Skill Introduction

The `@accessibility-expert` skill ensures your UI is usable by everyone, including people using screen readers, keyboard-only navigation, or voice control. It targets WCAG 2.1/2.2 AA standards.

**When to use this skill:**
- auditing components for accessibility issues
- Implementing complex ARIA patterns (e.g., Combobox)
- Fixing color contrast violations
- Implementing keyboard navigation logic
- Testing with screen readers

**Key strengths:**
- WCAG compliance knowledge
- ARIA patterns and attributes
- Focus management
- Semantic HTML best practices

---

### Accessibility Prompts

#### Implementing an Accessible Modal

**Context:** You are building a custom Modal dialog from scratch.

```text
@accessibility-expert specific Guide me to build a fully accessible Modal dialog:

Requirements:
- Traps focus inside the modal when open.
- Returns focus to the trigger button when closed.
- Closes on ESC key.
- Closes on clicking the backdrop.
- Proper ARIA attributes (role="dialog", aria-modal="true", aria-labelledby).

Please provide:
1. The React hook logic for focus trapping.
2. The required ARIA attributes and where to put them.
3. A checklist for testing the implementation.
```

**Expected Output:** Implementation code for focus trapping and ARIA attributes.

---

#### Auditing a Form

**Context:** Users are complaining they can't submit your form using a keyboard.

```text
@accessibility-expert Audit this form markup for accessibility issues:

 Markup:
 <div onClick={submitForm}>Submit</div>
 <input placeholder="Enter name" />

 Critiques needed:
 1. Interactive elements needing keyboard support.
 2. Missing labels.
 3. Focus indication.
 4. Error message association (aria-describedby).
```

**Expected Output:** A list of critical accessibility fixes.

---

## 8.4 Design Tokens with @design-tokens

### Skill Introduction

The `@design-tokens` skill bridges the gap between design tools (Figma) and code. It manages the atomic visual values (colors, spacing, typography) that define your brand.

**When to use this skill:**
- Creating a new token taxonomy
- Automating token handoff from Figma
- Implementing Dark Mode
- Converting tokens to CSS Variables / Sass / iOS / Android
- Refactoring hardcoded values to tokens

**Key strengths:**
- Token taxonomy design
- Cross-platform format conversion (Style Dictionary)
- Theming architecture
- Semantic aliasing

---

### Design Token Prompts

#### Creating a Semantic Token Layer

**Context:** You have raw hex codes but want a flexible semantic system.

```text
@design-tokens Design a Semantic Token structure for our colors:

Primitives (Raw):
- Blue.500: #0000FF
- Red.500: #FF0000
- Gray.100: #F0F0F0

Goal: Create semantic aliases so we can change themes easily.

Please define semantic tokens for:
1. Primary Actions (Background, Hover, Text)
2. Destructive Actions
3. Surfaces (Background, Card, Modal)
4. Borders
5. Text (Primary, Secondary, Disabled)
```

**Expected Output:** A semantic JSON token structure mapping primitives to usage.

---

## 8.5 Documentation with @storybook-expert

### Skill Introduction

The `@storybook-expert` skill helps create living documentation for your UI. It focuses on writing better stories, automating documentation generation, and testing components in isolation.

**When to use this skill:**
- Setting up Storybook for a new project
- Writing interactive stories with Controls
- Documenting component edge cases
- Setting up visual regression testing
- Creating "Docs" pages with MDX

**Key strengths:**
- Storybook configuration
- MDX documentation
- Interactive controls setup
- Visual testing integration

---

### Storybook Prompts

#### Documenting a Complex Component

**Context:** You need to document a "DataGrid" component so other devs know how to use it.

```text
@storybook-expert specific Create a Storybook Story for our DataGrid component:

Features to demonstrate:
- Sorting
- Filtering
- Pagination
- Custom cell rendering

Please provide:
1. The Story file code (CSF format).
2. How to use args/controls to let users toggle features on/off.
3. An MDX description explaining the "renderCell" prop.
```

**Expected Output:** Complete Storybook configuration code for the component.

---

## Best Practices Summary

### Consistency First
- **Don't Invent:** Use existing components whenever possible.
- **Strict Tokens:** Hardcoded hex values are technical debt. Use tokens.
- **Single Source of Truth:** Code is the truth, but it should match Figma.

### Flexibility vs Rigidity
- **Composition over Configuration:** Avoid props like `isBigAndRedWithIcon`. Use composition instead.
- **Escape Hatches:** Allow className or style overrides for edge cases, but discourage them.

### Inclusion
- **Accessibility is not a Feature:** It's a requirement.
- **Keyboard First:** If you can't use it without a mouse, it's broken.

---

## Reflection Points

1. **Adoption:** Is your design system actually used, or do teams bypass it?
2. **Maintenance:** Who owns the system? Is it a side project or a product?
3. **Synchronization:** Is there a drift between Figma and Code? How to fix it?
4. **Performance:** Are you shipping the whole library or supporting tree-shaking?

---

**Next Chapter:** [Chapter 9: Workflow & Automation Architecture →](09-workflow-automation.md)
