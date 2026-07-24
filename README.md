# Prompt-website-novaagent











# 
```


```

# 
```


```
# 
```

LANJUTKAN PROJECT NOVAAGENT DARI STATUS TERAKHIR.

JANGAN membuat fitur baru.
JANGAN mengerjakan Sprint 17.
JANGAN mengubah arsitektur.
JANGAN refactor kecuali ditemukan bug.

Fokus hanya pada MANUAL INTEGRATION TEST seluruh NovaAgent.

Lakukan pengujian nyata (bukan hanya build/typecheck/lint) terhadap seluruh sistem.

WAJIB TEST:

1. Authentication
- Register
- Login
- Refresh token
- Logout
- Forgot password
- Reset password

2. Workspace
- Create workspace
- Rename workspace
- Invite member
- Change role
- Delete workspace

3. AI Provider
- Tambah provider
- Edit provider
- Test connection
- Ambil daftar model
- Hapus provider

4. AI Runtime
- Workspace tanpa API Key → memakai Default NovaAgent AI.
- Workspace dengan API Key sendiri → memakai API Key Workspace (BYOK).
- Pastikan pergantian provider tidak mengubah kontrak AI Engine.

5. Agent
- Create agent
- Edit agent
- Delete agent
- Chat
- Streaming
- Tool calling

6. File Manager
- Upload
- Download
- Rename
- Move
- Delete
- Folder tree
- Search

7. Code Editor
- Open file
- Save
- Multi tab
- Search
- Replace
- Lock file

8. Git
- Clone
- Status
- Commit
- Branch
- Diff
- Push
- Pull

9. Terminal
- Open terminal
- Execute command
- Resize
- Reconnect
- Close session

10. Build Service
- Create build
- Monitor progress
- View logs
- Cancel build

11. Notification
- Notification Bell
- Dropdown
- Notification Center
- Real-time WebSocket
- Mark read
- Mark all read

12. API Gateway
Pastikan seluruh route berjalan.

13. Docker
Pastikan semua container healthy.

14. Database
Pastikan seluruh migration valid.

15. WebSocket
Pastikan streaming agent, terminal, notification berjalan.

16. Frontend
Pastikan seluruh halaman dapat dibuka tanpa error.

17. Security
Test JWT
RBAC
Workspace Isolation

18. Performance
Pastikan tidak ada memory leak
Tidak ada query lambat
Tidak ada error di console browser

WAJIB menghasilkan laporan:

✔ PASS
⚠ WARNING
✖ FAILED

untuk setiap modul.

Jika menemukan bug:

- Jelaskan penyebab.
- Perbaiki.
- Jalankan ulang test.
- Pastikan bug benar-benar selesai.

WAJIB update:

- README.md
- CURRENT_STATE.md
- CHANGELOG.md
- DECISIONS.md

Sprint baru TIDAK BOLEH dimulai sebelum seluruh manual integration test selesai dan seluruh bug kritikal diperbaiki.

Setelah selesai tampilkan:

- PROJECT HEALTH
- BUG SUMMARY
- FIX SUMMARY
- MANUAL TEST RESULT
- READY FOR SPRINT 17 (YES/NO)
```
# 
```
LANJUTKAN PROJECT NOVAAGENT DARI KONDISI REPOSITORY SAAT INI.

JANGAN membuat project baru.
JANGAN mengulang sprint yang sudah selesai.
JANGAN mengubah arsitektur tanpa alasan teknis.
JANGAN langsung mengerjakan Sprint 16.

LANGKAH PERTAMA WAJIB ADALAH AUDIT MENYELURUH.

Lakukan audit terhadap seluruh repository dan bandingkan dengan:

- ARCHITECTURE_BLUEPRINT.md
- PRD.md
- IMPLEMENTATION_PLAN.md
- AGENT_SPEC.md
- API_SPEC.md
- DATABASE_DESIGN.md
- UI_UX_SPEC.md
- README.md
- CURRENT_STATE.md
- CHANGELOG.md
- DECISIONS.md

Audit seluruh project meliputi:

1. Monorepo structure
2. Hexagonal Architecture
3. Dependency antar service
4. Workspace isolation
5. Authentication & RBAC
6. AI Provider Service
7. AI Engine
8. Agent Service
9. File Service
10. Editor Service
11. Git Service
12. Terminal Service
13. Build Service
14. Notification Service
15. API Gateway
16. Frontend
17. Database Schema
18. Prisma Migration
19. Docker Compose
20. Nginx
21. Environment Variables
22. WebSocket
23. Tool Calling
24. AI Bridge
25. Provider Runtime
26. Build Pipeline
27. Security
28. Documentation
29. README consistency
30. CURRENT_STATE consistency
31. CHANGELOG consistency
32. DECISIONS consistency

WAJIB menemukan:

- Bug
- Missing implementation
- TODO yang tertinggal
- Duplicate code
- Dead code
- Wrong architecture
- Memory leak
- Race condition
- Security issue
- Performance bottleneck
- Naming inconsistency
- Folder inconsistency
- API inconsistency
- Prisma inconsistency
- Frontend inconsistency
- Build issue
- Type issue
- Lint issue
- Documentation mismatch

Jalankan seluruh verifikasi:

pnpm install
pnpm prisma generate
pnpm typecheck
pnpm lint
pnpm build
pnpm test (jika tersedia)

JANGAN memperbaiki apa pun sebelum seluruh audit selesai.

Setelah audit selesai tampilkan:

1. Audit Summary
2. Critical Issues
3. Medium Issues
4. Minor Issues
5. Missing Modules
6. Missing APIs
7. Missing UI
8. Missing Documentation
9. Security Findings
10. Performance Findings
11. Architecture Findings
12. Sprint Progress (%)
13. Recommendation

Jika hasil audit menunjukkan repository sehat dan tidak ada masalah kritis, BARU lanjut otomatis ke Sprint 16 sesuai IMPLEMENTATION_PLAN.md.

Setelah Sprint 16 selesai WAJIB:

- Build PASS
- Typecheck PASS
- Lint PASS
- Test PASS (jika tersedia)
- README.md diperbarui
- CURRENT_STATE.md diperbarui
- CHANGELOG.md diperbarui
- DECISIONS.md diperbarui

Kemudian tampilkan:

PROJECT STATUS
CURRENT SPRINT
COMPLETED MODULES
NEXT MODULE
NEXT SPRINT
PROJECT HEALTH
NEXT PROMPT

Jangan pernah membuat implementasi fiktif. Semua klaim harus berasal dari hasil pemeriksaan repository yang sebenarnya.

```
# Sprint 16 – AI Provider Runtime & BYOK,
```

LANJUTKAN PROJECT NOVAAGENT DARI STATUS TERAKHIR.

Jangan membuat project baru.
Jangan mengulang sprint yang sudah selesai.
Jangan mengubah arsitektur.
Jangan mengubah roadmap tanpa alasan teknis yang kuat.

Sprint 15 telah selesai.

Selanjutnya implementasikan Sprint 16 — AI Provider Runtime & BYOK.

Tujuan sprint ini adalah membuat NovaAgent dapat bekerja dengan dua mode:

1. Default NovaAgent AI
- Menggunakan AI bawaan NovaAgent jika user belum memiliki API Key.

2. Bring Your Own API Key (BYOK)
- User dapat menambahkan API Key sendiri.
- Setelah API Key aktif, seluruh proses AI menggunakan provider tersebut.

Implementasikan Provider Runtime yang mendukung:

- OpenAI
- Anthropic
- Gemini
- DeepSeek
- Kimi
- OpenRouter
- OmniRoute
- OpenAI Compatible

Implementasikan:

- Provider Adapter
- Dynamic Provider Loading
- Provider Health Check
- Auto Reconnect
- Streaming Support
- Tool Calling Support
- Model Discovery
- Cost Tracking
- Token Tracking
- Fallback Provider
- Priority Provider
- Default Provider
- Workspace Provider
- User Provider
- API Key Encryption
- API Key Validation
- Test Connection
- Provider Capability Detection

Tambahkan halaman Provider Runtime yang menampilkan:

- Provider aktif
- Model aktif
- Health Status
- Token Usage
- Cost Usage
- Response Time
- Test Connection
- Switch Provider
- Enable/Disable Provider

Integrasikan AI Engine sehingga seluruh request AI selalu melewati Provider Runtime.

Jika Workspace memiliki API Key, gunakan API Key tersebut.

Jika Workspace tidak memiliki API Key, gunakan Default NovaAgent AI.

Pastikan seluruh Tool Calling, Editor, Terminal, Git, Build, File Manager, dan AI Engine bekerja tanpa perubahan meskipun provider diganti.

WAJIB update:

- README.md
- CURRENT_STATE.md
- CHANGELOG.md
- DECISIONS.md

Sprint tidak boleh selesai sebelum:

- Build PASS
- Typecheck PASS
- Lint PASS
- Dokumentasi sinkron

Setelah selesai tampilkan PROJECT STATUS, CURRENT SPRINT, COMPLETED MODULES, NEXT MODULE, NEXT SPRINT, PROJECT HEALTH, dan NEXT PROMPT.
```
# Sprint 15
```

LANJUTKAN PROJECT NOVAAGENT DARI STATUS TERAKHIR.

Jangan membuat project baru.
Jangan mengulang sprint yang sudah selesai.
Jangan mengubah arsitektur.
Jangan mengubah roadmap tanpa alasan teknis yang kuat.

==================================================
CURRENT STATUS
==================================================

Sprint terakhir selesai:

✅ Sprint 14 - Build Service

Seluruh dokumentasi sudah tersedia:

README.md
CURRENT_STATE.md
CHANGELOG.md
DECISIONS.md
ARCHITECTURE_BLUEPRINT.md
PRD.md
UI_UX_SPEC.md
DATABASE_DESIGN.md
API_SPEC.md
AGENT_SPEC.md
IMPLEMENTATION_PLAN.md

WAJIB membaca seluruh dokumentasi sebelum implementasi.

==================================================
SPRINT 15
AI CODING ENGINE
==================================================

Sprint ini adalah inti NovaAgent.

Target sprint ini adalah membuat AI benar-benar mampu mengerjakan project menggunakan seluruh service yang sudah dibangun.

==================================================
AI ENGINE
==================================================

Bangun ai-engine-service menggunakan Fastify + Hexagonal Architecture.

Implementasikan:

- Planner
- Task Manager
- Context Manager
- Conversation Manager
- Memory Manager
- Workspace Context
- Prompt Builder
- Tool Registry
- Tool Executor
- Tool Permission
- Model Router
- Provider Router
- AI Session
- AI Job Queue
- AI Result Cache
- AI History
- Token Usage
- Cost Tracking
- Retry Strategy
- Error Recovery
- Cancellation
- Streaming Response
- Approval Workflow
- Human Approval Mode

==================================================
REACT LOOP
==================================================

Implementasikan penuh:

Reason

Action

Observe

Reason

Action

Observe

Finish

Loop harus modular dan dapat diperluas.

==================================================
TOOLS
==================================================

Hubungkan AI dengan seluruh service yang sudah ada.

AI dapat:

Workspace

- membaca workspace
- memilih workspace
- membuat workspace

File Manager

- membaca file
- membuat file
- rename file
- move file
- copy file
- delete file
- upload file
- download file
- search file

Code Editor

- open file
- edit file
- save file
- search
- replace
- diff
- go to line

Git

- status
- diff
- commit
- push
- pull
- fetch
- checkout
- merge
- rebase
- create branch

Terminal

- membuat terminal
- menjalankan command
- membaca output
- menghentikan process

Build

- menjalankan build
- menjalankan test
- menjalankan lint
- membaca build log
- retry build

==================================================
AI PROVIDER
==================================================

Gunakan Provider Service yang sudah ada.

Dukung:

OpenAI

Anthropic

Gemini

DeepSeek

Kimi

OpenRouter

OmniRoute

OpenAI Compatible

BYOK (Bring Your Own API Key)

Jika Workspace memiliki API Key sendiri gunakan API Key tersebut.

Jika tidak ada gunakan Default NovaAgent AI.

Implementasikan Provider Priority:

1. Workspace API Key
2. User API Key
3. Default NovaAgent AI

==================================================
STREAMING
==================================================

Implementasikan:

Realtime Token Streaming

Realtime Tool Status

Realtime Reasoning Status

Realtime Progress

Realtime Build Status

Realtime Terminal Output

==================================================
AI MEMORY
==================================================

Implementasikan:

Short Term Memory

Workspace Memory

Conversation Memory

Task Memory

File Memory

Git Memory

Terminal Memory

Build Memory

==================================================
APPROVAL
==================================================

Implementasikan Human Approval Mode.

Sebelum AI:

- delete file
- overwrite file
- git push
- merge
- menjalankan command berbahaya

AI harus meminta persetujuan user.

==================================================
SECURITY
==================================================

Implementasikan:

Workspace Isolation

Permission Check

Audit Log

Encrypted API Key

Rate Limit

Timeout

Resource Limit

==================================================
QUALITY GATE
==================================================

Sprint tidak boleh selesai sebelum:

✅ Build PASS

✅ Typecheck PASS

✅ Lint PASS

Review:

Bug

Security

Performance

Memory Leak

Duplicate Code

Dependency Conflict

Perbaiki seluruh issue sebelum sprint selesai.

==================================================
DOCUMENTATION
==================================================

WAJIB update:

README.md

CURRENT_STATE.md

CHANGELOG.md

DECISIONS.md

==================================================
OUTPUT
==================================================

Setelah sprint selesai tampilkan:

PROJECT STATUS

CURRENT PHASE

CURRENT SPRINT

CURRENT MODULE

COMPLETED MODULES

NEXT MODULE

NEXT SPRINT

PROJECT HEALTH

BUILD STATUS

TYPECHECK STATUS

LINT STATUS

TEST STATUS

NEXT PROMPT

==================================================
IMPORTANT
==================================================

Project ini akan dilanjutkan oleh beberapa AI berbeda.

Seluruh dokumentasi harus selalu sinkron.

AI Engine harus menggunakan seluruh service yang telah selesai dibangun (Workspace, Provider, API Gateway, File Manager, Monaco Editor, Git, Terminal, Build Service).

Jangan membuat implementasi sederhana. Bangun AI Coding Engine yang modular, scalable, production-ready, dan mudah diperluas untuk mendukung multi-agent di sprint berikutnya.

Jangan lanjut ke Sprint 16 sebelum Sprint 15 benar-benar selesai, seluruh quality gate PASS, dan seluruh dokumentasi telah diperbarui.
```

