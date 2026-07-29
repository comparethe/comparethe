# ChatGPT Atlas Migration Post Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Publish a sourced first-person post recommending what to use after ChatGPT Atlas shuts down.

**Architecture:** Add one root-level Markdown page that combines a personal migration narrative with a compact product comparison. Keep future blog organization out of scope; use first-party web sources and a dated research snapshot so volatile claims remain auditable.

**Tech Stack:** Markdown, Flowershow/Obsidian-style wiki links, first-party product documentation

---

### Task 1: Verify the migration landscape

**Files:**
- Reference: `docs/plans/2026-07-29-chatgpt-atlas-migration-design.md`
- Create: `ChatGPT Atlas is shutting down.md`

**Step 1: Verify OpenAI's migration path**

Check OpenAI's Atlas retirement notice and built-in browser documentation. Record the shutdown date, export guidance, desktop-browser capabilities, cloud-browser limitations, plan requirements, and download location.

**Step 2: Verify browser-first alternatives**

Check first-party documentation and pricing for Dia and Perplexity Comet. Record supported platforms, free/paid availability, browser-context chat, agent capability, and download links.

**Step 3: Verify conventional-browser integrations**

Check first-party documentation and pricing for Gemini in Chrome, Claude in Chrome, Brave Leo, and Edge Copilot. Record availability constraints and whether each product offers page-aware chat, multi-tab context, or agentic actions.

**Step 4: Choose the recommendation**

Rank options against the four requirements in the design note. Separate an immediately usable recommendation in Europe from promising but region-limited options.

### Task 2: Write the post

**Files:**
- Create: `ChatGPT Atlas is shutting down.md`

**Step 1: Add front matter and opening**

Add `title`, `description`, `created`, and `updated` fields. Open in first person with the shutdown date and the short recommendation.

**Step 2: Explain the requirements and market map**

Describe what worked about Atlas, distinguish passive browsing from AI usage, and explain the three replacement shapes: AI app with browser, AI-native browser, and conventional browser with AI integration.

**Step 3: Add the comparison table**

Include price, platform, where the AI lives, page/tab context, agent mode, immediate fit, and official download/product link. Mark volatile or rollout-dependent information.

**Step 4: Add option assessments and migration checklist**

Give concise sections for the serious candidates, then list steps to export bookmarks, save open tabs, install the first-choice replacement, and run a short trial.

**Step 5: Add a visual walkthrough**

Explain exactly where to open ChatGPT's built-in browser in the desktop app. Add clearly attributed first-party product imagery where it helps readers understand the interface; do not fabricate UI screenshots.

**Step 6: Add open questions, sources, and transcript appendix**

Keep unresolved hands-on judgments explicit. Provide first-party sources and a cleaned, faithful version of the original dictated request.

### Task 3: Verify and commit

**Files:**
- Verify: `ChatGPT Atlas is shutting down.md`
- Verify: `assets/dia-browser-chat.png`
- Verify: `docs/plans/2026-07-29-chatgpt-atlas-migration.md`

**Step 1: Check document structure**

Run:

```bash
rg -n '^(---|#|##|\|)' 'ChatGPT Atlas is shutting down.md'
```

Expected: front matter, one H1, all planned H2 sections, and a well-formed comparison table are visible.

**Step 2: Check links and whitespace**

Run:

```bash
rg -o 'https://[^)> ]+' 'ChatGPT Atlas is shutting down.md'
git diff --check
```

Expected: first-party links are present and `git diff --check` exits successfully with no output.

**Step 3: Inspect the final diff**

Run:

```bash
git diff -- 'ChatGPT Atlas is shutting down.md' assets/dia-browser-chat.png docs/plans/2026-07-29-chatgpt-atlas-migration.md
```

Expected: only the planned post and implementation plan are added after the design commit.

**Step 4: Commit**

```bash
git add 'ChatGPT Atlas is shutting down.md' assets/dia-browser-chat.png docs/plans/2026-07-29-chatgpt-atlas-migration.md
git commit -m "add ChatGPT Atlas migration comparison"
```
