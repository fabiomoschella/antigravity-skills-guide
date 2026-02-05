# Chapter 10: SEO & Content Marketing

**Last Updated:** February 5, 2026

---

## Overview

Search Engine Optimization (SEO) and content marketing are the engines of organic growth. This chapter covers skills for technical optimization, content strategy, keyword research, and authority building to ensure your content reaches its intended audience.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@seo-expert` | Technical & On-page SEO | Site audits, optimization |
| `@content-strategist` | Content planning | Editorial calendars, pillars |
| `@seo-content-writer` | Optimization writing | Blog posts, landing pages |
| `@keyword-researcher` | Keyword discovery | Finding ranking opportunities |
| `@programmatic-seo` | Scalable content | Large-scale page generation |
| `@link-building-expert` | Off-page SEO | Authority, outreach |

---

## 10.1 Technical & On-Page SEO with @seo-expert

### Skill Introduction

The `@seo-expert` skill provides comprehensive guidance on technical SEO foundation and on-page optimization. It helps diagnose crawling issues, optimize site structure, and implement schema markup for better visibility.

**When to use this skill:**
- Conducting a technical site audit
- Optimizing meta tags (Title, Description)
- Implementing structured data (Schema.org)
- Fixing Core Web Vitals issues
- Planning site architecture and internal linking

**Key strengths:**
- Technical diagnostics (indexing, canonicals)
- On-page optimization checklists
- Schema markup generation
- Core Web Vitals optimization

---

### SEO Prompts

#### Conducting a Technical Audit

**Context:** You noticed a drop in organic traffic and suspect technical issues.

```text
@seo-expert Conduct a technical SEO audit plan for our SaaS website:

Symptoms:
- Traffic dropped 15% last month
- "Crawled - currently not indexed" errors increasing in Search Console
- Site speed feels slow on mobile

Tech Stack: Next.js hosted on Vercel.

Please provide:
1. A checklist of technical elements to investigate (Robots.txt, Sitemap, Canonical tags).
2. How to debug the indexing issue specifically.
3. Core Web Vitals assessment plan (LCP, CLS, INP).
4. Tools recommended for the diagnosis.
```

**Expected Output:** A prioritized audit checklist and debugging steps for the indexing and speed issues.

---

#### Optimizing Schema Markup

**Context:** You want your product pages to show price and ratings in search results (Rich Snippets).

```text
@seo-expert Generate JSON-LD Schema markup for our product page:

Product: "ErgoChair Pro"
Price: $399.00
Currency: USD
Availability: In Stock
Rating: 4.8 (based on 150 reviews)
Description: "The ultimate ergonomic office chair for remote work."
Image URL: "https://example.com/ergochair.jpg"

Please provide:
1. Valid JSON-LD code block.
2. Where to place it in the HTML/Next.js head.
3. How to test if Google can read it.
```

**Expected Output:** Ready-to-copy JSON-LD code and implementation instructions.

---

## 10.2 Content Strategy with @content-strategist

### Skill Introduction

The `@content-strategist` skill helps you plan, organize, and execute a content marketing strategy. It focuses on topical authority, content pillars, and mapping content to the buyer's journey.

**When to use this skill:**
- Developing a quarterly editorial calendar
- Defining content pillars and topic clusters
- Conducting a content gap analysis
- Creating buyer personas for content
- Repurposing content strategies

**Key strengths:**
- Topic cluster strategy (Hub & Spoke)
- Buyer journey mapping (Awareness, Consideration, Decision)
- Editorial planning
- Content audit frameworks

---

### Content Strategy Prompts

#### Developing Topic Clusters

**Context:** You want to build authority in the "Remote Team Management" niche.

```text
@content-strategist Design a Topic Cluster strategy for "Remote Team Management":

Pillar Page: "The Ultimate Guide to Managing Remote Teams"

Goal: Rank for broad terms and capture long-tail traffic.

Please provide:
1. The Pillar Page structure (H2 topics).
2. 10 related "Cluster Content" ideas (Blog posts) that link back to the pillar.
3. User intent for each cluster topic (Informational vs Transactional).
4. Internal linking strategy between them.
```

**Expected Output:** A structured content plan with a central pillar and supporting satellite articles.

---

#### Content Gap Analysis

**Context:** Your competitor is outranking you. You need to find what they are writing that you aren't.

```text
@content-strategist Guide me through a Content Gap Analysis:

My Site: [MySaaS.com]
Key Competitor: [CompetitorSaaS.com]

Goal: Identify high-value topics they cover that I'm missing.