# Selanjutnya: Sprint 14 — Build Service
```
LANJUTKAN PROJECT NOVAAGENT DARI STATUS TERAKHIR.

Sebelum mengerjakan apa pun:

1. Selesaikan update README.md, CURRENT_STATE.md, CHANGELOG.md, dan DECISIONS.md untuk Sprint 13.
2. Pastikan Build PASS, Typecheck PASS, dan Lint PASS.
3. Setelah seluruh dokumentasi sinkron, lanjutkan Sprint 14.

==================================================
SPRINT 14
BUILD SERVICE
==================================================

Target sprint ini adalah membangun Build Service enterprise yang dapat menjalankan, memonitor, dan mengelola proses build project dalam setiap workspace.

==================================================
BACKEND
==================================================

Buat build-service (Fastify + Hexagonal Architecture).

Implementasikan:

- Build Service
- Task Runner
- Build Queue
- Job Scheduler
- Build Session
- Build History
- Build Log
- Real-time Build Output
- Process Manager
- Artifact Manager
- Environment Variables
- Exit Code Tracking
- Retry Build
- Cancel Build
- Parallel Build
- Workspace Isolation

==================================================
SUPPORTED COMMANDS
==================================================

Implementasikan dukungan:

npm install
npm run dev
npm run build
npm run test
npm run lint

pnpm install
pnpm dev
pnpm build
pnpm test
pnpm lint

yarn install
yarn dev
yarn build

bun install
bun run

custom command

==================================================
FRONTEND
==================================================

Bangun Build UI lengkap.

Implementasikan:

- Build Dashboard
- Build History
- Build Console
- Live Output
- Progress Bar
- Status Badge
- Running Jobs
- Failed Jobs
- Success Jobs
- Retry Button
- Cancel Button
- Build Detail
- Build Artifact
- Search Build
- Filter Build

==================================================
TERMINAL INTEGRATION
==================================================

Build menggunakan Terminal Service.

Semua output harus tampil secara real-time melalui WebSocket.

==================================================
EDITOR INTEGRATION
==================================================

Jika build gagal:

- tampilkan file error
- tampilkan line number
- buka Monaco Editor pada posisi error

==================================================
GIT INTEGRATION
==================================================

Tampilkan:

- Commit yang sedang dibangun
- Branch
- Author
- Commit Message

==================================================
AI BRIDGE
==================================================

Persiapkan interface agar AI nantinya dapat:

- menjalankan build
- membaca output build
- menganalisis error
- menjalankan test
- membaca hasil test
- retry build

Belum perlu implementasi AI otomatis.

==================================================
SECURITY
==================================================

Implementasikan:

Workspace Isolation

Permission Check

Audit Log

Timeout

Resource Limit

Rate Limiting

==================================================
QUALITY GATE
==================================================

Sprint tidak boleh selesai sebelum:

Build PASS

Typecheck PASS

Lint PASS

Semua dokumentasi diperbarui.

==================================================
OUTPUT
==================================================

Setelah selesai tampilkan:

PROJECT STATUS

CURRENT PHASE

CURRENT SPRINT

CURRENT MODULE

COMPLETED MODULES

NEXT MODULE

NEXT SPRINT

PROJECT HEALTH

BUILD STATUS

TYPECHECK STATUS

LINT STATUS

TEST STATUS

NEXT PROMPT

```

