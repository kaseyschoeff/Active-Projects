# Active-Projects

# Kasey Schoeff - Software Engineer

Full-stack engineer building data-intensive systems and AI-powered applications. Most of my active work lives in private repositories due to client contracts and startup IP. This repo serves as a portfolio overview.

## Active Projects

### Job Market Intelligence Platform

### Pet Projects

**Startup (Cofounder)** | AI-Powered Career Readiness Platform

Student-company marketplace where university students solve real business challenges, earn verified credentials, and build a portfolio of proven skills. Features a multi-stage AI evaluation pipeline for platform-issued credentials with citation-grounded scoring and adversarial review.

* **Platform:** Full end-to-end workflow — company posts problem, student applies/submits, company reviews, credential issued with cryptographic verification (HMAC-SHA256)
* **AI Engine:** 4-stage evaluation pipeline (Haiku quality gate → Sonnet primary evaluation → adversarial review → final determination) with programmatic citation verification against submission text
* **White-Label:** University-first branding system — each partner university sees their own colors, logo, and name throughout. Platform engine runs underneath
* **Stack:** Next.js 14, React, TypeScript, Supabase (PostgreSQL + Auth + RLS), Tailwind CSS, Resend, Anthropic Claude API, Vercel

---

**Contract Project** | Full-Stack + AI Pipeline

Full-stack pipeline that continuously scrapes job listings from multiple APIs, deduplicates across platforms using SHA-256 hashing, and enriches records via LLM with structured JSON output.

- **Architecture:** Two-service system - async Python scraper with scheduled jobs (APScheduler) writing to PostgreSQL, and a Next.js web app with interactive dashboards and 15+ filter dimensions
- **AI/ML:** LLM enrichment using gpt-4.1-mini with JSON schema enforcement for domain classification, compensation normalization, and seniority extraction across 2,500+ listings
- **Data Sources:** Multiple job APIs, ATS platforms (Greenhouse), Common Crawl, Wayback Machine for historical analysis
- **Stack:** Next.js 15, React 19, TypeScript, Python, PostgreSQL, Prisma, Docker Compose, OpenAI API

---

### Second Connections
**Startup (In Development)** | AI-Powered Professional Networking

Professional networking platform that matches users using a 6-factor scoring algorithm combining structured criteria with semantic similarity via vector embeddings.

- **Matching Engine:** Combines seniority, timezone, function, and interest matching with cosine similarity over 512-dimensional OpenAI embeddings (text-embedding-3-small)
- **Optimization:** Greedy assignment algorithm to find highest-scoring pairings without conflicts
- **Features:** PDF resume parsing for embedding context, dual authentication (Google OAuth + magic link), Cloudflare Turnstile, rate limiting
- **Stack:** Next.js 16, React 19, TypeScript, Prisma, PostgreSQL, OpenAI Embeddings API, Vercel

---

### Autonomous AI Development Pipeline

**Internal Tooling** | Multi-Agent Orchestration

22-agent autonomous development pipeline organized across 7 operational tiers, managing parallel workstreams across multiple active projects with minimal human intervention.

* **Architecture:** 7-tier agent hierarchy (Command & Control, Development, Infrastructure, Productivity, Quality, Intelligence, Financial) orchestrated via Discord, Redis, and BullMQ on Railway
* **Optimization:** Dynamic context loading and prompt caching reducing steady-state operating cost to ~$140–170/month across all agents and workstreams
* **Capabilities:** Autonomous task decomposition, cross-project coordination, code generation and review, infrastructure management, and financial tracking across 4 concurrent projects
* **Stack:** TypeScript, Node.js, Redis, BullMQ, Discord.js, Anthropic Claude API, Railway, Stripe

---

### SE Job Market Research
**Contract Project** | Data Science + NLP

Research project analyzing ~2,500 software engineering job postings to quantify skill demand patterns, pay premiums, and market segmentation.

- **Pipeline:** Two-pass LLM extraction classifying postings against a 38-umbrella YAML-driven skill taxonomy across domains, verticals, and role scopes
- **Statistical Methods:** Bootstrap confidence intervals, Kruskal-Wallis tests, Mann-Whitney U tests, Benjamini-Hochberg FDR correction, controlled OLS regression
- **Output:** 23 publication-ready visualizations, normalized concentration scoring to correct for category-size bias
- **Stack:** Python, OpenAI API, pandas, scipy, matplotlib, seaborn

---

### Cracked Gaming
**Founding Engineer** | Twitch-Native Platform Startup

Real-time gaming platform focused on creator engagement and monetization through interactive systems.

- **Core Systems:** Arena queue system for live matches, Stripe monetization infrastructure, real-time Twitch integrations (WebSocket, tmi.js, OBS overlays)
- **Architecture:** Full-stack ownership from product definition through production deployment, shipping features on weekly cadence
- **Stack:** React, TypeScript, Express, PostgreSQL, Drizzle ORM, Stripe API, Twitch API

---

## Technical Overview

| Domain | Technologies |
|---|---|
| **Frontend** | React, TypeScript, Next.js, Angular, Tailwind CSS, ECharts |
| **Backend** | Node.js, Express, Python, REST APIs, GraphQL, OAuth, JWT |
| **Databases** | PostgreSQL, Elasticsearch, Redis, MongoDB, DynamoDB |
| **AI/ML** | OpenAI API, Claude API, embeddings, structured JSON output, prompt engineering, RAG |
| **Cloud** | AWS, Azure, Docker, Vercel, Railway, CI/CD (GitHub/GitLab Actions) |

## Contact

- [LinkedIn](https://www.linkedin.com/in/kaseyschoeff)
- kasey.a.schoeff@gmail.com
