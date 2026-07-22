# Prompt-website-novaagent











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