# Sprint 13 — Terminal Service (Sekali Copy)
```

LANJUTKAN PROJECT NOVAAGENT DARI STATUS TERAKHIR.

Jangan membuat project baru.
Jangan mengulang sprint yang sudah selesai.
Jangan mengubah arsitektur.
Jangan mengubah roadmap.

==================================================
CURRENT STATUS
==================================================

Sprint terakhir selesai:

✅ Sprint 12 - Git Integration

Sebelum implementasi:

Pastikan BUILD benar-benar PASS.

Jika ada dependency yang belum terpasang (misalnya @monaco-editor/react atau dependency lain), selesaikan terlebih dahulu sampai Build, Typecheck, dan Lint semuanya PASS.

Setelah itu baru lanjut Sprint 13.

==================================================
SPRINT 13
TERMINAL SERVICE
==================================================

Target sprint ini adalah membangun Terminal Service enterprise yang menjadi dasar AI Agent.

==================================================
BACKEND
==================================================

Buat terminal-service menggunakan Fastify + Hexagonal Architecture.

Implementasikan:

- PTY Service
- Interactive Shell
- Bash
- Zsh
- Fish (jika tersedia)
- PowerShell abstraction
- Terminal Session
- Multi Session
- Session Restore
- Session History
- Command History
- Environment Manager
- Workspace Isolation
- Process Manager
- Process Tree
- Kill Process
- Resize Terminal
- Terminal Logs
- Resource Monitoring
- Timeout
- Idle Cleanup
- Terminal Permission
- Terminal Audit Log

==================================================
FRONTEND
==================================================

Gunakan xterm.js

Implementasikan:

- Multi Tab Terminal
- Split Terminal
- Terminal Sidebar
- Terminal Toolbar
- Resize
- Font Size
- Theme
- Copy
- Paste
- Search
- Clear
- Download Log
- Session List
- Session Restore
- Terminal Settings

==================================================
WORKSPACE
==================================================

Setiap Workspace memiliki terminal sendiri.

Terminal tidak boleh dapat mengakses workspace lain.

==================================================
EDITOR INTEGRATION
==================================================

Hubungkan Monaco Editor dengan Terminal.

Implementasikan:

Open Terminal Here

Run Current File

Run Selected File

Open Folder Terminal

==================================================
FILE MANAGER
==================================================

Implementasikan:

Open Folder in Terminal

Reveal Current Directory

==================================================
GIT
==================================================

Terminal harus dapat menjalankan:

git status

git add

git commit

git pull

git push

git checkout

git branch

git merge

git rebase

==================================================
AI BRIDGE
==================================================

Persiapkan interface agar AI nantinya dapat:

- menjalankan command
- membaca output terminal
- menghentikan process
- membuka terminal
- membuat terminal baru
- memilih terminal
- membaca exit code

Belum perlu AI otomatis.

Cukup interface, service, event, dan extension point.

==================================================
SECURITY
==================================================

Implementasikan:

Workspace Isolation

Command Validation

Permission Check

Rate Limit

Audit Log

Timeout

Resource Limit

==================================================
QUALITY GATE
==================================================

Sprint tidak boleh selesai sebelum:

✅ Build PASS

✅ Typecheck PASS

✅ Lint PASS

Review:

- Bug
- Security
- Memory Leak
- Duplicate Code
- Performance
- Dependency Conflict

==================================================
DOCUMENTATION
==================================================

WAJIB update:

README.md

CURRENT_STATE.md

CHANGELOG.md

DECISIONS.md (jika ada keputusan baru)

==================================================
OUTPUT
==================================================

Setelah sprint selesai tampilkan:

PROJECT STATUS

CURRENT PHASE

CURRENT SPRINT

CURRENT MODULE

COMPLETED MODULES

NEXT MODULE

NEXT SPRINT

PROJECT HEALTH

BUILD STATUS

TYPECHECK STATUS

LINT STATUS

TEST STATUS

NEXT PROMPT

==================================================
IMPORTANT
==================================================

Project ini akan dilanjutkan oleh AI lain.

Pastikan seluruh dokumentasi selalu sinkron.

Jangan lanjut ke Sprint 14 sebelum Sprint 13 benar-benar selesai dan seluruh dokumentasi telah diperbarui.
```
# Sprint 12 — Git Integration
```

LANJUTKAN PROJECT NOVAAGENT DARI STATUS TERAKHIR.

Jangan membuat project baru.
Jangan mengulang sprint yang sudah selesai.
Jangan mengubah arsitektur.
Jangan mengubah roadmap.
Jangan mengubah struktur folder.

==================================================
CURRENT STATUS
==================================================

Sprint terakhir selesai:

✅ Sprint 11 - Code Editor

Project telah memiliki:

- Authentication
- Workspace
- Provider Manager
- Agent Backend
- API Gateway
- File Manager
- Monaco Code Editor

Seluruh dokumentasi sudah tersedia:

README.md
CURRENT_STATE.md
CHANGELOG.md
DECISIONS.md

ARCHITECTURE_BLUEPRINT.md
PRD.md
UI_UX_SPEC.md
DATABASE_DESIGN.md
API_SPEC.md
AGENT_SPEC.md
IMPLEMENTATION_PLAN.md

WAJIB membaca seluruh dokumen sebelum implementasi.

==================================================
SPRINT 12
GIT INTEGRATION
==================================================

Target sprint ini adalah membangun Git Service enterprise yang terintegrasi penuh dengan Workspace, File Manager, Monaco Editor, API Gateway, dan AI Bridge.

==================================================
BACKEND
==================================================

Buat Git Service (Fastify + Hexagonal Architecture).

Implementasikan:

- Repository Manager
- Git Init
- Git Clone
- Git Pull
- Git Push
- Git Fetch
- Git Commit
- Git Status
- Git Diff
- Git Log
- Git Branch
- Create Branch
- Delete Branch
- Rename Branch
- Checkout Branch
- Merge Branch
- Rebase
- Cherry Pick
- Stash
- Tag
- Remote Manager
- Credential Manager
- SSH Key Support
- HTTPS Authentication
- Repository Validation
- Workspace Repository Isolation
- Audit Log

==================================================
API
==================================================

Implementasikan REST API:

GET Repository

POST Clone

POST Init

POST Commit

POST Push

POST Pull

POST Fetch

GET Status

GET Diff

GET Log

GET Branches

POST Checkout

POST Merge

POST Rebase

POST Stash

POST Tag

POST Remote

POST Credentials

==================================================
FRONTEND
==================================================

Bangun Git UI lengkap.

Implementasikan:

Git Sidebar

Repository Dashboard

Repository Selector

Clone Dialog

Commit Dialog

Commit History

Changed Files

Diff Viewer

Branch Selector

Branch Manager

Push Button

Pull Button

Fetch Button

Merge Dialog

Conflict Viewer

Repository Settings

Git Activity

Git Status Badge

==================================================
EDITOR INTEGRATION
==================================================

Hubungkan Git dengan Monaco Editor.

Implementasikan:

Open Changed File

Inline Diff

File History

Unsaved Indicator

Git Decorations

Current Branch Display

Git Status Indicator

==================================================
FILE MANAGER INTEGRATION
==================================================

Hubungkan Git dengan File Manager.

Implementasikan:

Git Status per File

Modified Icon

Added Icon

Deleted Icon

Ignored File

Rename Tracking

==================================================
AI BRIDGE
==================================================

Persiapkan interface agar AI nantinya dapat:

- membaca status Git
- membaca commit
- membaca diff
- membuat commit
- membuat branch
- checkout branch
- merge branch
- push
- pull

Belum perlu implementasi AI otomatis.

Cukup siapkan interface, service, event, dan extension point.

==================================================
SECURITY
==================================================

Implementasikan:

Workspace Isolation

Permission Check

Credential Encryption

SSH Key Storage

Audit Log

Validation

Error Handling

Rate Limiting

==================================================
QUALITY GATE
==================================================

Sprint tidak boleh selesai sebelum:

Build PASS

Typecheck PASS

Lint PASS

Review:

Bug

Duplicate Code

Performance

Memory Leak

Security

Dependency Conflict

==================================================
DOCUMENTATION
==================================================

WAJIB update:

README.md

CURRENT_STATE.md

CHANGELOG.md

DECISIONS.md (jika ada keputusan baru)

==================================================
OUTPUT
==================================================

Setelah sprint selesai tampilkan:

PROJECT STATUS

CURRENT PHASE

CURRENT SPRINT

CURRENT MODULE

COMPLETED MODULES

NEXT MODULE

NEXT SPRINT

PROJECT HEALTH

BUILD STATUS

TYPECHECK STATUS

LINT STATUS

TEST STATUS

NEXT PROMPT

==================================================
IMPORTANT
==================================================

Semua implementasi harus tetap mengikuti seluruh dokumentasi NovaAgent.

Project ini akan dikerjakan oleh beberapa AI berbeda.

Pastikan seluruh dokumentasi selalu sinkron.

Jangan lanjut ke Sprint 13 sebelum Sprint 12 benar-benar selesai dan seluruh dokumentasi telah diperbarui.
```
# Sprint 11 – Code Editor
```
LANJUTKAN PROJECT NOVAAGENT DARI STATUS TERAKHIR.

Jangan membuat project baru.
Jangan mengulang sprint yang sudah selesai.
Jangan mengubah arsitektur.
Jangan mengubah roadmap.
Jangan mengubah struktur project.

==================================================
CURRENT STATUS
==================================================

Sprint terakhir selesai:
Sprint 10 - File Manager

Sebelum coding WAJIB membaca:

README.md
CURRENT_STATE.md
CHANGELOG.md
DECISIONS.md

ARCHITECTURE_BLUEPRINT.md
PRD.md
UI_UX_SPEC.md
DATABASE_DESIGN.md
API_SPEC.md
AGENT_SPEC.md
IMPLEMENTATION_PLAN.md

Lanjutkan project dari status terakhir.

==================================================
SPRINT 11
CODE EDITOR
==================================================

Target sprint ini adalah membangun Code Editor enterprise yang akan menjadi editor utama NovaAgent.

Backend

- Editor Service
- File Open API
- File Save API
- Auto Save
- File Lock
- File Version
- Diff API
- Search API
- Replace API
- Recent Files
- Editor Settings
- Session Restore

Frontend

Gunakan Monaco Editor.

Implementasikan:

- Monaco Editor
- Multi Tab
- Split View
- Syntax Highlight
- Auto Save
- Search
- Replace
- Go To Line
- Minimap
- Line Numbers
- Word Wrap
- Theme Light/Dark
- Font Size
- Font Family
- Keyboard Shortcut
- File Tabs
- Unsaved Indicator
- Dirty State
- Read Only Mode
- Breadcrumb
- Right Click Menu
- Open From File Manager
- Save To File Manager
- Restore Last Session

Workspace

Editor harus langsung terintegrasi dengan:

- Workspace
- File Manager
- Agent
- Chat
- Provider
- Build System

AI Integration

Persiapkan editor agar nantinya AI dapat:

- membaca file
- mengedit file
- membuat file baru
- rename file
- delete file
- highlight perubahan
- preview diff

Belum perlu implementasi AI editing.

Cukup siapkan interface, event, service, dan extension point.

==================================================
IMPLEMENTATION RULES
==================================================

Gunakan:

Hexagonal Architecture

Repository Pattern

Service Layer

Dependency Injection

Interface

Validation

Error Handling

Logging

Workspace Isolation

Permission Check

Modular Design

==================================================
QUALITY GATE
==================================================

Sprint tidak boleh selesai sebelum:

Build PASS

Typecheck PASS

Lint PASS

Review:

Bug

Security

Duplicate Code

Performance

Memory Leak

Dependency Conflict

Perbaiki seluruh issue sebelum sprint selesai.

==================================================
DOCUMENTATION
==================================================

WAJIB update:

README.md

CURRENT_STATE.md

CHANGELOG.md

DECISIONS.md (jika ada keputusan baru)

==================================================
OUTPUT
==================================================

Setelah sprint selesai tampilkan:

PROJECT STATUS

CURRENT PHASE

CURRENT SPRINT

CURRENT MODULE

COMPLETED MODULES

NEXT MODULE

NEXT SPRINT

PROJECT HEALTH

BUILD STATUS

TYPECHECK STATUS

LINT STATUS

TEST STATUS

NEXT PROMPT

==================================================
IMPORTANT
==================================================

Seluruh implementasi harus konsisten dengan semua dokumentasi NovaAgent.

Project ini akan dilanjutkan oleh beberapa AI berbeda.

Pastikan seluruh dokumentasi selalu sinkron.

Jangan lanjut ke Sprint 12 sebelum Sprint 11 benar-benar selesai dan seluruh dokumentasi telah diperbarui.

```
# Sprint 10 – File Manager
```
LANJUTKAN PROJECT NOVAAGENT DARI STATUS TERAKHIR.

Jangan membuat project baru.
Jangan mengulang sprint yang sudah selesai.
Jangan mengubah arsitektur.
Jangan mengubah roadmap.

==================================================
CURRENT STATUS
==================================================

Project : NovaAgent

Sprint terakhir selesai:
Sprint 9 - API Gateway

Seluruh dokumentasi sudah tersedia:

- README.md
- CURRENT_STATE.md
- CHANGELOG.md
- DECISIONS.md
- ARCHITECTURE_BLUEPRINT.md
- PRD.md
- UI_UX_SPEC.md
- DATABASE_DESIGN.md
- API_SPEC.md
- AGENT_SPEC.md
- IMPLEMENTATION_PLAN.md

Baca seluruh dokumen tersebut sebelum mengimplementasikan kode.

==================================================
SPRINT 10
FILE MANAGER
==================================================

Target sprint ini adalah membangun File Manager enterprise yang akan menjadi dasar seluruh AI Agent.

Backend:

- File Service
- Folder Service
- Upload
- Download
- Rename
- Delete
- Move
- Copy
- Create Folder
- Recursive Folder Tree
- File Metadata
- Search
- Pagination
- Sorting
- Filter
- Storage abstraction
- Permission checking
- Workspace isolation
- Audit log
- Soft delete
- Restore file
- File version metadata

Frontend:

- File Explorer
- Folder Tree
- Breadcrumb
- Context Menu
- Drag & Drop
- Upload Dialog
- Rename Dialog
- Delete Confirmation
- Search Box
- Empty State
- Loading State
- File Icons
- Multi Select
- Right Click Menu
- Preview Panel
- Responsive Layout

API:

- CRUD File
- CRUD Folder
- Upload API
- Download API
- Move API
- Copy API
- Search API
- Restore API

==================================================
IMPLEMENTATION RULES
==================================================

Ikuti Hexagonal Architecture.

Semua module harus modular.

Gunakan dependency injection.

Jangan hardcode.

Gunakan interface.

Gunakan repository pattern.

Gunakan service abstraction.

Gunakan validation.

Gunakan error handling.

Gunakan logging.

Gunakan audit.

==================================================
QUALITY
==================================================

Sprint tidak boleh selesai sebelum:

✅ Build PASS

✅ Typecheck PASS

✅ Lint PASS

Review:

- Bug
- Security
- Duplicate code
- Memory leak
- Performance
- Dependency

Perbaiki semua issue sebelum sprint selesai.

==================================================
DOCUMENTATION
==================================================

Setelah selesai WAJIB update:

README.md

CURRENT_STATE.md

CHANGELOG.md

DECISIONS.md (jika ada keputusan arsitektur baru)

==================================================
OUTPUT
==================================================

Setelah sprint selesai tampilkan:

PROJECT STATUS

CURRENT PHASE

CURRENT SPRINT

CURRENT MODULE

COMPLETED MODULES

NEXT MODULE

NEXT SPRINT

PROJECT HEALTH

BUILD STATUS

TYPECHECK STATUS

LINT STATUS

TEST STATUS

NEXT PROMPT

Jangan melanjutkan ke Sprint 11 sebelum Sprint 10 benar-benar selesai dan seluruh dokumentasi telah diperbarui.

```

