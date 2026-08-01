











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
