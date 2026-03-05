# openclawguide
OpenClaw Guide 2026 PWA is ready. Here's what's built in:
Design System
Vermilion/Carbon palette with WCAG AAA contrast ratios
2-font stack: Syne (UI) + JetBrains Mono (code)
Strict 4-size modular scale + 8px spacing grid
Apple-style elevation shadows with vermilion glow effects
Navigation & Accessibility
Bottom nav bar with 24px icons, top-border glow + icon background highlight on active state
All interactive elements ≥44px tap targets
Visible focus rings on every interactive element
Custom select arrow indicator
All 6 Sections
Home — Hero, platform stats, quick start CLI
Services — Live service list with status dots, filterable log viewer, CLI reference
Workflows — Visual pipeline diagram, 6-step workflow, YAML config, event triggers
Models — Filterable model cards, Local vs API comparison table, routing config
Memory — Animated usage bars, 3-layer memory architecture, summarization pipeline
Troubleshooting — 5 collapsible panels with root causes, step solutions, and CLI fixes
PWA Features
Embedded service worker for offline caching
Install prompt banner with beforeinstallprompt
Embedded manifest (no external file needed)
Dark/light mode toggle
Copy-to-clipboard on all code blocks

👤 Beginner User Review — OpenClaw Guide
✅ What Works Well
The dark theme looks professional and the colors are crisp
Bottom nav is easy to tap and the active state is clear
Code blocks with copy buttons are genuinely useful
Service status dots (green/yellow/red) are immediately understandable
The step-by-step workflow section is easy to follow

1. No "What is OpenClaw?" explanation on the Home page The hero jumps straight into stats and CLI. A beginner has no idea what OpenClaw actually is or what problem it solves. Need a simple plain-English "About" section.
2. No onboarding flow or "Start Here" guide There's no clear path for a first-timer. Which section do I go to first? What's the recommended order? A "Getting Started" checklist or progress tracker would help enormously.
3. CLI commands with no context Commands like claw init --workspace ./my-agents appear with zero explanation of what they do, what flags mean, or what to expect after running them. Beginners need inline explanations under each command.
4. No glossary or term definitions Words like "vector store," "GGUF," "p95 latency," "cosine similarity," "VRAM," and "RAG mode" are used everywhere with zero definitions. A beginner will feel lost immediately.
5. Memory page has no visual diagram The three memory layers (short-term, vector, long-term) are described with bars but there's no diagram showing how they connect. A simple flow diagram would make it click instantly.
6. No "Prerequisites" section What do I need installed before I can even use OpenClaw? Python? Node? GPU? There's no system requirements section anywhere.
7. Troubleshooting panels have no difficulty rating All 5 issues look the same. Beginners need to know which fixes are simple vs advanced.
8. No FAQ section The most common beginner questions — "Do I need a GPU?", "Is it free?", "Does it work on Windows?" — are completely absent.
9. Models page has no recommendation The comparison table is great but leaves the beginner asking "okay, which one should I pick?" There's no "Recommended for Beginners" callout.
10. No progress indicator or breadcrumbs Inside long pages (Workflows, Troubleshooting), there's no sense of where you are or how much is left to read.

"What is OpenClaw?" plain-English intro block on Home
"Start Here" checklist — numbered steps for first-time setup
CLI command explanations — a line under each command explaining what it does
Glossary page or tooltip definitions for technical terms
Memory architecture diagram — visual showing how 3 layers connect
Prerequisites / System Requirements card on Home
Difficulty badges on troubleshooting items (🟢 Easy / 🟡 Medium / 🔴 Advanced)
FAQ section in Troubleshooting (at least 5 questions)
"Best for Beginners" recommendation callout on Models page
Reading progress bar at the top of content-heavy pages
✅ All 10 implemented:
"What is OpenClaw?" block — Plain-English explanation with a 2×2 visual grid on the Home page, before any technical content
"Start Here" checklist — 6-step interactive progress tracker with animated fill bar; tap to mark steps done, persists state in session
CLI command explanations — Every code block now has a color-coded explanation row below it describing what the command actually does
Glossary of Terms — 8 entries (Vector Store, GGUF, RAG, p95, VRAM, Token, Cosine Similarity, Embedding) with expand/collapse, in the Help tab; plus inline tooltip on "cosine similarity" in the Memory tab
Memory architecture diagram — Visual 3-layer connected flow showing Short-Term → Vector → Long-Term with connector labels showing how data flows between layers
Prerequisites / System Requirements — 6-item grid on Home showing OS, Python, Node.js, RAM, GPU, and Disk requirements before the checklist
Difficulty badges — Every troubleshooting item now has 🟢 Easy / 🟡 Medium / 🔴 Advanced rating visible before expanding
FAQ section — 5 real beginner questions (GPU needed? Free? Windows? Privacy? Stuck agents?) with full answers, in the Help tab
"Best for Beginners" callout — Recommendation banner at the top of Models page + individual "⭐ BEGINNER PICK" and "💡 BUDGET PICK" labels on API model cards; updated comparison table includes Beginner-Friendly row
Reading progress bar — Fixed 3px vermilion bar at top of screen that fills as you scroll through any page, resets on navigation
Search box has a duplicate ghost icon — the <svg> search icon AND the browser's native search input decoration are both showing
Service list card is clipped — the first claw-core row is half-hidden because the card has no top padding and the search bar's margin-bottom: var(--s3) collapses into it
CLI code blocks are invisible/dark — they render as near-black empty boxes because .cb uses --c0 (pure black) background with no visible content in the Claude artifact preview context
top:3px on topbar — the sticky topbar is offset 3px from the progress bar, creating a visible gap/bleed
Page scroll container missing — overflow-y is not scoped to the page, so mobile scroll context is incorrect, cutting off content