# 
```
LANJUTKAN PROJECT NOVAAGENT YANG SUDAH ADA.

Jangan membuat project baru.
Jangan mengulang sprint yang sudah selesai.
Jangan mengubah arsitektur tanpa alasan teknis yang kuat.
Jangan mengubah roadmap.
Jangan mengubah struktur folder.
Jangan membuat implementasi yang bertentangan dengan dokumentasi.

==================================================
SOURCE OF TRUTH
==================================================

Sebelum mengerjakan apa pun WAJIB membaca:

README.md
CURRENT_STATE.md
CHANGELOG.md
DECISIONS.md (jika sudah ada)

ARCHITECTURE_BLUEPRINT.md
PRD.md
UI_UX_SPEC.md
DATABASE_DESIGN.md
API_SPEC.md
AGENT_SPEC.md
IMPLEMENTATION_PLAN.md

Seluruh keputusan implementasi HARUS mengikuti dokumen tersebut.

==================================================
LANJUTKAN PROJECT
==================================================

Identifikasi terlebih dahulu:

- Current Phase
- Current Sprint
- Current Module
- Last Completed Task
- Completed Sprint
- Completed Modules
- Current Progress
- Next Module
- Next Sprint

Kemudian LANJUTKAN PROJECT dari posisi terakhir.

Jangan mengulang pekerjaan yang sudah selesai.

==================================================
DEVELOPMENT RULES
==================================================

Kerjakan hanya SATU sprint atau SATU modul.

Urutan wajib:

Planning

Implementation

Self Review

Refactor

Testing

Build

Typecheck

Lint

README Update

CURRENT_STATE Update

CHANGELOG Update

DECISIONS Update (jika ada keputusan baru)

Sprint Checklist Update

Finish

==================================================
QUALITY GATE
==================================================

Sprint tidak boleh selesai sebelum:

Build PASS

Typecheck PASS

Lint PASS

Semua test PASS

Tidak ada bug kritis

Tidak ada security issue

Tidak ada duplicate code yang tidak perlu

Tidak ada memory leak

Tidak ada dependency conflict

Jika ada masalah WAJIB diperbaiki dahulu.

==================================================
README.md
==================================================

README adalah Master Progress Project.

Selalu update:

Project Status

Current Phase

Current Sprint

Current Module

Overall Progress

Completed Sprint

Completed Modules

Current Module

Next Module

Next Sprint

Project Health

Architecture Version

Database Version

API Version

Agent Version

Developer Notes

Known Issues

TODO

==================================================
CURRENT_STATE.md
==================================================

Selalu update:

Current Phase

Current Sprint

Current Module

Completed Sprint

Completed Modules

Next Sprint

Next Module

Build

Typecheck

Lint

Last Update

==================================================
CHANGELOG.md
==================================================

Setiap sprint tambahkan:

Tanggal

Sprint

Module

Feature

Files Created

Files Updated

Files Deleted

Database Changes

API Changes

Breaking Changes

Testing Result

Build Result

Typecheck Result

Lint Result

Next Sprint

==================================================
DECISIONS.md
==================================================

Jika terdapat keputusan arsitektur atau teknologi baru WAJIB membuat atau memperbarui DECISIONS.md.

Format setiap keputusan:

Decision ID

Title

Date

Status

Context

Problem

Alternatives Considered

Decision

Reason

Benefits

Trade-offs

Impact

Affected Modules

Migration Needed

Notes

Jangan menghapus keputusan lama.

Tambahkan keputusan baru secara berurutan.

==================================================
PROJECT HEALTH
==================================================

Setelah sprint selesai tampilkan:

PROJECT STATUS

CURRENT PHASE

CURRENT SPRINT

CURRENT MODULE

OVERALL PROGRESS

COMPLETED MODULES

NEXT MODULE

NEXT SPRINT

BUILD STATUS

TYPECHECK STATUS

LINT STATUS

TEST STATUS

PROJECT HEALTH

==================================================
IMPORTANT
==================================================

Project ini akan dikerjakan oleh beberapa AI yang berbeda (DeepSeek, GPT, Claude, Gemini, dan model lainnya).

Seluruh dokumentasi harus selalu sinkron.

Jika README.md, CURRENT_STATE.md, CHANGELOG.md, atau DECISIONS.md belum sesuai dengan kondisi project, perbarui terlebih dahulu sebelum melanjutkan sprint berikutnya.

Selalu lanjutkan project dari status terakhir.

Jangan membuat ulang project.

Jangan mengulang sprint.

Jangan mengubah arsitektur tanpa persetujuan.

Prioritaskan kualitas, konsistensi, dan maintainability dibanding kecepatan implementasi.

```


