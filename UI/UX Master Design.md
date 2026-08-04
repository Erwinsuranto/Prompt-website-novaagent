








# 
```


```
# 
```


```
# 
```


```
# 
```


```
# 
```


```
# 
```

Before answering, inspect the current workspace. Confirm you can read the repository. List the project root files, detect package.json, run pwd and git status. If the repository is accessible, continue implementing Prompt 37. Do not claim you cannot access the repo unless these checks fail
```
# Prompt 37 — Observability, Security & Policy Engine
```

# Prompt 37 — Observability, Security & Policy Engine

Continue NovaAgent from the current repository state.

IMPORTANT

- Do NOT rewrite completed modules.
- Preserve all functionality from Prompts 26–36.
- Keep all tests green.

==================================================
OBJECTIVE
==================================================

Implement enterprise-grade observability,
security, policy enforcement, auditing,
and runtime governance.

NovaAgent remains the controller.

==================================================
1. Audit Engine
==================================================

Log every action.

Include:

- AI request
- AI response
- Tool invocation
- Terminal command
- File changes
- Git operations
- Deployment events

==================================================
2. Policy Engine
==================================================

Implement policies.

Examples:

Allow

Warn

Require Confirmation

Block

Policies may target:

terminal

filesystem

git

deployment

browser

plugins

==================================================
3. Permission System
==================================================

Support:

Workspace permissions

Tool permissions

Plugin permissions

Provider permissions

==================================================
4. Secrets Protection
==================================================

Never expose secrets.

Detect:

API keys

Passwords

Private keys

Tokens

Automatically redact logs.

==================================================
5. Runtime Monitoring
==================================================

Track:

CPU

Memory

Execution time

Retries

Agent activity

Tool usage

Provider usage

==================================================
6. Incident Recovery
==================================================

Detect:

stuck task

crash

timeout

memory leak

Automatically recover when possible.

==================================================
7. Security Review
==================================================

ReviewerAI performs:

Security review

Dependency review

Permission review

Risk classification

==================================================
8. Documentation
==================================================

Update:

README.md

CURRENT_STATE.md

IMPLEMENTATION_PLAN.md

CHANGELOG.md

Create:

SECURITY.md

AUDIT_GUIDE.md

==================================================
9. Validation
==================================================

Run until green:

pnpm typecheck

pnpm lint

pnpm test

pnpm build

==================================================
10. Final Report
==================================================

Output:

Implemented modules

Security architecture

Audit architecture

Policy engine

Files added

Files modified

Tests added

Build status

Lint status

Typecheck status

Production readiness

Remaining work

Do not stop until every requirement above is complete.
```

# Prompt 36 — Cloud & Deployment Agent
```
# Prompt 36 — Cloud & Deployment Agent

Continue NovaAgent from the current repository state.

IMPORTANT

- Do NOT rewrite completed modules.
- Preserve all functionality from Prompts 26–35.
- Keep all tests green.

==================================================
OBJECTIVE
==================================================

Implement a production-ready Cloud & Deployment Agent.

NovaAgent must be able to build, package, deploy,
monitor, and rollback applications.

==================================================
1. Deployment Agent
==================================================

Implement DeploymentAgent.

Support:

- deployment planning
- environment detection
- pre-flight validation
- deployment execution
- deployment rollback

==================================================
2. Deployment Targets
==================================================

Support adapters for:

- Docker
- Docker Compose
- Local Linux Server
- VPS
- Static Site

Architecture must allow adding more providers later.

==================================================
3. Environment Manager
==================================================

Manage:

- .env
- secrets
- environment profiles
- staging
- production
- development

==================================================
4. Build Pipeline
==================================================

Support:

- build
- package
- artifact generation
- checksum
- release bundle

==================================================
5. Health Checks
==================================================

Verify:

- service running
- HTTP endpoint
- logs
- startup timeout
- restart detection

==================================================
6. Rollback
==================================================

Automatic rollback if deployment fails.

Support:

- previous build
- previous artifact
- previous environment

==================================================
7. Monitoring
==================================================

Track:

deployment history

deployment duration

success rate

rollback count

==================================================
8. Documentation
==================================================

Update:

README.md

CURRENT_STATE.md

IMPLEMENTATION_PLAN.md

CHANGELOG.md

Create:

DEPLOYMENT_GUIDE.md

==================================================
9. Validation
==================================================

Run until all pass:

pnpm typecheck

pnpm lint

pnpm test

pnpm build

==================================================
10. Final Report
==================================================

Output:

Implemented modules

Deployment architecture

Supported deployment targets

Files added

Files modified

Tests added

Build status

Lint status

Typecheck status

Production readiness

Remaining work

Do not stop until everything above is complete.

```

