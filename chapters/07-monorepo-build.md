# Chapter 7: Monorepo & Build Architecture

**Last Updated:** February 5, 2026

---

## Overview

Modern scalable development often relies on Monorepos (multiple projects in a single repository). This chapter covers the architectural skills needed to design, maintain, and optimize these complex environments using tools like Nx and Turborepo.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@monorepo-architect` | Strategy & Structure | Workspace organization |
| `@build-system-expert` | Performance | Caching, pipelines, CI |
| `@nx-expert` | Nx Tooling | Angular/React enterprise scale |
| `@turborepo-expert` | Turborepo Tooling | lightweight JS/TS scaling |
| `@dependency-manager` | Package Management | Versioning, compatibility |

---

## 7.1 Monorepo Strategy with @monorepo-architect

### Skill Introduction

The `@monorepo-architect` skill helps you design the layout, dependency boundaries, and sharing strategy of your workspace. It prevents the "Distributed Monolith" anti-pattern.

**When to use this skill:**
- Initializing a new monorepo
- Migrating from polyrepo to monorepo
- Designing shared library boundaries
- Setting up code visibility rules (constraints)
- Planning for independent deployability

**Key strengths:**
- Workspace organization
- Dependency graph design
- Code sharing strategy guidance
- Tool selection (Nx vs Turbo vs Bazel)

---

### Strategy Prompts

#### Planning Workspace Structure

**Context:** You are planning a monorepo for a SaaS with a Web App, Mobile App, and Shared UI/Logic.

```text
@monorepo-architect Design the folder structure for our new SaaS monorepo:

Apps:
1. `dashboard-web` (React)
2. `mobile-app` (React Native)
3. `marketing-site` (Next.js)

Goals:
- Maximize code sharing (UI components, API clients, Utils).
- Keep apps thin.

Please provide:
1. Ideally detailed folder structure (libs/ui, libs/data-access, etc.).
2. Dependency rules (e.g., UI cannot import Data Access).
3. Strategy for sharing types/interfaces.
```

**Expected Output:** A scalable directory tree and dependency boundary rules.

---

#### Migration Strategy

**Context:** You have 3 separate Git repos and want to merge them.

```text
@monorepo-architect Create a migration plan to move 3 separate repos into a single Monorepo:

Current State:
1. `frontend-repo` (Create React App)
2. `backend-repo` (Node/Express)
3. `component-library` (Rollup/NPM)

Please provide:
1. Step-by-step git merge process (preserving history).
2. How to handle CI/CD during the transition.
3. Strategy for "breaking" the existing internal NPM dependency.
```

**Expected Output:** A safe migration plan preserving git history and workflow continuity.

---

## 7.2 Build Performance with @build-system-expert

### Skill Introduction

The `@build-system-expert` skill optimizes the "Inner Loop" (local dev speed) and "Outer Loop" (CI speed). It focuses on caching, parallelization, and remote execution.

**When to use this skill:**
- Debugging slow CI builds
- Configuring remote caching (Nx Cloud / Vercel Remote Cache)
- Optimizing task graphs (Parallel execution)
- Reducing docker image sizes
- Implementing "Affected" commands

**Key strengths:**
- CI/CD pipeline optimization
- Caching strategies
- Task orchestration
- Pruning/Hashing logic

---

### Build System Prompts

#### Optimizing a Slow CI Pipeline

**Context:** Your CI currently takes 20 minutes because it builds everything every time.

```text
@build-system-expert Optimize our GitHub Actions pipeline for a Monorepo:

Current:
- Simple "npm install && npm test && npm build" script.
- Takes 20 minutes.

Goal: Use "Affected" logic to only build changed apps.

Please provide:
1. The logic/command to detect changes (using Nx or Turbo).
2. The GitHub Actions YAML snippet for parallel execution.
3. How to implement caching for `node_modules` and build artifacts.
```

**Expected Output:** Optimized CI configuration focusing on "Run Only What Changed".

---

## 7.3 Nx Mastery with @nx-expert

### Skill Introduction

The `@nx-expert` skill is specialized for the Nx build system. It covers generators, executors, module boundaries, and deep Angular/React integration.

**When to use this skill:**
- Creating custom Nx Generators (scaffolding)
- Configuring `project.json` targets
- Setting up Module Boundary Linting roles
- Debugging cyclic dependencies
- Migrating to "Standalone" mode

**Key strengths:**
- Nx CLI mastery
- Generator creation
- Custom Executor implementation
- Graph visualization

---

### Nx Prompts

#### Creating a Scaffolding Generator

**Context:** You want every new feature library to look exactly the same.

```text
@nx-expert detailed Help me create a custom Nx Generator for a "Feature Library":

Requirements:
- Takes a name (e.g., `user-profile`).
- Creates a `data-access` lib and a `feature-ui` lib.
- Updates the parent App's routing automatically.

Please provide:
1. The CLI command to generate the generator.
2. The implementation logic (schema.json and generator.ts).
3. How to test this generator locally.
```

**Expected Output:** Code for a custom Nx generator to standardize library creation.

---

## 7.4 Turborepo Mastery with @turborepo-expert

### Skill Introduction

The `@turborepo-expert` skill focuses on the Vercel ecosystem's build tool. It emphasizes simplicity, configuration via `turbo.json`, and handling environment variables.

**When to use this skill:**
- optimizing a Yarn/npm/pnpm workspace
- Configuring complex task dependencies (Topo-sort)
- Managing Environment Variables in cached builds
- Pruning builds for Docker deployment

**Key strengths:**
- pipeline configuration
- Remote cache setup
- Docker container pruning
- Variable dependency management

---

### Turborepo Prompts

#### Docker Entrypoint Optimization

**Context:** You are deploying a Next.js app from a Turborepo to Docker. The image is huge.

```text
@turborepo-expert detailed Guide me to create an optimized Dockerfile using `turbo prune`:

App: `apps/web`
PackageManager: `pnpm`

Goal: A minimal production image containing only necessary dependencies for `web`.

Please provide:
1. The `turbo prune` command.
2. The multi-stage Dockerfile (Builder stage vs Runner stage).
3. How to handle `lockfile` consistency.
```

**Expected Output:** An optimized multi-stage Dockerfile using turbo pruning.

---

## Best Practices Summary

### Architecture
- **Libs > Apps:** Keep apps as thin containers. Move logic to libraries.
- **Strict Boundaries:** Enforce rules (e.g., "UI cannot import Data"). Use `eslint-plugin-nx` or similar.

### Performance
- **Cache Everything:** If you run it twice, the second time should be instant.
- **Parallelize:** Don't run tests sequentially if they don't depend on each other.

### Developer Experience
- **Single Command Start:** A new dev should run `npm start` and see the whole system.
- **Scaffold:** Don't let devs Copy-Paste folders. Use generators.

---

## Reflection Points

1. **Complexity Cost:** Is the tooling overhead worth it for your team size?
2. **Ghost Dependencies:** Are you relying on hoisted packages that aren't in your `package.json`?
3. **CI Bottlenecks:** Is the limitation CPU or Network/IO?
4. **Onboarding:** How long does it take a new hire to understand the workspace map?

---

**Next Chapter:** [Chapter 8: Design Systems & UI Architecture →](08-design-systems.md)