# 
```
LANJUTKAN PROJECT NOVAAGENT YANG SUDAH ADA.

Jangan membuat project baru.
Jangan mengubah arsitektur.
Jangan mengubah roadmap.
Jangan mengubah struktur folder.
Jangan membuat implementasi yang bertentangan dengan seluruh dokumentasi project.

==================================================
SOURCE OF TRUTH
==================================================

Sebelum mengerjakan apa pun WAJIB membaca:

README.md
CURRENT_STATE.md
CHANGELOG.md
ARCHITECTURE_BLUEPRINT.md
PRD.md
UI_UX_SPEC.md
DATABASE_DESIGN.md
API_SPEC.md
AGENT_SPEC.md
IMPLEMENTATION_PLAN.md

Seluruh keputusan implementasi harus mengikuti dokumen tersebut.

==================================================
LANJUTKAN PROJECT
==================================================

Identifikasi terlebih dahulu:

- Current Phase
- Current Sprint
- Current Module
- Last Completed Task
- Current Progress
- Next Module
- Next Sprint

Setelah itu LANJUTKAN PROJECT dari posisi terakhir.

Jangan mengulang sprint yang sudah selesai.

==================================================
DEVELOPMENT RULES
==================================================

Kerjakan hanya SATU sprint atau SATU modul dalam satu waktu.

Setiap sprint wajib mengikuti urutan:

1. Planning
2. Implementation
3. Self Review
4. Refactor
5. Testing
6. Build
7. Typecheck
8. Lint
9. README Update
10. CURRENT_STATE Update
11. CHANGELOG Update
12. Sprint Checklist Update
13. Finish

==================================================
QUALITY RULES
==================================================

Sebelum sprint dianggap selesai WAJIB:

- Review seluruh source code
- Cari bug
- Cari duplicate code
- Cari security issue
- Cari memory leak
- Cari performance issue
- Cari dependency issue
- Pastikan build berhasil
- Pastikan typecheck berhasil
- Pastikan lint berhasil

Jika ada error:

Perbaiki terlebih dahulu.

Jangan lanjut sprint berikutnya.

==================================================
README RULES
==================================================

README.md adalah Master Progress Project.

README wajib selalu diperbarui setelah setiap sprint.

README minimal memiliki:

# Project Status

Current Phase

Current Sprint

Current Module

Overall Progress (%)

Progress Checklist

Completed Modules

Completed Sprint

Current Sprint

Current Module

Next Module

Next Sprint

Architecture Version

Database Version

API Version

Agent Version

Developer Notes

Breaking Changes

Known Issues

TODO

==================================================
PROJECT HEALTH REPORT
==================================================

Tambahkan bagian berikut ke README.md

Project Health

Sprint

Overall Progress

Completed Modules

Current Module

Next Module

Build Status

Typecheck Status

Lint Status

Architecture Status

Database Status

API Status

Frontend Status

Backend Status

Known Issues

Ready For Next Sprint

==================================================
CURRENT_STATE.md
==================================================

Selalu update CURRENT_STATE.md

Isi minimal:

Project Name

Current Phase

Current Sprint

Current Module

Status

Completed Sprint

Completed Modules

Next Sprint

Next Module

Last Build

Last Typecheck

Last Lint

Architecture Version

Database Version

API Version

README Updated

CHANGELOG Updated

Last Update

==================================================
CHANGELOG.md
==================================================

Setiap sprint WAJIB menambahkan:

Tanggal

Sprint

Module

Feature

Files Created

Files Updated

Files Deleted

Database Changes

API Changes

Breaking Changes

Testing Result

Build Result

Typecheck Result

Lint Result

Next Sprint

==================================================
END OF SPRINT
==================================================

Setelah sprint selesai tampilkan ringkasan:

PROJECT STATUS

CURRENT PHASE

CURRENT SPRINT

CURRENT MODULE

COMPLETED MODULES

NEXT MODULE

NEXT SPRINT

PROJECT HEALTH

BUILD STATUS

TYPECHECK STATUS

LINT STATUS

==================================================
IMPORTANT
==================================================

Project ini akan dikerjakan oleh beberapa AI yang berbeda (DeepSeek, GPT, Claude, Gemini, atau lainnya).

Karena itu seluruh dokumentasi HARUS selalu diperbarui agar AI berikutnya dapat langsung melanjutkan project tanpa kehilangan konteks.

Selalu lanjutkan project dari status terakhir.

Jangan membuat ulang project.

Jangan mengulang sprint.

Jangan mengubah arsitektur tanpa persetujuan.

Selalu pastikan README.md, CURRENT_STATE.md, CHANGELOG.md, dan seluruh dokumentasi tetap sinkron setelah setiap sprint selesai.

```