# Prompt 35 — Plugin System & MCP Platform
```

# Prompt 35 — Plugin System & MCP Platform

Continue NovaAgent from the current repository state.

IMPORTANT

- Do NOT rewrite completed modules.
- Preserve all functionality from Prompts 26–34.
- Keep all tests green.
- Extend the existing architecture.

==================================================
OBJECTIVE
==================================================

Transform NovaAgent into an extensible platform by
implementing a production-ready Plugin System and
Model Context Protocol (MCP) integration.

NovaAgent remains the controller.

==================================================
1. Plugin Manager
==================================================

Implement:

- Plugin Registry
- Plugin Loader
- Plugin Lifecycle
- Plugin Metadata
- Plugin Versioning
- Plugin Dependencies
- Enable / Disable Plugin
- Hot Reload (development)

==================================================
2. Plugin SDK
==================================================

Provide an SDK for plugin developers.

Support:

- Tool registration
- Event hooks
- Command registration
- Configuration
- Logging
- Storage
- Permissions

==================================================
3. Plugin Sandbox
==================================================

Every plugin runs in an isolated environment.

Support:

- Resource limits
- Permission checks
- Safe execution
- Crash isolation
- Plugin timeout

==================================================
4. MCP Client
==================================================

Implement MCP Client.

Support:

- Multiple MCP Servers
- Auto Discovery
- Tool Discovery
- Tool Metadata
- Version Negotiation
- Connection Retry
- Health Check

==================================================
5. Tool Registry
==================================================

Merge built-in tools and MCP tools into a unified registry.

Support:

- Search
- Categories
- Permissions
- Version
- Availability
- Dynamic loading

==================================================
6. Plugin Marketplace Foundation
==================================================

Implement backend foundation for:

- Install
- Update
- Remove
- Verify
- Signature validation
- Compatibility checks

(No UI redesign.)

==================================================
7. Integration
==================================================

PlannerAI can discover tools dynamically.

CoderAI can request plugin tools.

ReviewerAI validates plugin outputs.

BrowserAgent can discover plugin documentation.

==================================================
8. Documentation
==================================================

Update:

README.md

CURRENT_STATE.md

IMPLEMENTATION_PLAN.md

CHANGELOG.md

Create:

PLUGIN_SDK.md

MCP_GUIDE.md

==================================================
9. Validation
==================================================

Run until green:

pnpm typecheck

pnpm lint

pnpm test

pnpm build

Fix every issue.

==================================================
10. Final Report
==================================================

Output:

Implemented modules

Plugin architecture

MCP architecture

SDK overview

Files added

Files modified

Tests added

Build status

Lint status

Typecheck status

Production readiness

Remaining work

Do not stop until every requirement above is complete.
```
# Prompt 34 — Browser Agent & Documentation Intelligence
```
# Prompt 34 — Browser Agent & Documentation Intelligence

Continue NovaAgent from the current repository state.

IMPORTANT

- Do NOT rewrite completed modules.
- Preserve all functionality from Prompts 26–33.
- Keep all tests green.
- Extend the existing architecture.

==================================================
OBJECTIVE
==================================================

Implement a Browser Agent capable of retrieving,
understanding, caching, and citing official
documentation before generating code.

NovaAgent remains the controller.

==================================================
1. Browser Agent
==================================================

Implement BrowserAgent.

Support:

- HTTP/HTTPS browsing
- HTML parsing
- Markdown parsing
- robots.txt awareness
- configurable timeout
- retry
- download cancellation

==================================================
2. Documentation Sources
==================================================

Support official documentation for:

- React
- Next.js
- TypeScript
- Node.js
- Prisma
- Tailwind
- Express
- Fastify
- Docker
- Git
- pnpm
- npm

Architecture must allow adding new providers.

==================================================
3. Documentation Search
==================================================

Implement:

keyword search

page search

heading search

API reference search

version-aware search

==================================================
4. Documentation Cache
==================================================

Store:

downloaded pages

metadata

version

timestamp

ETag/Last-Modified

Support refresh and offline reuse.

==================================================
5. Intelligent Retrieval
==================================================

Before asking CoderAI to generate code:

Check local memory.

Check documentation cache.

Fetch official documentation if needed.

Return structured context.

==================================================
6. Citation Engine
==================================================

Track:

documentation source

page title

section

URL

retrieval time

Include citations in execution report.

==================================================
7. Integration
==================================================

PlannerAI may request BrowserAgent.

CoderAI receives retrieved context.

ReviewerAI verifies implementation against
official documentation when available.

==================================================
8. Documentation
==================================================

Update:

README.md

CURRENT_STATE.md

IMPLEMENTATION_PLAN.md

CHANGELOG.md

==================================================
9. Validation
==================================================

Run until green:

pnpm typecheck

pnpm lint

pnpm test

pnpm build

Fix every issue.

==================================================
10. Final Report
==================================================

Output:

Implemented modules

Supported documentation providers

Files added

Files modified

Tests added

Build status

Lint status

Typecheck status

Production readiness

Remaining work

Do not stop until every requirement above is complete.

```
# Prompt 33 — Git Intelligence & Workspace Management
```
# Prompt 33 — Git Intelligence & Workspace Management

Continue NovaAgent from the current repository state.

IMPORTANT

- Do NOT rewrite completed modules.
- Preserve all functionality from Prompts 26–32.
- Extend the existing runtime.
- Keep all tests green.

==================================================
OBJECTIVE
==================================================

Implement an intelligent Git and Workspace Management
system allowing NovaAgent to safely manage repositories,
branches, commits, rollbacks, and multiple workspaces.

==================================================
1. Workspace Manager
==================================================

Implement:

- Multiple Workspaces
- Active Workspace
- Workspace Metadata
- Workspace Isolation
- Workspace Switching
- Workspace Snapshot

==================================================
2. Git Intelligence
==================================================

Implement:

- Repository Detection
- Branch Detection
- Dirty Workspace Detection
- Commit History Analysis
- File Change Analysis
- Conflict Detection

==================================================
3. Automatic Branch Strategy
==================================================

Support:

Create feature branch automatically.

Reuse branch when appropriate.

Protect main/master.

Support configurable branch naming.

==================================================
4. Smart Commit Engine
==================================================

Generate:

Commit Message

Commit Summary

Changed Files

Breaking Change Detection

Support:

Conventional Commits

==================================================
5. Diff Engine
==================================================

Generate structured diff.

Categorize:

Added

Modified

Deleted

Renamed

Binary

Large Files

==================================================
6. Safe Rollback
==================================================

Support:

Undo last patch

Undo session

Restore branch

Restore workspace snapshot

==================================================
7. Multi-Workspace Execution
==================================================

Each workspace has:

Own memory

Own git state

Own execution history

Own terminal session

Own AI context

==================================================
8. Review Before Commit
==================================================

Before commit:

ReviewerAI checks:

Diff

Commit message

Architecture impact

Security

Regression

Reject if needed.

==================================================
9. Documentation
==================================================

Update:

README.md

CURRENT_STATE.md

IMPLEMENTATION_PLAN.md

CHANGELOG.md

==================================================
10. Validation
==================================================

Run until all pass:

pnpm typecheck

pnpm lint

pnpm test

pnpm build

Fix every issue.

==================================================
11. Final Report
==================================================

Output:

Implemented modules

Workspace architecture

Git architecture

Files added

Files modified

Tests added

Build status

Lint status

Typecheck status

Production readiness

Remaining work

Do not stop until every requirement above is complete.

```