Please provide:
1. The process/tools to identify gaps.
2. Criteria for prioritizing which gaps to fill first (Volume vs Difficulty).
3. A template for a content brief to give to writers to fill these gaps.
```

**Expected Output:** A step-by-step process for finding and exploiting content gaps.

---

## 10.3 SEO Content Writing with @seo-content-writer

### Skill Introduction

The `@seo-content-writer` skill is specialized in creating content that appeals to both humans and search engines. It balances keyword usage with readability, engagement, and conversion optimization.

**When to use this skill:**
- Writing blog posts optimized for specific keywords
- Creating landing page copy
- Optimizing existing articles to rank higher
- Writing compelling meta titles and descriptions
- Structuring articles for featured snippets

**Key strengths:**
- Keyword integration (Primary + LSI)
- Readability optimization
- Search intent alignment
- Featured snippet optimization

---

### Content Writing Prompts

#### Writing an Optimized Blog Post Outline

**Context:** You are writing a post targeting the keyword "Best AI Coding Tools 2026".

```text
@seo-content-writer Create an SEO-optimized outline for "Best AI Coding Tools 2026":

Target Keyword: "Best AI Coding Tools"
Secondary Keywords: "AI code assistant", "coding copilot", "developer productivity"
Target Length: 2000 words
Audience: Senior Developers and CTOs

Please provide:
1. Optimized H1 Title (high CTR).
2. Detailed H2 and H3 structure.
3. Where to place primary and secondary keywords.
4. "Key Takeaways" section for Featured Snippet optimization.
5. Internal link suggestions.
```

**Expected Output:** A detailed content outline ready for drafting.

---

#### Optimizing for Featured Snippets

**Context:** You rank #4 for "How to optimize React performance" and want to capture "Position Zero" (the snippet).

```text
@seo-content-writer Optimize a paragraph to capture the Featured Snippet for "How to optimize React performance":

Current Content: "There are many ways to make React faster. You should look at memoization and also aggressive code splitting..." (It's too vague).

Requirement:
- Clear, direct answer.
- Definition style or list style.
- 40-60 words optimal length.

Please provide:
1. The optimized paragraph/list.
2. HTML formatting advice (e.g., use <li> tags?).
```

**Expected Output:** A snippet-optimized text block designed to answer the user's query instantly.

---

## 10.4 Keyword Research with @keyword-researcher

### Skill Introduction

The `@keyword-researcher` skill helps validte content ideas by analyzing search volume, difficulty, and intent. It ensures you don't waste time writing about things nobody is searching for.

**When to use this skill:**
- Finding low-competition, high-volume keywords
- Analyzing search intent (Navigational, Informational, Transactional)
- Discovering long-tail keyword opportunities
- Validating product naming ideas
- Seasonal trend analysis

**Key strengths:**
- Search volume vs difficulty analysis
- Intent classification
- Long-tail discovery
- Competitor keyword analysis

---

### Keyword Research Prompts

#### Finding Low-Hanging Fruit

**Context:** You have a new domain (low authority) and need keywords you can actually rank for.

```text
@keyword-researcher Help me find "low-hanging fruit" keywords for a new coffee blog:

Niche: Specialty Coffee / Home Brewing.
Constraint: Domain Authority (DA) is low (10). Can't compete for "coffee beans".

Please provide:
1. A strategy to find low-difficulty (KD < 20) long-tail keywords.
2. 5 example keyword patterns (e.g., "best coffee for [specific machine]").
3. How to validte if the SERP is "weak" (e.g., forums ranking on page 1).
```

**Expected Output:** A strategy for finding accessible keywords and specific examples.

---

## Best Practices Summary

### User Experience is SEO
- **Speed Matters:** Google penalizes slow sites. Optimize images and scripts.
- **Engagement Signals:** Dwell time and bounce rate matter. Write engaging intros.
- **Mobile First:** Most indexing is mobile-first. Ensure your mobile UX is flawless.

### Content Quality
- **E-E-A-T:** Experience, Expertise, Authoritativeness, Trustworthiness. Show your credentials.
- **Uniqueness:** Don't just rewrite the top result. Add new data, a unique angle, or personal experience.
- **Freshness:** Update old content regularly. Current year in title helps CTR.

### Ethics
- **White Hat Only:** Avoid buying links or keyword stuffing. It works short term, but kills you long term.
- **Focus on the User:** If it helps the user, it usually helps SEO.

---

## Reflection Points

1. **Search Intent:** Are you trying to sell on a "How to" keyword? (Mismatched intent).
2. **Authority:** Are you staying in your lane (topical authority) or writing about everything?
3. **Patience:** SEO is a marathon. Are you tracking progress over months, not days?
4. **Diversification:** Do you rely 100% on Google? What if an algorithm update hits?

---

**Next Chapter:** [Chapter 11: Copywriting & Content Creation →](11-copywriting.md)
