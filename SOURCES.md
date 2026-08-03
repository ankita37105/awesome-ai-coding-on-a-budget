# **HANDOFF.md**

This handoff document provides a comprehensive inventory, functional categorization, and hyperlinked repository/website index of all sources included in this session. It is structured to serve as an immediate operational manual for incoming AI agents, developers, and autonomous harnesses.

## **Executive Summary**

The collected materials represent an ecosystem spanning **LLM Gateways, Token Compression Engines, Agent Skills, Codebase Intelligence Systems, and Execution Infrastructure**. This document indexes all project repositories, API endpoints, web portals, technical analyses, and podcasts into a unified reference framework.

## **1\. LLM Gateways, Routers & API Proxies**

This class of tools centralizes access to commercial, open-source, and local LLMs by providing OpenAI/Claude/Gemini-compatible endpoints, dynamic routing, auto-fallback, cost limits, and multi-account load balancing.

| Name | GitHub / Source Repository | Documentation & Portal Links | Primary Capabilities & Functions |
| :---- | :---- | :---- | :---- |
| **Manifest** | [mnfst/manifest](https://github.com/mnfst/manifest) | [manifest.build](https://manifest.build/) | Open-source LLM gateway supporting 300+ models across 32 providers. Features custom routing, full-body logging, cost tracking, and on-the-fly request Auto-fix. |
| **OmniRoute** | [diegosouzapw/OmniRoute](https://github.com/diegosouzapw/OmniRoute) | [omniroute.online](https://omniroute.online) | Free MIT AI gateway aggregating 290+ providers and 500+ models. Includes 19 routing strategies, built-in RTK/Caveman token compression, and MCP/A2A servers. |
| **9router** | [decolua/9router](https://github.com/decolua/9router) | [9router.com](https://9router.com/) | Next.js-based AI proxy providing 3-tier fallback, multi-account rotation, format translation, and token-saving RTK/Caveman modes. |
| **CLIProxyAPI** | [router-for-me/CLIProxyAPI](https://github.com/router-for-me/CLIProxyAPI) | [docs/sdk-usage.md](https://github.com/router-for-me/CLIProxyAPI/blob/main/docs/sdk-usage.md) | Go-based proxy server exposing OpenAI/Gemini/Claude/Grok endpoints for CLI accounts (Codex, Claude Code, Grok, Gemini, Kimi). |
| **CLI Proxy Management Center** | [router-for-me/Cli-Proxy-API-Management-Center](https://github.com/router-for-me/Cli-Proxy-API-Management-Center) | [GitHub Repository](https://github.com/router-for-me/Cli-Proxy-API-Management-Center) | WebUI dashboard for CLIProxyAPI managing runtime status, config.yaml, OAuth flows, auth files, quotas, and request logs. |
| **LiteLLM** | [BerriAI/litellm](https://github.com/BerriAI/litellm) | [docs.litellm.ai](https://docs.litellm.ai/docs/) | Rust core \+ Python SDK proxy serving 100+ LLM APIs in unified OpenAI format with cost tracking, guardrails, and MCP/A2A support. |
| **Free Claude Code** | [Alishahryar1/free-claude-code](https://github.com/Alishahryar1/free-claude-code) | [GitHub Repository](https://github.com/Alishahryar1/free-claude-code) | Local proxy and desktop launcher running Claude Code, Codex, and Pi over 31 cloud/local providers with Admin UI control. |
| **Sub2API** | [Wei-Shaw/sub2api](https://github.com/Wei-Shaw/sub2api) | [GitHub Repository](https://github.com/Wei-Shaw/sub2api) | Open-source subscription relay service unifying Claude, OpenAI, Gemini, and Grok into a shared, cost-effective API endpoint. |
| **Antigravity-Manager** | [lbjlaq/Antigravity-Manager](https://github.com/lbjlaq/Antigravity-Manager) | [GitHub Repository](https://github.com/lbjlaq/Antigravity-Manager) | Tauri v2 \+ React desktop application for Google/Antigravity multi-account management, protocol translation, and 429 failover. |

## **2\. Token Optimization & Prompt Compression**

Solutions focused on compressing prompt context, terminal outputs, documentation, and agent responses to mitigate context window bloat and cut API costs.

> * **Headroom** ([GitHub](https://github.com/headroomlabs-ai/headroom) | [Docs](https://docs.headroomlabs.ai/docs/)): Context compression engine operating as a library, proxy, or MCP server. Uses reversible compression (CCR), SmartCrusher, and Kompress-v2-base models to reduce token burn by 20–95%.  
> * **Runtime Token Kit (RTK)** ([GitHub](https://github.com/rtk-ai/rtk) | [Guide](https://rtk-ai.app/guide)): High-performance Rust CLI proxy that intercepts and compresses shell command outputs (git, grep, cargo test, ls) by 60–90% before reaching LLMs.  
> * **Caveman** ([GitHub](https://github.com/JuliusBrussee/caveman) | [Website](https://caveman.so/)): Agent skill/plugin for 30+ agents that strips filler words and enforces concise caveman-speak, reducing output tokens by 65% while preserving code exactness.  
> * **Ponytail** ([GitHub](https://github.com/DietrichGebert/ponytail) | [Website](https://ponytail.dev)): YAGNI-focused agent skill ("lazy senior dev") that prompts agents to write minimal code changes, reducing output code by \~54% and saving tokens.  
> * **SimpleEnglish** ([GitHub](https://github.com/AminBlg/SimpleEnglish)): ASD-STE100 Simplified Technical English agent skill enforcing 53 rules to eliminate AI slop and ambiguity from technical documentation.  
> * **The Token Company** ([Website](https://thetokencompany.com) | [Docs](https://thetokencompany.com/docs)): API service and SDK wrapper for OpenAI/Anthropic clients offering automated prompt compression.  
> * **Technical Taxonomy of Token Optimization**: Comparative study evaluating token-reduction paradigms across WOZCODE, Token Optimizer, Token Savior, RTK, and Graphify.

## **3\. Agent Skills, Quality & Engineering Frameworks**

Composable workflows, deterministic rule files, and static code analysis tools designed to enforce engineering standards within AI agent sessions.

| Resource | Source Link | Purpose & Integration |
| :---- | :---- | :---- |
| **Matt Pocock Agent Skills** | [mattpocock/skills](https://github.com/mattpocock/skills) | Suite of practical engineering skills (/grill-me, /triage, /to-spec, /to-tickets, /implement, /wayfinder, /tdd). |
| **Fallow** | [fallow-rs/fallow](https://github.com/fallow-rs/fallow) | Codebase intelligence for TypeScript/JS providing static analysis, circular dependency tracking, and an integrated MCP server/skill. |
| **jscpd** | [kucherenko/jscpd](https://github.com/kucherenko/jscpd) | Copy/paste duplicate detector supporting 223 formats, complete with an AI-ready token-efficient reporter and dry-refactoring skill. |

## **4\. Codebase Intelligence, RAG & MCP Servers**

Tools that index codebases into knowledge graphs or retrieve documentation to supply accurate context without exhausting context windows.

> * **Codebase Memory MCP** ([GitHub](https://github.com/DeusData/codebase-memory-mcp)): High-performance Tree-sitter knowledge graph indexing 158 languages into a persistent SQLite store. Enables sub-millisecond structural queries and 120x token reduction compared to file searches.  
> * **Context7** ([GitHub](https://github.com/upstash/context7) | [Website](https://context7.com)): Up-to-date documentation platform and MCP server fetching version-specific library docs directly into prompts.

## **5\. Usage Analytics, Cost Tracking & Benchmarks**

Monitoring solutions and database indexes for inspecting token burn, model pricing, and execution metrics.

> * **Tokscale** ([GitHub](https://github.com/junhoyeo/tokscale) | [Leaderboard](https://tokscale.ai)): Terminal CLI and global leaderboard tracking token consumption and cost across 30+ agent environments.  
> * **ccusage** ([GitHub](https://github.com/ccusage/ccusage)): CLI analytics utility summarizing token spend across Claude Code, Codex, OpenCode, Goose, Droid, and other agent platforms.  
> * **Models.dev** ([Website](https://models.dev) | [GitHub](https://github.com/opencode-ai/models)): Open-source database and JSON API detailing model specs, context windows, providers, and pricing.  
> * **Awesome Free LLM APIs** ([GitHub](https://github.com/mnfst/awesome-free-llm-apis)): Curated index of permanent free-tier LLM API keys.  
> * **Artificial Analysis** ([Website](https://artificialanalysis.ai)): Independent benchmarking site tracking LLM performance across agentic knowledge work and SaaS workflow benchmarks.

## **6\. Infrastructure, Batching & Routers**

Execution sandboxes, batch execution SDKs, and cloud meta-routers.

> * **Sail Research** ([Website](https://sail.services)): Long-horizon agent infrastructure providing cost-efficient inference and Sailboxes (VMs) for autonomous background workflows.  
> * **Batchwork** ([Website](https://batchwork.dev) | [Docs](https://batchwork.dev/docs/job)): Unified batch processing library for OpenAI, Anthropic, Gemini, Azure, Groq, Mistral, Together AI, and xAI.  
> * **OpenRouter Routing Solutions** ([Portal](https://openrouter.ai)):  
  * *Auto Router* (openrouter/auto)  
  * *Fusion Router* (openrouter/fusion)  
  * *Pareto Code Router* (openrouter/pareto-code)  
> * **The Pulse (Gergely Orosz)** ([Substack](https://newsletter.pragmaticengineer.com)): Industry analysis covering intelligent model routing trends (Weave, Kilo, OpenRouter).

## **7\. Operational Essays, Transcripts & Reference Guides**

Synthesized guides, podcasts, and architecture essays covering agent harness design.

> * **OmniRoute Guides**:  
  * [Provider Reference Spec](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/PROVIDER_REFERENCE.md)  
  * [Free Tiers Budget Methodology](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/FREE_TIERS.md)  
  * [Free Proxies API Reference](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/FREE_PROXIES_API.md)  
  * *OmniRoute with Claude Code Setup Walkthrough*: Integration notes for Claude Code, Open Design, and OpenCode.  
> * **Software After AI (Tomasz Tunguz)** ([Article](https://tomtunguz.com)): Defines the 7 pillars of agent harnesses (Context, Tools, Orchestration, State, Sandboxes, Observability, Cost Optimization).  
> * **8 Tech Choices Before Agentmaxxing**: Podcast discussion on establishing strict rules, linters, and architectural conventions before delegating tasks to autonomous agents.  
> * **How to Fix Vibe Coding**: Technical discussion covering headless browser execution (Agent Browser, Chrome DevTools MCP, Light Panda) and task management (dex.ri, beads).  
> * **This Coding Tool Kills AI Code Slop**: Review covering codebase inspection, plugin architectures, and automated agent skills.

## **Complete Source Reference Index**

| Resource / Document Title | Type | Reference / Direct URL | Citation Tag |
| :---- | :---- | :---- | :---- |
| mnfst/manifest | GitHub | [github.com/mnfst/manifest](https://github.com/mnfst/manifest) |  |
| AminBlg/SimpleEnglish | GitHub | [github.com/AminBlg/SimpleEnglish](https://github.com/AminBlg/SimpleEnglish) |  |
| Alishahryar1/free-claude-code | GitHub | [github.com/Alishahryar1/free-claude-code](https://github.com/Alishahryar1/free-claude-code) |  |
| Manifest Gateway | Website | [manifest.build](https://manifest.build/) |  |
| junhoyeo/tokscale | GitHub | [github.com/junhoyeo/tokscale](https://github.com/junhoyeo/tokscale) |  |
| diegosouzapw/OmniRoute | GitHub | [github.com/diegosouzapw/OmniRoute](https://github.com/diegosouzapw/OmniRoute) |  |
| DietrichGebert/ponytail | GitHub | [github.com/DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) |  |
| Tool Directory CSV | Data | Uploaded Document |  |
| BerriAI/litellm | GitHub | [github.com/BerriAI/litellm](https://github.com/BerriAI/litellm) |  |
| mattpocock/skills | GitHub | [github.com/mattpocock/skills](https://github.com/mattpocock/skills) |  |
| DeusData/codebase-memory-mcp | GitHub | [github.com/DeusData/codebase-memory-mcp](https://github.com/DeusData/codebase-memory-mcp) |  |
| decolua/9router | GitHub | [github.com/decolua/9router](https://github.com/decolua/9router) |  |
| router-for-me/CLIProxyAPI | GitHub | [github.com/router-for-me/CLIProxyAPI](https://github.com/router-for-me/CLIProxyAPI) |  |
| upstash/context7 | GitHub | [github.com/upstash/context7](https://github.com/upstash/context7) |  |
| Fix Vibe Coding | Transcript | Uploaded Document |  |
| OmniRoute Setup Guide | Guide | Uploaded Document |  |
| OmniRoute Provider Ref | Markdown | [OmniRoute/docs/reference/PROVIDER\_REFERENCE.md](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/PROVIDER_REFERENCE.md) |  |
| JuliusBrussee/caveman | GitHub | [github.com/JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman) |  |
| headroomlabs-ai/headroom | GitHub | [github.com/headroomlabs-ai/headroom](https://github.com/headroomlabs-ai/headroom) |  |
| OpenRouter Fusion | Doc | [openrouter.ai](https://openrouter.ai) |  |
| fallow-rs/fallow | GitHub | [github.com/fallow-rs/fallow](https://github.com/fallow-rs/fallow) |  |
| Wei-Shaw/sub2api | GitHub | [github.com/Wei-Shaw/sub2api](https://github.com/Wei-Shaw/sub2api) |  |
| mnfst/awesome-free-llm-apis | GitHub | [github.com/mnfst/awesome-free-llm-apis](https://github.com/mnfst/awesome-free-llm-apis) |  |
| Artificial Analysis | Website | [artificialanalysis.ai](https://artificialanalysis.ai) |  |
| lbjlaq/Antigravity-Manager | GitHub | [github.com/lbjlaq/Antigravity-Manager](https://github.com/lbjlaq/Antigravity-Manager) |  |
| Batchwork | Website | [batchwork.dev](https://batchwork.dev) |  |
| Models.dev | Website | [models.dev](https://models.dev) |  |
| rtk-ai/rtk | GitHub | [github.com/rtk-ai/rtk](https://github.com/rtk-ai/rtk) |  |
| OpenRouter Auto Router | Doc | [openrouter.ai](https://openrouter.ai) |  |
| OpenRouter Pareto Code | Doc | [openrouter.ai](https://openrouter.ai) |  |
| The Pulse Newsletter | Substack | [newsletter.pragmaticengineer.com](https://newsletter.pragmaticengineer.com) |  |
| CLI Proxy Management Center | GitHub | [github.com/router-for-me/Cli-Proxy-API-Management-Center](https://github.com/router-for-me/Cli-Proxy-API-Management-Center) |  |
| OmniRoute Free Proxies API | Markdown | [OmniRoute/docs/reference/FREE\_PROXIES\_API.md](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/FREE_PROXIES_API.md) |  |
| Technical Taxonomy Paper | Paper | Uploaded Document |  |
| kucherenko/jscpd | GitHub | [github.com/kucherenko/jscpd](https://github.com/kucherenko/jscpd) |  |
| OmniRoute Free Tiers | Markdown | [OmniRoute/docs/reference/FREE\_TIERS.md](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/FREE_TIERS.md) |  |
| Sail Research | Website | [sailresearch.com](https://www.sailresearch.com/) |  |
| ccusage/ccusage | GitHub | [github.com/ccusage/ccusage](https://github.com/ccusage/ccusage) |  |
| Tomasz Tunguz Essay | Article | [tomtunguz.com](https://tomtunguz.com) |  |
| The Token Company | Website | [thetokencompany.com](https://thetokencompany.com) |  |
|  |  |  |  |
|  |  |  |  |

## **8 Tech Choices to Lock In Before Agentmaxxing**

[8 Tech Choices to Lock In Before Agentmaxxing](https://www.youtube.com/watch?v=PrS_IyC9Jss)

### **Core Thesis: "Get Your House in Order" First**

Before unleashing AI agents onto a codebase ("agent maxing"), you must establish clear structures, rules, and architecture. If you don't give AI agents explicit homes and guidelines for code, they will invent redundant tables, mix architectural patterns, and create unmaintainable "slop."

Consistency and strong base architecture allow agents to move fast without ruining the project.

### **8 Essential Decisions to Lock In Before "Agent Maxing"**

* 1\. Database Schema  
  * Manually plan or pseudo-code data models (using Markdown or hand-authored TypeScript types) before having AI scaffold the database.  
  * *Why:* AI left on its own tends to create redundant tables, unnecessary status flags, and complex, uncleaned cross-references.  
* 2\. TypeScript Types  
  * Define core domain types, client-side data structures, and API request/response shapes early.  
  * *Why:* Establishes a shared contract across the codebase for both humans and AI agents.  
* 3\. Validation Implementation  
  * Choose a single validation framework (ideally one adhering to the Standard Schema specification, like Valibot or Zod) and stick to it on both client and server.  
  * *Why:* Ensures runtime validation remains consistent and prevents schema drift across boundaries.  
* 4\. Routing Structure & Access Control (Auth)  
  * Outline all public, protected, private, and admin routes upfront in an organized list.  
  * Implement user ownership and authorization controls from the start.  
  * *Why:* Adding user ownership to database tables and routes after the fact requires painful retrofits and complex migrations.  
* 5\. CSS Methodology & Base Styles  
  * Establish design tokens, styling conventions (e.g., Tailwind, CSS Modules, Utility classes), and linting rules (e.g., Stylelint).  
  * *Why:* Prevents AI from inventing random class structures, fragmented inline styles, or competing CSS naming conventions.  
* 6\. UI Component Framework  
  * Select a primary component library or design system (e.g., Base UI, Kumo) for complex inputs, modals, and datepickers.  
  * *Why:* Prevents AI from rewriting UI controls from scratch or importing arbitrary third-party component packages.  
* 7\. Client-Server Communication (Comms)  
  * Standardize one interaction pattern for fetching and mutating data (e.g., REST API routes, RPC, or React Server Components).  
  * *Why:* Stops AI from randomly mixing client-side fetching strategies across different features.  
* 8\. Folder Structure  
  * Define explicit rules for where files belong (e.g., feature-based vs. route-based directory structures).  
  * *Why:* Without clear rules, AI agents will dump new components into random folders or create a flat, disorganized root directory.

# 

# **How to Fix Vibe Coding**

[How to Fix Vibe Coding](https://www.youtube.com/watch?v=LSq485DvILM)

[https://syntax.fm/show/998/how-to-fix-vibe-coding](https://syntax.fm/show/998/how-to-fix-vibe-coding)

### **Show Notes**

* Code quality tools  
  * [jscpd.dev](https://jscpd.dev/)  
  * [knip.dev](https://knip.dev/)  
  * [fallow.tools](https://fallow.tools/)  
  * [wallace](https://github.com/projectwallace/wallace-cli)  
*  Finding and using components  
  * [Storybook AI](https://storybook.js.org/ai)  
* Finding bugs  
  * [Sentry CLI](https://cli.sentry.dev/)  
  * [Spotlight](https://spotlightjs.com/)  
* Formatting and linting  
  * [Vite+](https://viteplus.dev/)  
  * [ESLint](https://eslint.org/)  
  * [StyleLint](https://stylelint.io/)  
  * [Clint](https://github.com/stolinski/clint)  
  * [Ultracite](https://www.ultracite.ai/)  
* Headless browsers  
  * [agent-browser](https://github.com/vercel-labs/agent-browser)  
  * [chrome-devtools-mcp](https://github.com/ChromeDevTools/chrome-devtools-mcp)  
  * [Lightpanda](https://lightpanda.io/)  
* Docs  
  * [Context7](https://context7.com/)

### **Transcript Summary:**

#### **Core Philosophy**

* **Enforce Hard Guardrails Over Prompting:** Soft guidelines in agents.md or system prompts can easily be ignored by AI agents. Replace "wishy-washy vibes" with deterministic tools (linters, CLI checkers, tests) that produce binary pass/fail results.

#### **Code Quality & Architectural Health**

* **Catch Structural Slop Early:** Use code analysis tools to keep AI-generated code clean before complexity spiraling out of control:  
  * **Fallow:** Scans for dead code, duplicate functions, circular dependencies, complexity hotspots, and maintainability metrics out of the box.  
  * **Project Wallace:** Detects bloated CSS issues, such as AI explicitly defining font-size, line-height, or duplicate colors on every single element.  
  * **KnIP & JSCPD:** Useful fallback options for identifying unused dependencies/exports and cross-file duplicate logic.

#### **Ground-Truth Context & Components**

* **Feed Canonical Examples:** Prevent AI from guessing component implementations or reinventing local utilities by connecting design system tools like **Storybook** (via MCP) or documentation platforms like **Context7**.

#### **Real-Time Error Reporting & Debugging**

* **Give Agents Direct Diagnostics:** Instead of manually copying logs back and forth with the LLM:  
  * Use **Sentry CLI** so AI agents can look up error root causes directly in production/staging.  
  * Use **Spotlight** (spotlightjs.com) locally as an MCP server to expose dev logs, console errors, trace metrics, and database timing directly to the AI.

#### **Custom Linting & Guardrails**

* **Write Custom Linter Rules for AI Bad Habits:** AI often cheats types (e.g., overusing as assertions) or misuses reactivity (e.g., throwing useEffect / effect everywhere). Write custom **ESLint** or **Stylelint** plugins that fail builds when these specific AI antipatterns occur.  
* **Streamline Tools:** Use fast, zero-config checking pipelines like **Vite+ / VP Check** or modern Rust-based linters to keep feedback loops fast.

#### **Automated Browser Verification**

* **Give AI Visual/Console Access:** Use headless browser integrators like **Agent Browser**, **Chrome DevTools MCP**, or high-performance runtimes like **LightPanda** (Zig/V8 engine) so agents can take screenshots, verify DOM changes, inspect network calls, and self-correct UI bugs.

#### **Task Management & Execution Strategies**

* **Use Deterministic Task Trackers:** Track multi-step agent tasks using Git/JSON-backed task managers (such as **Dex** or **Beads**) to maintain strict execution sequences and task dependencies.  
* **Run Mandatory Post-Feature Pipelines:** Require AI agents to run an automated quality script (e.g., *Typecheck $\\rightarrow$ Linter $\\rightarrow$ Complexity Scan*) upon finishing a task, or block commits via Git hooks until all checks pass.  
* **Prefer Code Sandbox/CLI Execution:** LLMs perform better when executing scripts/CLI tools directly or using execution sandboxes (e.g., TanStack / Cloudflare "Code Mode") rather than relying on heavy context-heavy tool schemas.

## **AI Pricing Summary & The Grey Market**

While standard monthly AI subscriptions are typically advertised at a flat rate (e.g., $20 or $200), the actual prices users pay—and the prices found on third-party reseller sites—vary wildly. This discrepancy is driven by regional tax laws, currency valuations, and grey market exploitation.

### **How Resellers Offer "Discounted" Accounts**

Users will often find top-tier plans (like Claude Max 20x or ChatGPT Plus 20x, normally $200/month) sold for $130–$160 on third-party forums and marketplaces. There is no legitimate wholesale discount for these plans; instead, resellers use several tactics:

* **The Open-Source Grant Loophole (Specific to Claude):** Resellers create fake GitHub projects, artificially inflate their popularity using bots, and apply for Anthropic's free 6-month grant for open-source maintainers. They receive a $200/month account for free and sell the login credentials for pure profit until Anthropic audits and bans the account.  
* **Carding (Stolen Credit Cards):** Resellers use stolen credit card information to purchase a legitimate $200 subscription, then sell the login credentials for $150. The account functions normally until the victim's bank issues a chargeback, at which point the AI provider immediately terminates the account.  
* **Secret Account Sharing:** Resellers buy one legitimate $200 account and sell the exact same login credentials to multiple buyers (e.g., three people for $130 each). They gamble that the buyers won't exceed the massive usage limits. However, concurrent logins from different IPs often trigger security flags and account suspensions.  
* **Team Plan Arbitrage:** Resellers set up fake company workspaces to access multi-user business plans (like Claude's "Team Premium" at $150/seat). They sell access to a single seat for $160, making a small, chargeback-free profit. However, the reseller remains the "Admin," meaning they can read the buyer's chat history or revoke access at any time.

### **Regional Pricing, PPP, and Currency Arbitrage**

Based on data from [OpenTheRank](https://opentherank.com/ai-pricing/), AI subscription prices fluctuate globally. Companies often adjust base prices based on a country's Purchasing Power Parity (PPP)—lowering prices in developing economies to make the software affordable, while keeping them high in wealthy nations.

Furthermore, local taxes (like VAT or GST) are added to the final price. When users in expensive regions use VPNs to purchase subscriptions from cheaper regions, they engage in **currency arbitrage**.

### **General Trends**

* **Lowest Prices (PPP Focus):** Emerging markets and regions with favorable exchange rates against the USD, such as the Philippines, Pakistan, Indonesia, and Turkey, generally enjoy the lowest prices to align with local purchasing power.  
* **Highest Prices:** Scandinavian countries (like Denmark) and the UK consistently face the highest subscription costs, largely due to high Value Added Tax (VAT) rates (e.g., Denmark's 25%).  
* **Extreme Discrepancies:** Some specialized AI tools show massive regional price gaps. For example, Kling AI has a 1219% price gap (India: $1.04/mo vs. Denmark: $13.72/mo), and Captions has a 324% price gap (Nigeria: $3.45/mo vs. Denmark: $14.64/mo).

### **Common Marketplaces for Digital Goods**

As shown in image\_0d371b.png, these are common third-party marketplaces where digital goods (including grey-market accounts) are often traded:

* [g2g.com](https://www.g2g.com/)  
* [Eldorado.gg](https://www.eldorado.gg/)  
* [Z2U](https://www.z2u.com/)  
* [PlayerAuctions](https://www.playerauctions.com/)  
* [EpicNPC](https://www.epicnpc.com/)  
* [iGV](https://www.igv.com/)  
* [Gameflip](https://gameflip.com/)  
* [G2A](https://www.g2a.com/)  
* [Kinguin](https://www.kinguin.net/)

##  **Open-Source AI Gateway & Proxy Comparison**

| Feature / Metric | OmniRoute | 9router | CLIProxyAPI | LiteLLM |  |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **Primary Language** | TypeScript / Node.js | TypeScript / Node.js | **Go** (Golang) | **Python** |  |
| **Primary Focus** | Free-tier pooling & tool setup | Context token optimization | Multi-account OAuth load-balancing | Enterprise backend proxy & governance |  |
| **Provider Support** | **290+ providers** (90+ free) | 40+ providers | OAuth \+ major LLM APIs | 100+ LLM providers |  |
| **Token Saver Tech** | RTK \+ Caveman prompt compression | ⭐ **RTK, Caveman, Ponytail, Headroom** | None (pure pass-through) | Caching only |  |
| **Multi-Account OAuth** | Supported | Supported (Round-robin) | ⭐ **Best-in-class** (Smooth failover) | Virtual Keys / Team Budgets |  |
| **GUI / Dashboard** | ⭐ Built-in Next.js App (http://localhost:20128) | Built-in Next.js App (http://localhost:20128) | Separate community Docker UI | Built-in Streamlit / Web UI |  |
| **CLI Setup Helpers** | ⭐ omniroute setup-claude, launch-codex | Manual config / CLI launch scripts | Terminal flags (--claude-login) | Config via config.yaml |  |
| **Resource Footprint** | Medium | Medium | ⚡ **Ultra-low** (Single binary) | Medium (Python runtime \+ Postgres/Redis) |  |

### **🔍 Detailed Breakdown of Each Project**

#### **1\. OmniRoute (diegosouzapw/OmniRoute)**

> * **Best For:** Developers who want an all-in-one local manager that stacks **90+ zero-config free AI tiers** and provides out-of-the-box launcher integration for Claude Code, Codex, and OpenCode.  
> * **Key Strength:** Aggregates public free pools (computing up to 1.5B free tokens/month) and handles terminal setup automatically without needing manual config edits.

#### **2\. 9router (decolua/9router)**

> * **Best For:** Terminal power-users paying per token who want to cut API costs using **aggressive prompt optimization**.  
> * **Key Strength:** Specialized token-reducing engines like **RTK** (stripping noisy git diff / grep logs), **Caveman Mode** (forcing concise LLM outputs), and **Ponytail Mode** (forcing YAGNI-first code generation).

#### **3\. CLIProxyAPI (cliproxy)**

> * **Best For:** Developers who own **multiple paid accounts** (e.g., two Claude Pro plans, three ChatGPT Plus accounts) and want a hyper-lightweight daemon to balance traffic across them.  
> * **Key Strength:** Written in pure Go for zero-overhead execution; handles token auto-refresh and account switching seamlessly when hit by rate limits.

#### **4\. LiteLLM (berriai/litellm)**

> * **Best For:** Backend developers, DevOps, and enterprises building multi-model production apps rather than local CLI coding tools.  
> * **Key Strength:** The industry standard for Python backends. Normalizes 100+ LLM providers into a unified OpenAI format with virtual keys, spend tracking per developer/team, and fallback routing.

### **💡 Summary: Which One Should You Pick?**

> * Pick **OmniRoute** if you want to run CLI coding tools for free without dealing with complex configs.  
> * Pick **9router** if your main goal is reducing token burn on paid API keys during heavy coding sessions.  
> * Pick **CLIProxyAPI** if you want a minimalist, low-RAM Go background service to rotate your personal paid subscriptions.  
> * Pick **LiteLLM** if you are building an application backend in production and need enterprise key governance.

---

*User prompt: i want to use 2 claude code accounts: compare cliproxyapi, omniroute, claude-swap*

Response: Managing **2 Claude Code accounts** to avoid hitting rate limits or 5-hour quota walls is one of the most popular workflows in AI coding. However, **claude-swap**, **CLIProxyAPI**, and **OmniRoute** handle this problem using completely different architectural approaches.

Here is a breakdown of how they compare for running multiple Claude Code accounts:

### **📊 Quick Comparison Matrix**

| Feature / Metric | claude-swap (cswap) | CLIProxyAPI | OmniRoute |
| :---- | :---- | :---- | :---- |
| **How it Works** | **Credential Profile Switcher** (Swaps \~/.claude.json files) | **Local Go HTTP Proxy** (Intercepts requests at network level) | **Full AI Gateway & UI** (Next.js proxy server) |
| **Requires Proxy / Port?** | ❌ **No proxy needed** (Direct native connection) | Yes (localhost:8317) | Yes (localhost:20128) |
| **Failover Mechanism** | Proactive swapping before hitting limits | **Mid-request 429 retry** (Transparent failover) | Quota-aware fallback & circuit breakers |
| **Parallel Terminals** | Yes (cswap run 2 pins shell session) | Yes (Transparent multi-threading) | Yes (Handled by proxy pool) |
| **Fallback Beyond Claude** | ❌ Anthropic accounts only | ⚠️ OpenAI/Codex APIs only | ⭐ **500+ models** (DeepSeek, Gemini, Free tiers) |
| **Token Compression** | ❌ None | ❌ None | ⭐ **RTK & Caveman modes** |
| **System RAM / Overhead** | ⚡ **Near zero** (Pure Python/CLI script) | ⚡ **Ultra-low** (Compiled Go binary) | Medium (Node.js \+ Web UI process) |

### **🔍 Detailed Breakdown by Tool**

#### **1\. claude-swap (cswap) — *The Native Profile Switcher***

claude-swap is a dedicated CLI tool designed specifically for managing multiple Claude Code accounts without running a proxy or proxying network traffic.

> * **How it handles 2 accounts:**  
  * It snapshots your authenticated \~/.claude/ state for Account 1 and Account 2\.  
  * **Proactive Auto-Swap (cswap auto):** Runs a background loop that monitors your 5-hour and 7-day quota usage via Anthropic's usage endpoints. When Account 1 hits your set threshold (e.g., 85% of its limit), it swaps the credential file in place to Account 2 before you ever get blocked mid-task.  
  * **Session Isolation (cswap run 2):** You can launch Account 1 in Terminal A while forcing Terminal B to run Account 2 in parallel.  
> * **Best for:** Developers who want **100% official, native Claude Code behavior** without putting a proxy server between their CLI and Anthropic, and who don't care about non-Claude models.

#### **2\. CLIProxyAPI — *The High-Performance Request Load Balancer***

CLIProxyAPI sits as a local HTTP proxy between your terminal and Anthropic's servers (ANTHROPIC\_BASE\_URL="http://localhost:8317").

> * **How it handles 2 accounts:**  
  * You complete the browser OAuth login for both Account 1 and Account 2 inside CLIProxyAPI.  
  * **Request-Level Retries:** Unlike profile switchers, CLIProxyAPI load-balances at the raw API request level. If Account 1 returns a 429 Rate Limit HTTP response mid-prompt, CLIProxyAPI immediately resends that exact HTTP payload using Account 2's token in milliseconds. Your terminal prompt never crashes or fails.  
> * **Best for:** Power users with multiple paid accounts (Pro/Max) who want **instant, zero-interruption request retries** handled by a blazing-fast background Go daemon.

#### **3\. OmniRoute — *The Multi-Account Gateway & Safety Net***

OmniRoute acts as a full-fledged local API gateway with an embedded Next.js visual dashboard.

> * **How it handles 2 accounts:**  
  * You import both Claude Code OAuth accounts into the OmniRoute dashboard.  
  * **Combos & Custom Fallback Chains:** You can define smart routing chains. For example:  
    Claude Account 1⟶Claude Account 2⟶DeepSeek-V3 / Gemini 1.5 Pro (Free)  
  * If **both** of your Claude accounts hit their 5-hour rate limits during heavy coding, OmniRoute seamlessly shifts Claude Code's backend to another top-tier model so your coding session doesn't stop.  
  * **Context Compression:** Applies RTK compression to tool outputs (like long git diff outputs) to slow down how fast both accounts burn through their 5-hour windows.  
> * **Best for:** Developers who want a **visual GUI dashboard**, token compression to preserve account limits, and an emergency fallback to other AI models when both accounts are exhausted.

### **💡 Verdict: Which Should You Pick?**

**Use claude-swap if:**

You want a simple, lightweight CLI tool that doesn't modify network traffic or run a proxy, and just automatically switches your local .json credentials before rate limits hit.

**Use CLIProxyAPI if:**

You want a low-level, high-speed Go proxy that seamlessly retries failed requests mid-session without ever dropping your terminal state.

**Use OmniRoute if:**

You want to compress context tokens (making both accounts last longer), monitor usage on a visual dashboard, and automatically fall back to free Gemini/DeepSeek models when both Claude accounts run out.

## **Links**

**Web Links (Clickable)**  
**GitHub Repositories & Tools:**

* [Alishahryar1/free-claude-code](https://github.com/Alishahryar1/free-claude-code)  
* [AminBlg/SimpleEnglish](https://github.com/AminBlg/SimpleEnglish)  
* [aidenybai/react-scan](https://github.com/aidenybai/react-scan)  
* [ast-grep/ast-grep](https://github.com/ast-grep/ast-grep)  
* [BerriAI/litellm](https://github.com/BerriAI/litellm)  
* [ccusage/ccusage](https://github.com/ccusage/ccusage)  
* [decolua/9router](https://github.com/decolua/9router)  
* [DeusData/codebase-memory-mcp](https://github.com/DeusData/codebase-memory-mcp)  
* [diegosouzapw/OmniRoute](https://github.com/diegosouzapw/OmniRoute)  
* [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail)  
* [fallow-rs/fallow](https://github.com/fallow-rs/fallow)  
* [headroomlabs-ai/headroom](https://github.com/headroomlabs-ai/headroom)  
* [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman)  
* [junhoyeo/tokscale](https://github.com/junhoyeo/tokscale)  
* [kucherenko/jscpd](https://github.com/kucherenko/jscpd)  
* [lbjlaq/Antigravity-Manager](https://github.com/lbjlaq/Antigravity-Manager)  
* [mattpocock/skills](https://github.com/mattpocock/skills)  
* [millionco/react-doctor](https://github.com/millionco/react-doctor)  
* [mnfst/awesome-free-llm-apis](https://github.com/mnfst/awesome-free-llm-apis)  
* [mnfst/manifest](https://github.com/mnfst/manifest)  
* [router-for-me/CLIProxyAPI](https://github.com/router-for-me/CLIProxyAPI)  
* [router-for-me/Cli-Proxy-API-Management-Center](https://github.com/router-for-me/Cli-Proxy-API-Management-Center)  
* [rtk-ai/rtk](https://github.com/rtk-ai/rtk)  
* [upstash/context7](https://github.com/upstash/context7)  
* [webpro-nl/knip](https://github.com/webpro-nl/knip)  
* [Wei-Shaw/sub2api](https://github.com/Wei-Shaw/sub2api)

**Articles, Documentation & Pricing Aggregators:**

* [5x for Free : The Local Coding Stack | Tomasz Tunguz](https://tomtunguz.com/local-coding-models/)  
* [AI Model & API Providers Analysis | Artificial Analysis](https://artificialanalysis.ai/)  
* [Auto Router \- API Pricing & Providers | OpenRouter](https://openrouter.ai/openrouter/auto)  
* [Cheapest AI Subscriptions by Country 2026 | OpenTheRank](https://opentherank.com/ai-pricing/)  
* [Fusion \- API Pricing & Providers | OpenRouter](https://openrouter.ai/openrouter/fusion)  
* [Models.dev \- An open-source database of AI models](https://models.dev/)  
* [Ollama](https://ollama.com/)  
* [OmniRoute/docs/reference/FREE\_PROXIES\_API.md](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/FREE_PROXIES_API.md)  
* [OmniRoute/docs/reference/FREE\_TIERS.md](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/FREE_TIERS.md)  
* [OmniRoute/docs/reference/PROVIDER\_REFERENCE.md](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/PROVIDER_REFERENCE.md)  
* [OpenCode Go | Low cost coding models for everyone](https://opencode.ai/go)  
* [Pareto Code Router \- API Pricing & Providers | OpenRouter](https://openrouter.ai/openrouter/pareto-code)  
* [Prompt Compression API | Cut LLM Token Costs | The Token Company](https://thetokencompany.com/)  
* [Sail Research — Infrastructure for long-horizon agents](https://www.sailresearch.com/)  
* [Save up to 50% on LLM costs | Batchwork](https://batchwork.com/)  
* [Software After AI | Tomasz Tunguz](https://www.tomtunguz.com/)  
* [The Open Source LLM Router for AI Agents | Manifest](https://manifest.build/)  
* [The Pulse: a new trend, smart model routing](https://newsletter.pragmaticengineer.com/p/did-anthropics-new-model-just-boost)