# Prompt 32 — Autonomous Coding Loop
```
# Prompt 32 — Autonomous Coding Loop

Continue NovaAgent from the current repository state.

IMPORTANT

- Do NOT rewrite completed modules.
- Preserve all functionality from Prompts 26–31.
- Extend the existing runtime.
- Keep all tests green.

==================================================
OBJECTIVE
==================================================

Implement a fully autonomous coding loop where
NovaAgent can complete a coding task from start
to finish with minimal user intervention.

NovaAgent remains the controller.

==================================================
1. Goal Execution Engine
==================================================

Accept one high-level goal.

Example:

"Implement JWT authentication."

Create execution session.

Track progress.

Support pause/resume.

==================================================
2. Autonomous Loop
==================================================

Workflow

Receive Goal

↓

PlannerAI

↓

Execution Plan

↓

CoderAI

↓

Generate Patch

↓

NovaAgent

Apply Patch

↓

Run

Typecheck

Lint

Tests

Build

↓

ReviewerAI

↓

PASS?

YES → Finish

NO

↓

Feedback

↓

CoderAI

↓

Generate Improved Patch

↓

Repeat

Support configurable retry limit.

==================================================
3. Automatic Error Classification
==================================================

Categorize failures.

Examples:

TypeScript

ESLint

Runtime

Unit Test

Build

Dependency

Security

Regression

==================================================
4. Smart Retry
==================================================

Retry only failed areas.

Reuse previous successful work.

Avoid duplicate edits.

==================================================
5. Rollback Engine
==================================================

Automatic rollback.

Support:

failed patch

failed build

failed test

manual cancel

==================================================
6. Progress Reporting
==================================================

Expose:

Current Step

Current Agent

Retries

Completed Tasks

Remaining Tasks

Execution Timeline

==================================================
7. Review Feedback Loop
==================================================

ReviewerAI returns structured feedback.

CoderAI must fix only rejected items.

Repeat until accepted.

==================================================
8. Safety
==================================================

Never delete project files without confirmation.

Prevent infinite retry loops.

Limit repeated identical patches.

==================================================
9. Documentation
==================================================

Update

README.md

CURRENT_STATE.md

IMPLEMENTATION_PLAN.md

CHANGELOG.md

==================================================
10. Validation
==================================================

Run until green:

pnpm typecheck

pnpm lint

pnpm test

pnpm build

Fix every issue.

==================================================
11. Final Report
==================================================

Output:

Implemented modules

Architecture summary

Files added

Files modified

Tests added

Retry statistics

Build status

Lint status

Typecheck status

Production readiness

Remaining work

Do not stop until every requirement above is complete.

```

