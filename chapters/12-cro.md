# Chapter 12: Conversion Rate Optimization (CRO)

**Last Updated:** February 5, 2026

---

## Overview

Conversion Rate Optimization is the systematic process of increasing the percentage of website visitors who take desired actions. This chapter covers skills for analyzing user behavior, running experiments, and optimizing conversion funnels.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@cro-expert` | Conversion optimization | Site audits, hypothesis generation |
| `@ab-testing-expert` | Experimentation | Test design, statistical analysis |
| `@analytics-expert` | Data analysis | Traffic analysis, user flow tracking |
| `@user-research` | User insights | Surveys, heatmaps, interviews |
| `@funnel-optimization` | Funnel analysis | Drop-off reduction, checkout opt |

---

## 12.1 CRO Fundamentals with @cro-expert

### Skill Introduction

The `@cro-expert` skill provides a systematic approach to improving conversion rates. It helps you identify barriers to conversion, create hypotheses, and implement optimization strategies based on data and psychology.

**When to use this skill:**
- Auditing a website or landing page for conversion issues
- Developing a roadmap of optimization experiments
- Analyzing high bounce rates or low engagement
- Improving page load speed and technical performance concepts
- Applying persuasion psychology principles (Cialdini, Fogg)

**Key strengths:**
- Heuristic analysis frameworks (LIFT, MECLABS)
- Conversion copywriting and design principles
- Hypothesis generation and prioritization (ICE/PIE)
- Audit methodology

---

### CRO Prompts

#### Conducting a Heuristic Analysis

**Context:** You are optimizing a low-converting landing page for a B2B service.

```text
@cro-expert Conduct a heuristic analysis of our landing page using the LIFT Model:

Scenario: B2B consulting service landing page.
Current Conversion Rate: 0.5% (Benchmark: 2-3%)

Please analyze potential issues across these 6 factors:
1. Value Proposition (Is it clear and relevant?)
2. Relevance (Does it match ad intent?)
3. Clarity (Is the design/copy clear?)
4. Urgency (Is there a reason to act now?)
5. Anxiety (Are there trust or risk issues?)
6. Distraction (Are there competing elements?)

Provide specific recommendations to address the top 3 friction points identified.
```

**Expected Output:** A detailed audit report identifying friction points and specific recommendations for improvement.

---

#### Prioritizing Experiment Ideas

**Context:** You have a backlog of 20 ideas to test but limited traffic. You need to prioritize.

```text
@cro-expert Prioritize these 5 test ideas using the ICE Framework (Impact, Confidence, Ease):

Ideas:
1. Redesign the entire homepage (High effort)
2. Change the CTA button color (Low effort)
3. Add customer testimonials near the form (Medium effort)
4. Remove the navigation bar on checkout (Medium effort)
5. Rewrite the main headline (Low effort)

For each, estimate ICE scores (1-10) and explain the reasoning.
Rank them in order of implementation priority.
```

**Expected Output:** A prioritized list of experiments with scored reasoning.

---

## 12.2 A/B Testing with @ab-testing-expert

### Skill Introduction

The `@ab-testing-expert` skill applies scientific rigor to optimization. It covers experiment design, sample size calculation, statistical significance, and result interpretation to ensure you make data-backed decisions.

**When to use this skill:**
- Designing valid A/B or multivariate tests
- Calculating required sample sizes and test duration
- Analyzing test results for statistical significance
- Avoiding common testing pitfalls (Peeking, false positives)
- Documenting test learnings

**Key strengths:**
- Statistical analysis expertise
- Experiment design methodology
- Test tool configuration (Optimizely, VWO, Google Optimize)
- Result visualization and reporting

---

### A/B Testing Prompts

#### Designing a Valid A/B Test

**Context:** You want to test a new checkout flow to reduce abandonment.

```text
@ab-testing-expert Design a robust A/B test for our checkout page:

Hypothesis: Removing the "Create Account" forced step and allowing "Guest Checkout" will increase purchase completion rate by 10%.

Traffic: 5,000 visitors/week to checkout.
Current Conversion: 30%.

