# Chapter 45: Search & Discovery

**Last Updated:** February 5, 2026

---

## Overview

Search and discovery systems are critical for helping users find relevant information within large datasets. From product catalogs to document repositories, effective search requires understanding of text analysis, relevance ranking, and user behavior optimization.

This chapter covers essential skills for building powerful, accurate search experiences that delight users.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@elasticsearch-expert` | Elasticsearch mastery | Full-text search, analytics |
| `@search-architect` | Search system design | Enterprise search |
| `@relevance-engineer` | Search relevance | Ranking optimization |
| `@autocomplete-expert` | Typeahead systems | Suggestions, autocomplete |

---

## 45.1 Elasticsearch Development with @elasticsearch-expert

### Skill Introduction

The `@elasticsearch-expert` skill provides deep expertise in Elasticsearch for building search solutions. It helps you design indices, write queries, and optimize performance for large-scale search applications.

**When to use this skill:**
- Building full-text search functionality
- Product catalog search
- Log and event analytics
- Real-time search applications

**Key strengths:**
- Deep Elasticsearch knowledge
- Experience with query DSL and aggregations
- Understanding of text analysis and relevance

---

### Elasticsearch Prompts

#### Designing E-commerce Search

**Context:** You're building search for an e-commerce platform with millions of products.

```text
@elasticsearch-expert Design a comprehensive e-commerce search system:

Catalog details:
- 1 million products across 500 categories
- Multi-language content (English, Spanish, German)
- Product attributes vary by category
- Frequent inventory updates
- Real-time pricing changes

Search requirements:
- Full-text search across titles, descriptions, attributes
- Faceted navigation (category, brand, price, ratings)
- Autocomplete with product suggestions
- Typo tolerance and fuzzy matching
- Synonym handling (laptop = notebook)
- Boosting for featured products
- Personalization based on user history

Performance targets:
- Search latency < 50ms at p99
- 1000 searches per second
- Real-time inventory updates

Please provide:
1. Index design and mapping strategy
2. Text analysis configuration (analyzers, tokenizers)
3. Query structure for search and filters
4. Facet aggregation design
5. Autocomplete implementation
6. Relevance tuning approach
7. Indexing pipeline with real-time updates
8. Cluster sizing and scaling strategy
```

**Expected Output:** Complete Elasticsearch architecture for e-commerce.

---

#### Building Log Analytics Platform

**Context:** You need to build a centralized logging and analytics platform.

```text
@elasticsearch-expert Design log analytics with Elasticsearch:

Log sources:
- Application logs (JSON structured)
- Web server access logs
- Infrastructure metrics
- Security audit logs
- 500GB of logs per day

Requirements:
- Real-time log ingestion
- Full-text search across all logs
- Time-based queries and visualizations
- Alerting on patterns and anomalies
- 30-day retention with roll-up for older data
- Multi-tenancy (separate teams)

Operational needs:
- High availability (no single point of failure)
- Backup and recovery
- Index lifecycle management
- Cost optimization

Please provide:
1. Index patterns and lifecycle policies
2. Ingest pipeline configuration
3. Mapping optimization for logs
4. Query patterns for common use cases
5. Kibana dashboard recommendations
6. Alerting configuration
7. Cluster architecture for HA
8. Cost optimization strategies
```

**Expected Output:** Log analytics platform design.

---

## 45.2 Search Architecture with @search-architect

### Skill Introduction

The `@search-architect` skill provides expertise in designing enterprise search systems. It helps you architect scalable, maintainable search platforms that integrate multiple data sources.

**When to use this skill:**
- Designing enterprise search platforms
- Multi-source search federation
- Search infrastructure decisions
- Search technology selection

**Key strengths:**
- System design for search
- Experience with search technologies
- Understanding of search UX patterns

---

### Search Architecture Prompts

#### Designing Enterprise Knowledge Search

**Context:** You're building an enterprise search platform that unifies multiple data sources.

```text
@search-architect Design enterprise knowledge search platform:

Data sources to search:
- SharePoint documents (50K docs)
- Confluence wikis (20K pages)
- Jira tickets (100K issues)
- Slack messages (archived)
- Email archives
- Database records

Requirements:
- Unified search across all sources
- Access control respecting source permissions
- Real-time and batch indexing
- Natural language understanding
- Federated search with result merging
- Search analytics and insights