# Prompt 31 — AI Provider Manager & Review Pipeline
```
# Prompt 31 — AI Provider Manager & Review Pipeline

Continue NovaAgent from the current repository state.

IMPORTANT

- Do NOT rewrite completed modules.
- Preserve all functionality from Prompts 26–30.
- Extend the current architecture.
- Build production-ready provider abstraction.

==================================================
OBJECTIVE
==================================================

Implement a provider-agnostic AI system where NovaAgent
coordinates multiple AI roles.

NovaAgent is always the controller.

==================================================
1. AI Provider Manager
==================================================

Create a ProviderManager.

Support:

- Provider Registry
- Dynamic Provider Loading
- Health Checks
- Provider Priority
- Automatic Failover
- Usage Metrics

Supported provider types:

- OpenAI-compatible
- Anthropic-compatible
- Gemini-compatible
- Custom OpenAI endpoint

No provider-specific logic outside adapters.

==================================================
2. AI Roles
==================================================

Implement configurable AI roles.

Roles:

CoderAI

ReviewerAI

PlannerAI

OptionalSummarizerAI

Each role can use different providers/models.

==================================================
3. Coding Pipeline
==================================================

Workflow:

Receive task

↓

PlannerAI creates execution plan

↓

CoderAI generates patch

↓

NovaAgent applies patch

↓

Run:

typecheck

lint

tests

build

↓

ReviewerAI reviews:

patch

diff

logs

errors

test results

↓

If rejected:

send review feedback back to CoderAI

↓

Generate improved patch

↓

Repeat until accepted or retry limit reached

==================================================
4. Patch Engine
==================================================

Implement patch pipeline.

Support:

Unified Patch object

Diff metadata

Rollback

Patch validation

Conflict detection

==================================================
5. Review Engine
==================================================

Reviewer checks:

Correctness

Security

Performance

Maintainability

Code Style

Architecture

Potential regressions

Return structured review.

==================================================
6. Provider Configuration
==================================================

Configuration example:

PlannerAI -> Provider A

CoderAI -> Provider B

ReviewerAI -> Provider C

Allow runtime switching.

==================================================
7. Metrics
==================================================

Track:

provider latency

token usage

review iterations

success rate

patch acceptance rate

==================================================
8. Documentation
==================================================

Update:

README.md

CURRENT_STATE.md

IMPLEMENTATION_PLAN.md

CHANGELOG.md

==================================================
9. Validation
==================================================

Run until green:

pnpm typecheck

pnpm lint

pnpm test

pnpm build

Fix every issue.

==================================================
10. Final Report
==================================================

Output:

Implemented providers

Implemented AI roles

Pipeline architecture

Files added

Files modified

Tests added

Build status

Lint status

Typecheck status

Production readiness

Remaining work

Do not stop until every requirement above is complete.

```