# 
```

## Sprint Summary

Sprint: 6

Status:
✅ Complete

Modules Finished:
- Theme System
- UI Components
- Auth UI
- Dashboard
- Workspace
- API Client
- Auth Store

Verification:
- Build ✅
- Typecheck ✅
- Lint ✅

Project Health:
🟢 Stable

Next Sprint:
Agent UI
Chat Interface
File Explorer
Code Editor
Terminal

Resume Command:
LANJUTKAN PROJECT NOVAAGENT DARI README.md DAN CURRENT_STATE.md
```
# 
```

## AI Continuation Rules

Setiap AI yang melanjutkan project WAJIB:

1. Membaca README.md
2. Membaca CURRENT_STATE.md
3. Membaca CHANGELOG.md
4. Membaca IMPLEMENTATION_PLAN.md
5. Melihat Sprint terakhir
6. Melihat Next Module
7. Melanjutkan project
8. Tidak mengulang sprint sebelumnya
9. Tidak mengubah arsitektur
10. Setelah selesai wajib:
   - Testing
   - Self Review
   - Update README
   - Update CURRENT_STATE
   - Update CHANGELOG
`
# 
```

# CURRENT PROJECT STATE

Project:
NovaAgent

Current Phase:
Foundation

Current Sprint:
Sprint 4

Current Module:
Provider Service

Status:
In Progress

Completed Sprint:
✅ Sprint 1
✅ Sprint 2
✅ Sprint 3

Next Module:
Provider Service

After Next:
Agent Service

Last Build:
PASS

Last Typecheck:
PASS

Last Lint:
PASS

Architecture Version:
v1

Database Version:
v1

API Version:
v1

README:
Updated

CHANGELOG:
Updated

Implementation Plan:
Up To Date

IMPORTANT

Selalu baca file berikut sebelum coding:

README.md
CURRENT_STATE.md
CHANGELOG.md
ARCHITECTURE_BLUEPRINT.md
PRD.md
IMPLEMENTATION_PLAN.md

Jangan membuat project baru.
Lanjutkan project dari status terakhir.
`
# 
```
LANJUTKAN PROJECT NOVAAGENT YANG SUDAH ADA.

Jangan membuat project baru.
Jangan membuat ulang arsitektur.
Jangan mengubah struktur project yang sudah ada.

Sebelum mengerjakan apa pun:

1. Baca README.md sebagai Master Progress Project.
2. Baca CHANGELOG.md.
3. Baca seluruh dokumen berikut:
   - ARCHITECTURE_BLUEPRINT.md
   - PRD.md
   - UI_UX_SPEC.md
   - DATABASE_DESIGN.md
   - API_SPEC.md
   - AGENT_SPEC.md
   - IMPLEMENTATION_PLAN.md

Gunakan dokumen tersebut sebagai Source of Truth.

Kemudian identifikasi:

- Current Phase
- Current Sprint
- Current Module
- Last Completed Task
- Current Progress
- Next Module
- Next Task

Setelah memahami seluruh project, LANJUTKAN PROJECT dari posisi terakhir sesuai README.md.

Jangan mengulang pekerjaan yang sudah selesai.

Jangan mengubah implementasi yang sudah stabil kecuali diperlukan untuk bug fix atau peningkatan yang konsisten dengan arsitektur.

Ikuti seluruh Development Rules NovaAgent.

Setelah menyelesaikan modul:

- lakukan self review
- testing
- refactor bila diperlukan
- update README.md
- update CHANGELOG.md
- update checklist sprint
- tampilkan PROJECT STATUS terbaru
- tampilkan NEXT MODULE
- tampilkan NEXT PROMPT agar AI berikutnya dapat langsung melanjutkan project.

`
# 
```

Mulai saat ini ikuti aturan development NovaAgent berikut.

Jangan pernah mengerjakan seluruh proyek sekaligus.

Selalu ikuti dokumen berikut sebagai sumber kebenaran (Source of Truth):

1. ARCHITECTURE_BLUEPRINT.md
2. PRD.md
3. UI_UX_SPEC.md
4. DATABASE_DESIGN.md
5. API_SPEC.md
6. AGENT_SPEC.md
7. IMPLEMENTATION_PLAN.md

==================================================
DEVELOPMENT RULES
==================================================

- Kerjakan hanya SATU sprint atau SATU modul dalam satu waktu.
- Jangan mengubah arsitektur tanpa alasan yang jelas.
- Jangan membuat implementasi yang bertentangan dengan blueprint.
- Jangan menghapus fitur lama kecuali memang diminta.
- Semua implementasi harus modular.
- Semua kode harus production-ready.
- Semua perubahan harus backward-compatible jika memungkinkan.
- Setelah setiap tugas selesai, lakukan review internal terhadap hasil implementasi.

==================================================
README RULES
==================================================

README.md adalah Master Progress Project.

Setiap selesai mengerjakan tugas WAJIB memperbarui README.md.

README harus selalu memiliki bagian berikut:

# Project Status

Current Phase

Current Sprint

Current Module

Progress Checklist

Completed Tasks

Current Tasks

Next Tasks

Architecture Version

Database Version

API Version

Agent Version

Last Update

Developer Notes

Breaking Changes

Known Issues

TODO

==================================================
CHANGELOG
==================================================

Tambahkan changelog setiap selesai pekerjaan.

Format:

Tanggal

Sprint

Module

Feature

Files Created

Files Updated

Files Deleted

Database Changes

API Changes

Breaking Changes

Testing Result

Next Sprint

==================================================
IMPLEMENTATION
==================================================

Setiap modul WAJIB melewati urutan berikut:

1.
Planning

2.
Implementation

3.
Self Review

4.
Refactor

5.
Testing

6.
README Update

7.
Checklist Update

8.
Finish

==================================================
TESTING
==================================================

Setelah implementasi:

- Review seluruh source code
- Cari bug
- Cari duplicate code
- Cari security issue
- Cari performance issue
- Cari memory leak
- Cari dependency issue

Jika menemukan masalah:

Perbaiki terlebih dahulu.

Jangan lanjut sprint berikutnya.

==================================================
NEXT SESSION
==================================================

Setelah README diperbarui, tuliskan:

PROJECT STATUS

CURRENT SPRINT

CURRENT MODULE

NEXT MODULE

NEXT PROMPT

Agar AI berikutnya dapat langsung melanjutkan tanpa membaca ulang seluruh project.

==================================================
IMPORTANT
==================================================

README.md adalah dokumen yang wajib selalu diperbarui.

Jangan pernah menyelesaikan tugas tanpa memperbarui README.md.

README.md menjadi acuan utama apabila development dilanjutkan oleh AI lain (DeepSeek, GPT, Claude, Gemini, atau model lainnya).

Selalu pastikan seluruh dokumen tetap sinkron dengan README.md.
```