User needs:
- 5000 internal users
- Executives want simple Google-like search
- Power users need advanced filtering
- Mobile access required

Please provide:
1. Overall architecture design
2. Connector and ingestion strategy
3. Index design for heterogeneous content
4. Access control implementation
5. Query federation approach
6. Result ranking across sources
7. Technology stack recommendations
8. Scalability and performance considerations
```

**Expected Output:** Enterprise search platform architecture.

---

## 45.3 Relevance Engineering with @relevance-engineer

### Skill Introduction

The `@relevance-engineer` skill provides expertise in optimizing search relevance. It helps you tune ranking algorithms, measure relevance quality, and continuously improve search results.

**When to use this skill:**
- Improving search result quality
- Implementing learning-to-rank
- A/B testing search changes
- Building relevance evaluation systems

**Key strengths:**
- Relevance tuning expertise
- Machine learning for ranking
- Search metrics and evaluation

---

### Relevance Engineering Prompts

#### Improving Search Relevance

**Context:** Users are complaining that search results aren't relevant enough.

```text
@relevance-engineer Help improve our search relevance:

Current issues:
- Exact matches not ranking at top
- Synonym queries returning no results
- Popular items buried in results
- Category pages outranking products
- Old content ranking above new content

Current setup:
- Elasticsearch 8.x
- 500K documents
- 50K daily searches
- No relevance tuning in place

Business context:
- E-commerce product search
- Search drives 40% of revenue
- Conversion rate from search is low (2%)
- Goal: increase to 5%

Please provide:
1. Relevance audit methodology
2. Query analysis and categorization
3. Scoring model improvements
4. Boosting strategy (recency, popularity, etc.)
5. Synonym and expansion handling
6. A/B testing framework
7. Relevance metrics to track
8. Continuous improvement process
```

**Expected Output:** Relevance improvement roadmap.

---

## 45.4 Autocomplete Systems with @autocomplete-expert

### Skill Introduction

The `@autocomplete-expert` skill provides expertise in building typeahead and suggestion systems. It helps you create fast, relevant autocomplete experiences that guide users to results.

**When to use this skill:**
- Building search suggestions
- Typeahead implementation
- Query completion systems
- Did-you-mean features

**Key strengths:**
- Autocomplete algorithms
- Performance optimization
- User behavior integration

---

### Autocomplete Prompts

#### Building Smart Autocomplete

**Context:** You need to build an autocomplete system for your search.

```text
@autocomplete-expert Design autocomplete for product search:

Requirements:
- Product title suggestions
- Category suggestions
- Brand suggestions
- Recent search history (per user)
- Popular searches
- Query predictions

Performance:
- Response time < 20ms
- Support for 1M products
- 500 autocomplete requests/second

Features:
- Highlight matching text
- Show result counts
- Thumbnail images
- Handle typos gracefully
- Personal history prioritization

Please provide:
1. Data structure design
2. Matching algorithms
3. Ranking of suggestions
4. Personalization approach
5. Caching strategy
6. Real-time updates
7. Frontend integration
8. Mobile considerations
```

**Expected Output:** Autocomplete system design.

---

## Best Practices Summary

### Index Design
1. **Mapping Carefully:** Define explicit mappings
2. **Analyzers:** Choose appropriate text analysis
3. **Denormalization:** Optimize for query patterns
4. **Lifecycle:** Manage index growth
5. **Testing:** Test with realistic data

### Query Optimization
1. **Filter vs Query:** Use filters for exact matches
2. **Caching:** Cache frequent queries
3. **Pagination:** Use search_after for deep pagination
4. **Timeouts:** Set query timeouts
5. **Profiling:** Profile slow queries

### Relevance
1. **Measure First:** Establish baselines
2. **Iterate:** Small, testable changes
3. **User Feedback:** Incorporate signals
4. **Explain:** Use explain API
5. **Monitor:** Track relevance metrics

---

## Reflection Points

1. **Build vs Buy:** When to use managed search services?
2. **Relevance vs Speed:** How do you balance ranking quality with latency?
3. **Personalization:** How much personalization is appropriate?
4. **Zero Results:** What's your strategy for empty result sets?

---

**Next Chapter:** [Chapter 46: Event Streaming →](chapter-46-event-streaming.md)