# Prompt 30 — Memory Engine & Knowledge System
```

# Prompt 30 — Memory Engine & Knowledge System

Continue NovaAgent from the current repository state.

IMPORTANT

- Do NOT rewrite completed modules.
- Do NOT redesign the UI.
- Preserve all functionality from Prompts 26–29.
- Extend the existing architecture.

==================================================
OBJECTIVE
==================================================

Implement a production-ready Memory Engine that allows
NovaAgent to remember projects, previous executions,
user preferences, coding decisions, and reusable
knowledge across sessions.

==================================================
1. Memory Architecture
==================================================

Implement:

- Working Memory
- Short-term Memory
- Long-term Memory
- Project Memory
- Session Memory

==================================================
2. Memory Store
==================================================

Support:

- SQLite / Prisma persistence
- versioning
- timestamps
- tags
- metadata

==================================================
3. Context Builder
==================================================

Automatically build context from:

- project structure
- previous tasks
- commits
- documentation
- execution history

==================================================
4. Knowledge Retrieval
==================================================

Implement semantic retrieval.

Support:

- file lookup
- symbol lookup
- documentation lookup
- previous solution lookup

==================================================
5. Decision Memory
==================================================

Store:

- architectural decisions
- bug fixes
- coding conventions
- reviewer feedback
- successful solutions

Reuse them automatically.

==================================================
6. Agent Memory API
==================================================

Allow every agent to:

read memory

write memory

search memory

summarize memory

==================================================
7. Automatic Context Compression
==================================================

Compress old execution history while preserving
important decisions.

==================================================
8. Documentation
==================================================

Update:

README.md

CURRENT_STATE.md

IMPLEMENTATION_PLAN.md

CHANGELOG.md

==================================================
9. Validation
==================================================

Run until green:

pnpm typecheck

pnpm lint

pnpm test

pnpm build

Fix every issue.

==================================================
10. Final Report
==================================================

Output:

Implemented modules

Memory architecture

Files added

Files modified

Tests added

Build status

Lint status

Typecheck status

Production readiness

Remaining work

Do not stop until every requirement above is complete.
```


