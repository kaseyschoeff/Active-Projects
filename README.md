# Active-Projects

# Kasey Schoeff - Software Engineer

Full-stack engineer building data-intensive systems and AI-powered applications. Most of my active work lives in private repositories due to client contracts and startup IP. This repo serves as a portfolio overview.

## Active Projects

### Job Market Intelligence Platform
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
