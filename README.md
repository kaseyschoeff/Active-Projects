# Active-Projects

## Kasey Schoeff - Sales Engineer

Full-stack engineer building data-intensive systems and AI-powered applications. Most of my active work lives in private repositories due to client contracts and startup IP. This repo serves as a portfolio overview.

---

## Active Projects

### 1. AI-Powered Career Readiness Platform
**Startup (Cofounder)** | Student-Company Marketplace

Student-company marketplace where university students solve real business challenges, earn verified credentials, and build a portfolio of proven skills. Features a multi-stage AI evaluation pipeline for platform-issued credentials with citation-grounded scoring and adversarial review.

- **Platform:** Full end-to-end workflow — company posts problem, student applies/submits, company reviews, credential issued with cryptographic verification (HMAC-SHA256). Includes team formation via invite tokens, Office Hours Q&A, and a 500-entry skill taxonomy with autocomplete
- **AI Engine:** 4-stage evaluation pipeline (GPT-4.1-mini quality gate → GPT-4o primary evaluation → adversarial review → final determination) with programmatic citation verification against submission text
- **AI Challenge System:** 500+ challenge library with tier assignment (Foundational through Distinguished), cooldown logic, browse/submit flows, and auto-calibrating difficulty via nightly cron
- **White-Label:** University-first branding system — each partner university sees their own colors, logo, and name throughout. Platform engine runs underneath
- **Testing & QA:** Vitest (unit + integration), Playwright E2E with axe-core accessibility auditing, CodeRabbit automated PR reviews, Sentry error monitoring
- **Stack:** Next.js 14 (App Router), React 18, TypeScript, Supabase (PostgreSQL + Auth + RLS + Storage), Tailwind CSS, Resend, OpenAI API, Vercel

### 2. Job Market Intelligence Platform
**Contract Project (Better Career)** | Full-Stack + AI Pipeline

Full-stack pipeline that continuously scrapes job listings from multiple APIs, deduplicates across platforms using SHA-256 hashing, and enriches records via LLM with structured JSON output.

- **Architecture:** Two-service system — async Python scraper with scheduled jobs (APScheduler) writing to PostgreSQL, and a Next.js web app with interactive dashboards, 15+ filter dimensions, and an admin panel with scraper health monitoring, search query management (CRUD with inline edit), manual triggers, and enrichment prompt management
- **AI/ML:** LLM enrichment using gpt-4o-mini with JSON schema enforcement for domain classification, compensation normalization, seniority extraction, and contact discovery across 2,500+ filtered listings
- **Data Sources:** JSearch (RapidAPI), The Muse, Careerjet, with planned ATS web scraping (Greenhouse, Lever, Ashby) and LinkedIn integration via Playwright
- **Stack:** Next.js 15, React 19, TypeScript, Python, PostgreSQL, Prisma 6, NextAuth, TanStack Table, Recharts, Docker Compose, OpenAI API, Railway

### 3. 2nd Connections
**Startup (In Development)** | AI-Powered Professional Networking

Professional networking platform that matches users based on career goals, experience, and preferences using a multi-factor scoring algorithm combining structured criteria with semantic similarity via vector embeddings.

- **Matching Engine:** Hard constraints (seniority filters, timezone overlap) and soft preferences (interest overlap, function compatibility) with cosine similarity over 512-dimensional OpenAI embeddings (text-embedding-3-small). Availability management with weekly windows and exception dates
- **Optimization:** Greedy assignment algorithm to find highest-scoring pairings without conflicts, with proposed match expiration tracking
- **Safety & Moderation:** User blocking, reporting with audit trail, rate limiting, IP tracking, spam blocklist, and content moderation
- **Features:** Conversational onboarding flow, PDF resume parsing (Vercel Blob storage), dual authentication (Google OAuth + magic link via Nodemailer with multi-provider support), Cloudflare Turnstile, profile completeness tracking
- **Stack:** Next.js 16, React 19, TypeScript, Prisma, PostgreSQL, NextAuth, OpenAI Embeddings API, Vercel Blob, Nodemailer, Vercel

### 4. Autonomous Multi-Agent AI Pipeline
**Internal Tooling** | Multi-Agent Orchestration

26-agent autonomous development pipeline organized across 3 operational tiers, designed as a freelance agency that discovers clients, bids on work, delivers deployed products, and handles follow-ups with minimal human intervention.

- **Architecture:** Turborepo monorepo with 4 packages (core, agents, dashboard, headless). 3-tier model assignment — 5 GPT-4o command agents, 7 GPT-4o execution agents, 14 GPT-4.1-mini operations agents — orchestrated via Discord (14 structured channels), Redis pub/sub, and BullMQ priority queues
- **ModelRouter:** Provider-agnostic abstraction (OpenAI, Google Gemini, Local/Ollama) with per-agent Redis-backed config and hot-swap without restart. Per-agent, per-job token cost tracking with effective hourly rate calculation
- **Quality & Delivery:** Triple QA gate (GPT-4o self-review → o1 adversarial → human 2-minute scan), Project DNA fingerprinting with cosine similarity for 40-65% token savings on similar jobs, human blending system (voice profile, realistic timing delays, platform-adapted tone)
- **Dashboard:** Next.js 15 management app with real-time WebSocket to Redis, agent model hot-swap UI, job kanban with P&L tracking, client CRM, opportunity evaluation queue, financial dashboards, and chaos monkey resilience testing
- **Security:** AES-256-GCM credential vault with audit logging, automated quarterly key rotation
- **Revenue Streams:** Upwork/Fiverr API integration, RapidAPI endpoint monetization, Gumroad template sales, Stripe/LemonSqueezy payment processing
- **Stack:** TypeScript, Node.js 22+, Turborepo, pnpm, ioredis, BullMQ, Discord.js, Playwright, OpenAI SDK, Google AI SDK, Stripe, Next.js 15, React 19, Recharts, Radix UI