# 
```
Sekarang jangan langsung membuat source code.

Semua dokumen berikut sudah tersedia:
- ARCHITECTURE_BLUEPRINT.md
- PRD.md
- UI_UX_SPEC.md
- DATABASE_DESIGN.md
- API_SPEC.md
- AGENT_SPEC.md

Tugas berikutnya adalah membuat IMPLEMENTATION_PLAN.md.

Dokumen ini menjadi master plan implementasi NovaAgent.

Harus mencakup:

1. Development Phases
2. Module Dependency Graph
3. Build Order
4. Milestone
5. Sprint Planning
6. Folder Creation Order
7. Backend Implementation Order
8. Frontend Implementation Order
9. Database Migration Order
10. API Implementation Order
11. Authentication Implementation
12. Workspace Implementation
13. AI Provider Implementation
14. Agent Engine Implementation
15. File Manager Implementation
16. Code Editor Implementation
17. Terminal Implementation
18. Git Integration
19. Build System
20. Deployment System
21. Testing Strategy
22. CI/CD Plan
23. Documentation Strategy
24. Release Strategy
25. Rollback Strategy

Untuk setiap fase jelaskan:
- tujuan
- output
- dependensi
- estimasi kompleksitas
- risiko
- acceptance criteria

Tambahkan checklist implementasi yang sangat rinci sehingga setiap modul dapat dikerjakan satu per satu tanpa mengubah arsitektur.

Jangan membuat source code.

Jangan membuat file project.

Output hanya IMPLEMENTATION_PLAN.md yang akan menjadi acuan seluruh proses development.

```
# 
```
Sekarang lanjutkan proyek NovaAgent.

Jangan menulis kode sama sekali.

Berdasarkan:
- ARCHITECTURE_BLUEPRINT.md
- PRD.md

Buat dokumentasi enterprise-grade yang akan menjadi acuan implementasi seluruh proyek.

Buat dokumen berikut secara lengkap:

1. UI_UX_SPEC.md
- Design System
- Color Palette
- Typography
- Icon System
- Layout System
- Grid System
- Responsive Rules
- Dark & Light Theme
- Component Library
- Dashboard UI
- Login UI
- Workspace UI
- Chat UI
- AI Provider UI
- File Manager UI
- Code Editor UI
- Terminal UI
- Git UI
- Deployment UI
- Settings UI
- Admin UI
- Mobile UI
- Tablet UI
- Desktop UI
- User Flow
- UX Principles
- Loading State
- Empty State
- Error State
- Notification System

2. DATABASE_DESIGN.md
- Complete ERD
- Entity Description
- Table Definition
- Column Definition
- Relationships
- Constraints
- Index Strategy
- Partition Strategy
- Migration Strategy
- Backup Strategy
- Multi Workspace Design
- Audit Tables
- Soft Delete Strategy

3. API_SPEC.md
- REST API
- WebSocket API
- Authentication API
- Workspace API
- Project API
- Chat API
- AI Provider API
- Agent API
- File Manager API
- Editor API
- Terminal API
- Git API
- Build API
- Deploy API
- Admin API
- Response Format
- Error Codes
- Rate Limiting
- Versioning Strategy
- Authentication Flow

4. AGENT_SPEC.md
Dokumen ini menjadi otak NovaAgent.

Harus menjelaskan:
- Agent Architecture
- Agent Lifecycle
- Planner Agent
- Coding Agent
- Review Agent
- Debug Agent
- Build Agent
- Deployment Agent
- Documentation Agent
- Security Agent
- Git Agent
- File Agent
- Terminal Agent
- Context Manager
- Memory System
- Tool Registry
- Tool Permission
- Agent Communication
- Agent Orchestration
- Multi-Agent Collaboration
- AI Provider Selection Strategy
- Model Fallback Strategy
- Token Optimization Strategy
- Prompt Management
- Error Recovery
- Retry Strategy
- Safety Rules
- Approval Rules
- Workspace Isolation
- Logging
- Audit Trail
- Cost Optimization
- Performance Optimization
- Extensibility Strategy

Persyaratan:
- Enterprise-grade.
- Modular.
- Future-proof.
- Tidak membuat implementasi kode.
- Tidak membuat file source.
- Fokus pada spesifikasi teknis dan produk.
- Semua keputusan harus konsisten dengan ARCHITECTURE_BLUEPRINT.md dan PRD.md.
- Dokumen harus cukup lengkap sehingga developer dapat mulai implementasi tanpa mengubah arsitektur.

```
# PRD (Product Requirements Document)
```
Sekarang jangan menulis kode.

Buat Product Requirements Document (PRD) lengkap untuk NovaAgent.

Dokumen harus mencakup:

1. Product Vision
2. Target User
3. User Persona
4. User Journey
5. Core Features
6. MVP Features
7. Future Features
8. Functional Requirements
9. Non Functional Requirements
10. User Roles
11. Permission Matrix
12. Workspace Rules
13. AI Agent Rules
14. AI Provider Rules
15. Security Requirements
16. Performance Requirements
17. UI Principles
18. UX Principles
19. Business Rules
20. Success Metrics

Output dalam file:
PRD.md

Jangan membuat kode.
Jangan membuat database.
Jangan membuat API.

Fokus membuat spesifikasi produk enterprise yang menjadi acuan seluruh pengembangan berikutnya.

```
# Prompt 1 — Project Foundation & Architecture
```

Saya ingin membangun platform AI Agent berbasis web yang modular, scalable, dan mudah dikembangkan.

Jangan langsung membuat kode.

Tugas pertama adalah membuat perencanaan arsitektur proyek secara lengkap.

Buat dokumen yang berisi:

1. Project Architecture
2. Folder Structure
3. Technology Stack
4. Database Structure
5. Backend Architecture
6. Frontend Architecture
7. API Structure
8. Authentication Flow
9. Workspace Flow
10. AI Provider Flow
11. Agent Flow
12. File Manager Flow
13. Terminal Flow
14. Build Flow
15. Git Flow
16. Deployment Flow

Buat seluruh struktur menggunakan konsep modular sehingga setiap module dapat dikembangkan tanpa mengganggu module lain.

Setiap module harus memiliki:
- tujuan
- fungsi
- dependensi
- API yang digunakan
- alur data
- hubungan dengan module lain

Gunakan best practice enterprise.

Jangan membuat kode sama sekali.

Output hanya berupa blueprint dan roadmap teknis lengkap yang akan menjadi dasar pembangunan website AI Agent.
```