Please provide:
1. Test Variants (Control vs. Variation A)
2. Primary Metric (e.g., Completed Orders)
3. Secondary Metrics (e.g., AOV, Time on task)
4. Sample Size Calculation (How many visitors needed per variant for 95% significance?)
5. Estimated Test Duration
6. Guardrail Metrics (What shouldn't decrease?)
```

**Expected Output:** A complete test plan document including statistical calculations and metric definitions.

---

#### Analyzing Inconclusive Results

**Context:** You ran a test for 2 weeks, and the result is "No significant difference."

```text
@ab-testing-expert Analyze these inconclusive A/B test results and recommend next steps:

Test: Headline change.
Control: 2.1% CR
Variation: 2.2% CR
Confidence: 80% (not 95%)
Sample size: 2,000 per variant.

Questions:
1. Was the test underpowered? (Did we have enough sample?)
2. Should we run it longer?
3. Should we segment the data (Mobile vs Desktop)?
4. What does a "flat" result tell us about the element tested?
5. Recommendations for the next iteration.
```

**Expected Output:** An analysis of the test validity and strategic recommendations for next steps.

---

## 12.3 Funnel Optimization with @funnel-optimization

### Skill Introduction

The `@funnel-optimization` skill focuses on analyzing the full user journey, identifying drop-off points, and optimizing specific stages of the funnel (Acquisition, Activation, Retention, Revenue, Referral).

**When to use this skill:**
- Mapping user flows and funnels
- Identifying the biggest "leaks" in a conversion funnel
- Optimizing onboarding flows
- Reducing churn at specific funnel stages
- Analyzing micro-conversions

**Key strengths:**
- Funnel visualization and analysis
- Pirate Metrics (AARRR) framework
- User journey mapping
- Drop-off root cause analysis

---

### Funnel Optimization Prompts

#### Analyzing Drop-off Points

**Context:** You have an e-commerce site with high cart abandonment.

```text
@funnel-optimization Analyze our e-commerce checkout funnel to identify the biggest leak:

Funnel Data (Last 30 days):
1. Product Page View: 10,000 visitors
2. Add to Cart: 500 visitors (5% conversion)
3. View Cart: 450 visitors (90% of Add to Cart)
4. Start Checkout: 300 visitors (66% of View Cart)
5. Enter Shipping Info: 150 visitors (50% of Start Checkout)
6. Enter Payment Info: 100 visitors (66% of Shipping)
7. Purchase Complete: 80 visitors (80% of Payment)

Task:
1. Calculate the drop-off rate between each step.
2. Identify the single biggest bottleneck.
3. Propose 3 hypotheses for WHY users drop off there.
4. Suggest 3 specific optimizations to fix that bottleneck.
```

**Expected Output:** A funnel analysis report highlighting critical drop-offs and actionable fixes.

---

## 12.4 User Research for CRO with @user-research

### Skill Introduction

The `@user-research` skill provides qualitative insights to complement quantitative data. It covers methods like surveys, user interviews, heatmaps, and session recordings to understand "Why" users behave the way they do.

**When to use this skill:**
- Gathering feedback from users who didn't convert
- Analyzing heatmaps and scroll maps
- Designing exit-intent surveys
- Conducting usability testing sessions
- creating user personas based on behavior

**Key strengths:**
- Qualitative research methods
- Survey design and analysis
- Heatmap interpretation
- Usability testing protocols

---

### User Research Prompts

#### Designing a Post-Purchase Survey

**Context:** You want to understand what motivated successful customers to buy.

```text
@user-research Design a post-purchase survey to gather CRO insights:

Goal: Understand the primary driver for purchase and any friction experienced.
Placement: Thank You page (immediately after purchase).

Please provide:
1. 3-4 specific questions to ask.
2. Question type (Open-ended vs Multiple choice).
3. Explanation of what insight each question aims to uncover (e.g., "Voice of Customer" data).
4. How to analyze the responses to improve the landing page.
```

**Expected Output:** A survey script with rationale for each question.

---

## Best Practices Summary

### Systematic Process
- **Research First:** Don't guess; use data and user feedback to inform ideas.
- **Prioritize Ruthlessly:** You can't test everything. Focus on high-impact areas.
- **Test to Learn:** Even "failed" tests provide valuable insights about your audience.

### Statistical Rigor
- **Patience:** Wait for statistical significance. Don't stop tests early because they look "good."
- **Sample Size:** Ensure you have enough traffic to run valid tests.
- **Segmentation:** A test might lose overall but win for a specific segment (e.g., Mobile).

### User-Centricity
- **Remove Friction:** Make it as easy as possible for users to act.
- **Add Motivation:** Clearly communicate value and address anxieties.
- **Listen:** User research often reveals "why" the numbers are "what" they represent.

---

## Reflection Points

1. ** Culture of Experimentation:** Is testing encouraged, or is failure punished?
2. **Quality vs Quantity:** Are you running meaningless tests just to say you are testing?
3. **Data Integrity:** Do you trust your analytics setup? If data is bad, decisions are bad.
4. **Mobile Experience:** Are you optimizing for mobile users as a primary audience?

---

**Next Chapter:** [Chapter 13: Business Strategy & Analysis →](13-business-strategy.md)
