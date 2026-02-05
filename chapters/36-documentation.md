# Chapter 36: Documentation

**Last Updated:** February 5, 2026

---

## Overview

Documentation is a critical part of software development that enables knowledge sharing, onboarding, and long-term maintainability. Good documentation saves time, reduces errors, and makes systems more accessible.

This chapter covers essential documentation skills for creating effective technical documentation, API references, and developer guides.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@technical-writer` | Technical writing | Clear, effective documentation |
| `@api-docs-expert` | API documentation | OpenAPI, GraphQL docs |
| `@readme-expert` | README creation | Project documentation |
| `@docs-site-builder` | Documentation sites | Static site generators |

---

## 36.1 Technical Writing with @technical-writer

### Skill Introduction

The `@technical-writer` skill provides expertise in creating clear, effective technical documentation. It helps you write content that is accessible to its intended audience while maintaining technical accuracy.

**When to use this skill:**
- Writing technical guides
- Creating user manuals
- Improving existing documentation
- Documentation strategy

**Key strengths:**
- Clear technical communication
- Experience with documentation standards
- Understanding of audience needs

---

### Technical Writing Prompts

#### Creating Developer Documentation

**Context:** You need to create comprehensive documentation for your platform.

```text
@technical-writer Create developer documentation for our API platform:

Platform overview:
- REST and GraphQL APIs
- SDK for JavaScript, Python, Go
- Webhook integrations
- Authentication via OAuth 2.0
- Rate limiting and quotas

Target audience:
- External developers integrating our APIs
- Ranging from junior to senior
- Various programming backgrounds

Documentation needs:
- Getting started guide
- Authentication tutorial
- API reference
- SDK documentation
- Code examples for common use cases
- Troubleshooting guide

Please provide:
1. Documentation structure and organization
2. Writing style guide
3. Getting started guide template
4. API reference format
5. Code example patterns
6. Error message documentation
7. Maintenance strategy
8. Feedback collection
```

**Expected Output:** Developer documentation strategy and templates.

---

## 36.2 API Documentation with @api-docs-expert

### Skill Introduction

The `@api-docs-expert` skill provides expertise in documenting APIs effectively. It helps you create interactive, accurate API documentation that developers love.

**When to use this skill:**
- OpenAPI/Swagger documentation
- GraphQL documentation
- Interactive API playgrounds
- SDK documentation

**Key strengths:**
- Deep OpenAPI knowledge
- Experience with doc generators
- Understanding of API UX

---

### API Documentation Prompts

#### Creating OpenAPI Documentation

**Context:** You need to create comprehensive API documentation.

```text
@api-docs-expert Create OpenAPI documentation for our REST API:

API overview:
- 50+ endpoints across resources
- JWT authentication
- Pagination with cursor
- Complex filtering options
- Webhooks

Resources:
- Users, Organizations, Projects
- Tasks, Comments, Attachments
- Notifications, Webhooks

Requirements:
- Complete OpenAPI 3.1 spec
- Interactive documentation (Stoplight, Swagger UI)
- Code samples in multiple languages
- Clear error documentation
- Authentication flows documented

Please provide:
1. OpenAPI spec structure
2. Schema organization (components)
3. Authentication documentation
4. Pagination and filtering patterns
5. Error response schemas
6. Code sample generation
7. Tool recommendations
8. Versioning approach
```

**Expected Output:** OpenAPI documentation strategy.

---

## 36.3 README Creation with @readme-expert

### Skill Introduction

The `@readme-expert` skill provides expertise in creating effective README files. It helps you write READMEs that clearly communicate project purpose, setup, and usage.

**When to use this skill:**
- Creating project READMEs
- Open source documentation
- Repository documentation
- Internal project docs

**Key strengths:**
- README best practices
- Clear project communication
- Open source conventions

---

### README Prompts

#### Creating Project README

**Context:** You need to create a comprehensive README for an open-source project.

```text
@readme-expert Create a README for our open-source CLI tool:

Project:
- CLI tool for database migrations
- Supports PostgreSQL, MySQL, SQLite
- Written in Go
- Available via Homebrew, npm, and Go install
- Has configuration file and CLI options

Target audience:
- Developers using databases
- DevOps engineers
- Contributors to the project

README needs:
- Clear project description
- Quick start (under 5 minutes)
- Installation options
- Configuration reference
- Common use cases
- Troubleshooting
- Contributing guidelines

Please provide:
1. README structure and sections
2. Project badges to include
3. Quick start content
4. Installation instructions per platform
5. Usage examples
6. Configuration documentation
7. Contributing section
8. License and attribution
```

**Expected Output:** Complete README template.

---

## 36.4 Documentation Sites with @docs-site-builder

### Skill Introduction

The `@docs-site-builder` skill provides expertise in building documentation websites. It helps you create searchable, organized documentation using static site generators.

**When to use this skill:**
- Building documentation sites
- Choosing doc site frameworks
- Customizing doc site themes
- Search and navigation

**Key strengths:**
- Experience with doc frameworks
- Understanding of doc site UX
- Knowledge of search optimization

---

### Documentation Site Prompts

#### Building Documentation Site

**Context:** You need to build a documentation website for your product.

```text
@docs-site-builder Design and build a documentation site:

Requirements:
- 100+ pages of technical documentation
- Multi-version documentation support
- Full-text search
- Dark mode support
- API reference integration
- Self-hosted (not cloud service)

Content types:
- Guides and tutorials
- API reference
- CLI reference
- Configuration reference
- Changelog

Technical needs:
- Markdown authoring
- MDX for interactive components
- Automatic table of contents
- Mobile responsive
- Fast page loads

Please provide:
1. Framework recommendation (Docusaurus, Nextra, etc.)
2. Site structure and navigation
3. Multi-version implementation
4. Search configuration
5. Theme and styling approach
6. Build and deployment
7. Content contribution workflow
8. Analytics and feedback
```

**Expected Output:** Documentation site implementation plan.

---

## Best Practices Summary

### Content
1. **Audience Focus:** Know your reader
2. **Task-Oriented:** Focus on what users do
3. **Progressive Disclosure:** Simple to complex
4. **Examples:** Show, don't just tell
5. **Maintenance:** Keep docs current

### Organization
1. **Clear Structure:** Logical hierarchy
2. **Navigation:** Easy to find content
3. **Searchable:** Good search UX
4. **Versioning:** Match product versions
5. **Linking:** Cross-reference related content

### Quality
1. **Accuracy:** Technically correct
2. **Clarity:** Simple language
3. **Consistency:** Same terms throughout
4. **Completeness:** Cover all features
5. **Up-to-date:** Regular updates

---

## Reflection Points

1. **Docs as Product:** Should documentation be treated as a product?
2. **Who Writes:** Should developers write docs?
3. **Maintenance:** How do you keep docs current?
4. **Feedback:** How do you collect and act on feedback?

---

**Next Chapter:** [Chapter 37: Code Review →](chapter-37-code-review.md)