### 5. LinkedIn MCP Server
**AI Tooling** | SDK & API Integration

13-tool MCP server that extends AI agents with LinkedIn data access — used primarily as a research and lead-generation tool for sourcing contract opportunities and feeding data into other projects (e.g., Job Market Intelligence Platform).

- **Tools:** Job search and recommendations, posting analysis, structured LLM scoring with configurable criteria, profile and company contact extraction, recursive contact tree discovery, Notion CRM sync
- **Orchestrator:** Scheduled discovery cycles (8-hour intervals with jitter) for market monitoring, GPT-4o scoring against configurable criteria, Telegram notifications, one-time run mode for testing
- **Automation:** Persistent Playwright-based LinkedIn session with Voyager API interception, headless browser support, li_at cookie injection for CI environments, rate limiting, debug mode with response dumping
- **Stack:** TypeScript, Node.js, Playwright, MCP SDK, OpenAI SDK, Notion API, node-cron, Zod, Docker/Railway

### 6. SE Job Market Research
**Contract Project (Better Career)** | Data Science + NLP

Research project analyzing ~2,500 sales engineering job postings to quantify skill demand patterns, pay premiums, and market segmentation.

- **Pipeline:** Two-pass gpt-4o-mini extraction classifying postings against a YAML-driven taxonomy — 38 hard skill umbrellas, 31 soft skills, 7 domains, 14 verticals, 22 role scope tags, and 200+ daily tools. Cross-validated against GPT-4o for inter-model agreement (91 jobs)
- **Statistical Methods:** Bootstrap confidence intervals, Kruskal-Wallis tests, Mann-Whitney U tests, Benjamini-Hochberg FDR correction, controlled OLS regression, Wilson score intervals for binomial proportions, Pointwise Mutual Information (PMI) for co-occurrence analysis
- **Output:** 23 publication-ready visualizations with normalized concentration scoring to correct for category-size bias
- **Stack:** Python, OpenAI API, pandas, scipy, matplotlib, seaborn

### 7. Cracked Gaming
**Founding Engineer** | Twitch-Native Platform Startup

Real-time gaming platform where fans book gaming matches and live experiences with creators, featuring interactive queue systems, Twitch bot integration, and creator monetization.

- **Core Systems:** Arena queue system with visual position tracking, batch assignment, team formation, and game outcome recording. Pre-registration with scheduled start times and early-bird pricing. Weighted random selection favoring early queue joiners
- **Bounty System:** Community-proposed challenges with contribution pooling, Twitch chat yes/no voting via IRC (tmi.js), loop mode, and temporary bounty escrow for streamers without accounts
- **OBS Overlays:** Real-time queue display, earnings counter, celebration animations, bounty overlays — all streamed directly into creator broadcasts
- **Payments:** Stripe Connect for creator payouts, customer payment method management, fixed and auction pricing models
- **Performance:** Polling system load-tested at 50+ votes/sec sustained with <100ms latency and 95%+ success rate
- **Stack:** React 18, TypeScript, Vite, Express, PostgreSQL, Drizzle ORM, Stripe API, Twitch API (tmi.js + WebSocket), Radix UI, Framer Motion, TanStack React Query, Passport.js, React Hook Form + Zod

---

## Technical Overview

| Domain | Technologies |
|--------|-------------|
| **Languages** | TypeScript, Python, SQL |
| **Frontend** | React, Next.js, Vite, Tailwind CSS, Radix UI, Shadcn UI, Framer Motion, TanStack (React Query, Table), Recharts, ECharts |
| **Backend** | Node.js, Express, REST APIs, GraphQL, OAuth, JWT, APScheduler, BullMQ, Passport.js |
| **Databases** | PostgreSQL, Supabase, Neon, Redis (pub/sub, queues, state), Elasticsearch, MongoDB, DynamoDB, SQLite |
| **AI/ML** | OpenAI SDK (chat completions, embeddings, structured output, JSON schema), MCP (Model Context Protocol), multi-agent orchestration, multi-provider model routing, prompt engineering, RAG |
| **Cloud & DevOps** | AWS, Azure, Docker, Vercel, Railway, Turborepo, pnpm workspaces, CI/CD (GitHub/GitLab Actions) |
| **Testing** | Vitest, Playwright (E2E + accessibility), pytest, CodeRabbit |
| **Security** | AES-256-GCM encryption, HMAC-SHA256 credentials, Supabase RLS policies, Cloudflare Turnstile, rate limiting |

---

## Contact

- [LinkedIn](https://www.linkedin.com/in/kaseyschoeff)
- kasey.a.schoeff@gmail.com
