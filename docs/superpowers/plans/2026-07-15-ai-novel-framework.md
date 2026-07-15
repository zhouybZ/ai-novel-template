# AI Novel Framework Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Turn the empty AI novel directory scaffold into a usable Markdown template for AI-assisted long-form serial fiction.

**Architecture:** Keep the framework file-based and Markdown-only. Use `AGENTS.md` as the AI operating contract, `README.md` as the project entry, numbered directories for domain data, `prompts/` for repeatable AI workflows, and production directories for draft-review-publish flow.

**Tech Stack:** Markdown files, Git, shell verification with `rg` and `wc`.

---

### Task 1: Project Entry And AI Contract

**Files:**
- Modify: `README.md`
- Modify: `AGENTS.md`
- Modify: `00_规则/总体规则.md`
- Modify: `00_规则/文风规范.md`
- Modify: `00_规则/禁止事项.md`

- [ ] **Step 1: Fill project entry**

Write a practical `README.md` with project metadata fields, directory purpose, initialization sequence, and standard chapter workflow.

- [ ] **Step 2: Fill AI contract**

Write `AGENTS.md` with required pre-read files, write workflow, post-write updates, edit boundaries, and output rules.

- [ ] **Step 3: Fill rule templates**

Write the three rule files with stable sections for continuity, style, and prohibited behaviors.

### Task 2: Setting And Character Templates

**Files:**
- Modify: `01_小说设定/*.md`
- Modify: `02_人物档案/*.md`

- [ ] **Step 1: Fill setting files**

Add structured fields for positioning, worldbuilding, cultivation system, factions, map, and glossary.

- [ ] **Step 2: Fill character files**

Add structured fields for protagonist, antagonist, supporting cast, and relationship network.

### Task 3: Plot And Memory Templates

**Files:**
- Modify: `03_剧情规划/*.md`
- Modify: `04_动态记忆/*.md`

- [ ] **Step 1: Fill plot planning files**

Add structured templates for whole-book outline, volume outline, future 20-chapter rough outline, future 5-chapter detailed outline, and current chapter card.

- [ ] **Step 2: Fill dynamic memory files**

Add structured tracking tables for timeline, character state, world state, foreshadowing, recovered foreshadowing, and recent chapter summaries.

### Task 4: Prompts And Production Docs

**Files:**
- Create: `prompts/写新章节.md`
- Create: `prompts/审核章节.md`
- Create: `prompts/更新动态记忆.md`
- Create: `prompts/生成未来5章细纲.md`
- Create: `prompts/伏笔检查.md`
- Modify: `docs/AI工作流.md`
- Modify: `docs/平台运营.md`
- Modify: `docs/剧情节奏分析.md`
- Modify: `docs/TODO.md`
- Modify: `docs/发布计划.md`
- Modify: `docs/创作计划.md`

- [ ] **Step 1: Add prompt files**

Each prompt must define role, inputs, task, output, restrictions, and completion criteria.

- [ ] **Step 2: Fill operating docs**

Add concise templates for workflow, platform operations, rhythm analysis, task queue, release plan, and creation plan.

### Task 5: Verification And Commit

**Files:**
- Check: all modified Markdown files

- [ ] **Step 1: Check for empty Markdown files**

Run: `find . -name '*.md' -type f -size 0 -print`
Expected: no critical framework files remain empty.

- [ ] **Step 2: Check for unresolved placeholders**

Run: `rg -n "TBD|TODO|待定|占位"`
Expected: no accidental unresolved placeholder in the template content except intentional task labels.

- [ ] **Step 3: Review git diff**

Run: `git diff --stat` and `git diff --check`
Expected: no whitespace errors.

- [ ] **Step 4: Commit**

Run: `git add . && git commit -m "docs: complete ai novel framework template"`
Expected: commit succeeds.
