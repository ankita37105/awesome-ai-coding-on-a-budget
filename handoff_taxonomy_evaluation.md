# Handoff: Taxonomy Evaluation for awesome-ai-coding-on-a-budget

## **Executive Summary**

The objective of this project is to build a comprehensive, production-grade `README.md` for the GitHub repository [`mrtnrocks/awesome-ai-coding-on-a-budget`](https://github.com/mrtnrocks/awesome-ai-coding-on-a-budget). 

The repository serves as a practical, multi-angle resource guide for developers, solo builders, and engineering teams aiming to conduct cost-efficient AI-assisted software engineering. The project approaches cost reduction not only through free/cheap LLM APIs and proxy gateways, but also through token compression, deterministic quality guardrails ("fixing vibe coding"), context preservation, and pre-agent architectural discipline.

The source materials are indexed in [`SOURCES.md`](file:///C:/Users/mrtn/code/awesome-ai-coding-on-a-budget/SOURCES.md).

---

## **Current State & Progress**

1. **Wayfinder Initialization:** The `/wayfinder` skill was invoked to chart the path forward.
2. **GitHub Label Setup:** Canonical GitHub labels have been created on the repository (`wayfinder:map`, `wayfinder:research`, `wayfinder:prototype`, `wayfinder:grilling`, `wayfinder:task`, `ready-for-agent`, `ready-for-human`, `needs-triage`, `needs-info`).
3. **Scope Alignment:** A preliminary 7-section taxonomy was drafted based on user input and `SOURCES.md`.
4. **Current Focus:** The incoming agent must evaluate this 7-section taxonomy for completeness, clarity, categorization gaps, and logical flow before the Wayfinder map issue is published to GitHub.

---

## **Proposed 7-Section Taxonomy with Examples**

### **1. Model Selection & Benchmarking**
* **Focus:** Benchmark-driven model selection matching task requirements to intelligence-per-dollar efficiency.
* **Key Tools & Resources:**
  * [LMSYS Chatbot Arena Leaderboard](https://arena.ai/leaderboard) (general & coding benchmarks)
  * [DeepSWE Leaderboard](https://deepswe.datacurve.ai) (software engineering capabilities)
  * [Artificial Analysis](https://artificialanalysis.ai/#price-and-cost) (cost per million tokens, latency, quality)
  * [Models.dev](https://models.dev) (open-source model specification & pricing database)
* **Evaluation Approach:** Cross-reference leaderboard rankings (LMSYS, DeepSWE) against cost-per-token data (Artificial Analysis, Models.dev) to identify Pareto-optimal models per task class (planning, execution, code review).

### **2. LLM Gateways, Routing, API Proxies & Multi-Account Rotation**
* **Focus:** Centralizing access, dynamic model routing, aggregating free-tier pools, multi-account OAuth rotation, transparent 429 failover, and usage monitoring.
* **Key Tools & Resources:**
  * **OmniRoute** (`diegosouzapw/OmniRoute`): Aggregates 290+ providers & 90+ free pools with built-in CLI launchers.
    * [Provider Reference Spec](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/PROVIDER_REFERENCE.md) | [Free Tiers Methodology](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/FREE_TIERS.md) | [Free Proxies API](https://github.com/diegosouzapw/OmniRoute/blob/main/docs/reference/FREE_PROXIES_API.md)
  * **9router** (`decolua/9router`): Multi-account rotation with built-in RTK/Caveman compression modes.
  * **CLIProxyAPI** (`router-for-me/CLIProxyAPI`): High-performance Go background daemon for OAuth account load-balancing.
  * **CLI Proxy Management Center** (`router-for-me/Cli-Proxy-API-Management-Center`): WebUI dashboard for CLIProxyAPI managing runtime status, OAuth flows, auth files, quotas, and request logs.
  * **claude-swap** (`cswap`): Native CLI credential profile switcher for multiple Claude Code accounts with proactive auto-swap before rate limits hit.
  * **LiteLLM** (`BerriAI/litellm`): Enterprise Python/Rust proxy standardizing 100+ LLM APIs.
  * **Manifest** (`mnfst/manifest`): Open-source gateway supporting 300+ models.
  * **Sail Research** (`sail.services`): Long-horizon agent infrastructure providing cost-efficient inference and Sailboxes (VMs) for autonomous background workflows.
  * **Batchwork** (`batchwork.dev`): Unified batch processing library — up to 50% savings vs. real-time API calls.
  * [Awesome Free LLM APIs](https://github.com/mnfst/awesome-free-llm-apis): Curated index of permanent free-tier LLM API keys.
  * **Sub2API** (`Wei-Shaw/sub2api`), **Free Claude Code** (`Alishahryar1/free-claude-code`), **Antigravity-Manager** (`lbjlaq/Antigravity-Manager`).
* **Routing & Orchestration:**
  * OpenRouter Auto Router (`openrouter/auto`)
  * OpenRouter Fusion Router (`openrouter/fusion`)
  * OpenRouter Pareto Code Router (`openrouter/pareto-code`)
  * Manifest Dynamic Routing (`manifest.build`)
* **Usage & Cost Monitoring:**
  * **tokscale** (`junhoyeo/tokscale`): Terminal CLI and global leaderboard tracking token consumption and cost across 30+ agent environments.
  * **ccusage** (`ccusage/ccusage`): CLI analytics summarizing token spend across Claude Code, Codex, OpenCode, Goose, Droid, and other agent platforms.

### **3. Token Optimization & Prompt Compression**
* **Focus:** Context reduction, terminal output filtering, and agent response concise enforcement to prevent token waste.
* **Key Tools & Resources:**
  * **Runtime Token Kit (RTK)** (`rtk-ai/rtk`): Rust CLI proxy compressing shell outputs (git diff, grep, cargo test) by 60–90%.
  * **Headroom** (`headroomlabs-ai/headroom`): Reversible context compression engine (CCR & Kompress models).
  * **Caveman Mode** (`JuliusBrussee/caveman`): Agent skill enforcing concise output without fluff, saving 65% tokens.
  * **Ponytail** (`DietrichGebert/ponytail`): YAGNI agent skill enforcing minimal code changes (-54% code bloat).
  * **SimpleEnglish** (`AminBlg/SimpleEnglish`): ASD-STE100 technical English rules eliminating slop.
  * **The Token Company API** (`thetokencompany.com`).
* **Research:** Technical Taxonomy of Token Optimization — comparative study evaluating paradigms across WOZCODE, Token Optimizer, Token Savior, RTK, and Graphify.

### **4. Codebase Intelligence, RAG & MCP Context Preservation**
* **Focus:** Low-token, high-precision context retrieval using knowledge graphs and version-accurate docs without overloading context windows.
* **Key Tools & Resources:**
  * **Codebase Memory MCP** (`DeusData/codebase-memory-mcp`): Tree-sitter SQLite knowledge graph indexing 158 languages (120x token reduction over grep/file dumps).
  * **Context7** (`upstash/context7`): Real-time versioned documentation retriever via MCP.

### **5. Agent Harnesses, Skills & Quality Guardrails ("Fixing Vibe Coding")**
* **Focus:** Workflow skills, deterministic linters, pre-commit pipelines, headless browser verification, and foundational architectural choices prior to delegating tasks to agents.
* **Key Tools & Resources:**
  * **Matt Pocock Agent Skills** (`mattpocock/skills`): `/grill-me`, `/wayfinder`, `/tdd`, `/to-spec`, `/implement`.
  * **Fallow** (`fallow-rs/fallow`): Static analysis for TypeScript/JS tracking circular dependencies & complexity.
  * **jscpd** (`kucherenko/jscpd`): Duplicate code detector across 223 formats.
  * **Knip** (`webpro-nl/knip`): Unused exports and dependencies finder.
  * **AST-Grep** (`ast-grep/ast-grep`): Structural code search and pattern matching against ASTs.
  * **Project Wallace** (`projectwallace/wallace-cli`): Detects bloated CSS — AI-generated duplicate colors, redundant font-size/line-height declarations.
  * **Sentry CLI** & **Spotlight** (`spotlightjs.com`): Giving agents direct dev logs and runtime trace access.
  * **Storybook AI** (`storybook.js.org/ai`): Component discovery via MCP — prevents agents from reinventing existing UI components.
  * **Dex** & **Beads**: Deterministic Git/JSON-backed task trackers maintaining strict agent execution sequences and task dependencies.
  * **8 Tech Choices Before Agentmaxxing:** Establishing strict schema (Zod/Valibot), TypeScript types, folder structures, and client-server comms upfront.
* **Linting & Custom Guardrails:**
  * **ESLint** / **Stylelint**: Write custom rules targeting AI antipatterns (e.g., overusing `as` assertions, unnecessary `useEffect`).
  * **Clint** (`stolinski/clint`): Composable linting utilities.
  * **Ultracite** (`ultracite.ai`): Modern Rust-based linting engine.
  * **Vite+** (`viteplus.dev`): Fast zero-config typecheck → lint → complexity scan pipeline.
* **Headless Browser Verification:**
  * **Agent Browser** (`vercel-labs/agent-browser`): Gives agents screenshot/DOM/network access for self-correcting UI bugs.
  * **LightPanda** (`lightpanda.io`): High-performance Zig/V8 headless browser engine.
  * **Chrome DevTools MCP** (`ChromeDevTools/chrome-devtools-mcp`): Direct browser DevTools access for agents.
* **React-Specific Quality:**
  * **react-scan** (`aidenybai/react-scan`): React performance profiling.
  * **react-doctor** (`millionco/react-doctor`): React health diagnostics.

### **6. Local Runtimes & Self-Hosted Inference**
* **Focus:** Running LLMs on local hardware for zero-cost inference and full data privacy.
* **Key Tools & Resources:**
  * **Ollama** (`ollama.com`): Local LLM runner with model library and OpenAI-compatible API.
  * **Hermes** (NousResearch): Instruction-tuned open models optimized for function calling and agent workflows.
  * **OpenCode Go** (`opencode.ai/go`): Low-cost local coding models.
  * **open-design.ai**: Open-source design-to-code local inference.

### **7. Pricing Intelligence, Deals & Grey Market Awareness**
* **Focus:** Regional purchasing power parity (PPP) pricing, open-source maintainer grants, and grey market risk awareness.
* **Key Resources:**
  * **Pricing & PPP Arbitrage:** [OpenTheRank AI Pricing Analysis](https://opentherank.com/ai-pricing/) (PPP global gaps up to 1200%), Open-Source Maintainer Grants (e.g. Anthropic OSS grants).
* **⚠️ Grey Market Awareness & Warnings:**
  * Understanding risks of account sharing, carding, open-source grant loopholes, and seller admin access on marketplaces (G2G, Eldorado, Z2U).
  * This section exists to inform readers about **what to avoid**, not to endorse these practices.

---

## **Suggested Skills for the Incoming Agent**

1. **`research`**: Run targeted background lookups if additional cost-reduction tools or frameworks need to be verified.
2. **`domain-modeling`**: Create/update `CONTEXT.md` to formalize domain terms (e.g., *Model Tiering*, *Token Compression*, *Vibe Coding Guardrails*).
3. **`wayfinder`**: Chart the map issue (`gh issue create --label wayfinder:map`) and create child decision tickets once the 7-section taxonomy is finalized.
4. **`grilling`**: Use if further clarifying questions are needed from the human maintainer regarding section ordering or inclusions.

---

## **Next Steps for the Agent**

1. **Review & Evaluate:** Read `SOURCES.md` and assess whether the 7 sections fully cover all listed tools and concepts, or if any section should be split, combined, or reordered.
2. **Confirm Taxonomy:** Present any recommendations or confirm readiness to the user.
3. **Chart Wayfinder Issue Map:** Execute `gh issue create` to publish the Wayfinder map on GitHub and create child tickets for drafting each section of `README.md`.