# Prompt 29 — Planning Engine & Autonomous Task Decomposition
```
# Prompt 29 — Planning Engine

Continue NovaAgent from the current repository state.

IMPORTANT

- Do NOT rewrite completed modules.
- Do NOT redesign the UI.
- Preserve all functionality from Prompt 28.
- Extend the existing multi-agent architecture.

==================================================
OBJECTIVE
==================================================

Implement an intelligent Planning Engine capable of
analyzing user goals, generating execution plans,
assigning agents automatically, and adapting when
execution changes.

==================================================
1. Goal Analyzer
==================================================

Implement Goal Analyzer.

Responsibilities:

- understand user intent
- detect project type
- classify task complexity
- identify required tools
- estimate execution cost
- detect missing information

Return structured Goal object.

==================================================
2. Task Decomposition
==================================================

Automatically split work into subtasks.

Support:

- sequential tasks
- parallel tasks
- conditional branches
- nested subtasks

Generate dependency graph.

==================================================
3. Dynamic Agent Assignment
==================================================

Automatically assign:

PlannerAgent

CodingAgent

ReviewAgent

TestingAgent

DocumentationAgent

GitAgent

TerminalAgent

based on capabilities.

==================================================
4. Execution Plan
==================================================

Generate:

priority

dependencies

estimated duration

required tools

expected outputs

rollback strategy

==================================================
5. Adaptive Replanning
==================================================

If a task fails:

detect failure

analyze cause

replan remaining tasks

reuse completed work

avoid duplicate execution

==================================================
6. Execution Memory
==================================================

Persist:

execution history

completed subtasks

failed attempts

reasoning summary

artifacts

Support resume execution.

==================================================
7. Plan Visualization API
==================================================

Create backend API exposing:

Execution Graph

Current Status

Completed Tasks

Running Tasks

Blocked Tasks

Timeline

(No UI redesign required.)

==================================================
8. Observability
==================================================

Track:

planning latency

execution latency

agent utilization

success rate

retry count

==================================================
9. Documentation
==================================================

Update:

README.md

CURRENT_STATE.md

IMPLEMENTATION_PLAN.md

CHANGELOG.md

==================================================
10. Validation
==================================================

Run until all pass:

pnpm typecheck

pnpm lint

pnpm test

pnpm build

Fix every issue.

==================================================
11. Final Report
==================================================

Output:

Implemented modules

Architecture summary

Files added

Files modified

Tests added

Build status

Lint status

Typecheck status

Production readiness

Remaining work

Do not stop until every requirement above is complete.

```
# 
```


```
# Prompt 28 — Multi-Agent Orchestrator
```
# Prompt 28 — Multi-Agent Orchestrator

Continue NovaAgent from the current repository state.

IMPORTANT

- Do NOT rewrite completed modules.
- Do NOT redesign the UI.
- Preserve all functionality from Prompt 27.
- Extend the existing runtime.

==================================================
OBJECTIVE
==================================================

Implement a production-ready Multi-Agent Orchestrator.

The orchestrator must coordinate multiple specialized agents to solve a single user request.

==================================================
1. Agent Registry
==================================================

Create a central registry.

Support:

- dynamic registration
- enable/disable agents
- metadata
- capabilities
- version
- health status

==================================================
2. Built-in Agents
==================================================

Implement:

- PlannerAgent
- CodingAgent
- ReviewAgent
- TestingAgent
- DocumentationAgent
- TerminalAgent
- GitAgent

Each agent exposes:

name
description
capabilities
required_tools

==================================================
3. Planner
==================================================

Planner receives a request.

Generate execution plan.

Split into subtasks.

Estimate dependencies.

Return execution graph.

==================================================
4. Orchestrator
==================================================

Execute plan.

Support:

parallel execution

dependency graph

retry

timeout

cancellation

priority queue

==================================================
5. Shared Context
==================================================

Implement shared context.

Agents can exchange:

artifacts

messages

progress

logs

temporary memory

==================================================
6. Agent Communication
==================================================

Support:

request

response

broadcast

events

status updates

==================================================
7. Task Lifecycle
==================================================

Queued

Planning

Running

Waiting

Completed

Failed

Cancelled

==================================================
8. Recovery
==================================================

Retry failed tasks.

Resume interrupted workflow.

Persist orchestration state.

==================================================
9. Monitoring
==================================================

Track:

running agents

completed tasks

failed tasks

execution time

tool usage

token usage

==================================================
10. Documentation
==================================================

Update:

README.md

CURRENT_STATE.md

IMPLEMENTATION_PLAN.md

CHANGELOG.md

==================================================
11. Validation
==================================================

Run until green:

pnpm typecheck

pnpm lint

pnpm test

pnpm build

Fix every issue.

==================================================
12. Final Report
==================================================

Output:

Implemented agents

Architecture summary

Files added

Files modified

Test status

Build status

Remaining work

Production readiness

Do not stop until every requirement is complete.

```
# 
```
# Prompt 27 — AI Agent Runtime

Continue NovaAgent from the current repository state.

IMPORTANT:
- Do NOT redesign the UI.
- Do NOT rewrite completed modules.
- Build on top of Prompt 26.
- Preserve all existing functionality.

OBJECTIVE

Implement the core AI Agent Runtime that powers NovaAgent.

========================
1. Agent Runtime
========================

Create a modular runtime capable of executing agent tasks.

Features:
- Task Queue
- Agent Session
- Context Manager
- Memory Cache
- Tool Registry
- Event Bus
- Cancellation
- Retry
- Timeout
- Progress Events

========================
2. Tool Calling
========================

Implement a unified tool interface.

Built-in tools:

- Terminal
- FileSystem
- Search Files
- Read File
- Write File
- Edit File
- Git
- Shell
- HTTP
- Workspace

Every tool must expose:

name
description
schema
permissions

========================
3. Workspace Execution
========================

Each workspace has:

working directory

terminal session

git repository

environment variables

temporary storage

Workspace isolation is required.

========================
4. Terminal Service
========================

Support:

persistent sessions

multiple terminals

streaming output

stdin/stdout

kill process

restart session

========================
5. Git Integration
========================

Implement:

status

diff

commit

branch

checkout

stash

log

pull

push

========================
6. File Operations
========================

Implement secure operations:

read

write

rename

move

delete

search

watch changes

Prevent access outside workspace.

========================
7. Event System
========================

Emit events:

Task Started

Task Progress

Task Completed

Task Failed

Tool Started

Tool Finished

Terminal Output

Git Changed

========================
8. Documentation
========================

Update:

README.md

CURRENT_STATE.md

IMPLEMENTATION_PLAN.md

CHANGELOG.md

========================
9. Validation
========================

Run until all pass:

pnpm typecheck

pnpm lint

pnpm build

Fix every issue.

========================
10. Final Report
========================

Output:

Completed modules

Files added

Files modified

Build status

Lint status

Typecheck status

Remaining work

Production readiness percentage

Do not stop until everything in this prompt is complete.

```
# 
```
Audit seluruh hasil Prompt 26.

Jangan menambahkan fitur baru.

Lakukan pemeriksaan menyeluruh terhadap repository saat ini.

Periksa:

1. Semua file yang diubah pada Prompt 26.
2. Tidak ada placeholder, TODO, FIXME, atau mock implementation yang tertinggal.
3. Semua import benar dan tidak ada dependency yang rusak.
4. Tidak ada TypeScript error.
5. Tidak ada ESLint error.
6. Tidak ada React hydration issue.
7. Tidak ada dead code atau duplicate component.
8. Semua route dapat diakses.
9. Semua halaman responsive.
10. Semua design token digunakan secara konsisten.
11. Semua dokumentasi diperbarui.
12. Jalankan:
   - pnpm install
   - pnpm typecheck
   - pnpm lint
   - pnpm build
13. Perbaiki seluruh error sampai semuanya PASS.
14. Jangan membuat fitur baru.
15. Di akhir tampilkan:
   - Ringkasan hasil audit.
   - Daftar file yang diperbaiki.
   - Build status.
   - Lint status.
   - Typecheck status.
   - Persentase production readiness.

```

# 
```
Sprint 27 – Core UI Components

Audit repository terlebih dahulu.
Jangan mengulang pekerjaan Sprint 26.

Implementasikan Design System menjadi komponen React yang reusable.

Selesaikan:
- Button
- Input
- Textarea
- Select
- Checkbox
- Radio
- Switch
- Badge
- Avatar
- Card
- Alert
- Modal
- Drawer
- Tabs
- Tooltip
- Dropdown
- Table
- Pagination
- Skeleton
- Spinner

Gunakan TypeScript, Tailwind CSS, shadcn/ui, dan design token dari Sprint 26.

Pastikan semua komponen:
- Mendukung Light/Dark Mode
- Responsive
- Accessible (WCAG AA)
- Memiliki varian dan ukuran
- Memiliki dokumentasi penggunaan

Jalankan typecheck, lint, build, dan perbaiki semua error hingga PASS.
Update dokumentasi setelah selesai.

```
# 
```

Lanjutkan Sprint 26 dari progress terakhir.

Jangan mengulang dokumen yang sudah selesai.

Fokus menyelesaikan:
- 01-design-tokens.md
- 02-color-system.md
- 03-typography.md
- 04-spacing-layout.md
- 05-elevation-motion.md

Pastikan seluruh design token konsisten, reusable, mendukung Light/Dark Mode, Responsive, Accessibility (WCAG AA), serta menjadi acuan implementasi React/Next.js berikutnya.

Setelah selesai, update MASTER_DESIGN_SYSTEM.md sebagai index tanpa mengubah struktur dokumen yang sudah ada.
```
# 
```

Lanjutkan Sprint 26 dari TODO terakhir saja.

Selesaikan berurutan:
- 05b Monitoring wireframe (Prometheus + Grafana)
- 05c Settings wireframe
- 05d Admin Panel wireframe
- 06 User Journey & State Diagram
- 07 Content (tone, microcopy, error states)
- 08 Accessibility (WCAG 2.2 AA)
- 09 Implementation Guide (Tailwind, Radix, struktur komponen)
- Update README.md, IMPLEMENTATION_PLAN.md, CURRENT_STATE.md

Jangan mengulang pekerjaan yang sudah selesai.
Di akhir jalankan:
pnpm typecheck
pnpm lint
pnpm build

Jika ada error, perbaiki sampai PASS lalu tampilkan ringkasan Sprint 26.
```
# 
```

Audit seluruh project NovaAgent yang sudah Production Ready.

Jangan ubah backend, API, database, service, deployment, atau testing.

Fokus membuat Master UI/UX Design System untuk seluruh aplikasi.

Kerjakan:
1. Design System (color, typography, spacing, icon, radius, shadow, animation).
2. Layout desktop & mobile.
3. Sidebar, topbar, navigation.
4. Dashboard.
5. Workspace.
6. Agent.
7. AI Chat.
8. File Manager.
9. Code Editor.
10. Git.
11. Terminal.
12. Build & Deployment.
13. Monitoring.
14. Settings.
15. Admin Panel.
16. Landing Page.
17. Login & Register.

Gunakan style modern seperti Linear + Vercel + GitHub + Cursor.

Jangan implementasi React dulu. Buat blueprint/wireframe, komponen, flow, dan dokumentasi agar implementasi berikutnya tinggal mengikuti desain.

Update README.md, CURRENT_STATE.md, IMPLEMENTATION_PLAN.md.
```
