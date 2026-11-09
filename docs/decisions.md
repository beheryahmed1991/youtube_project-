# Decision log

## 001 — Keep coordination small (2026-11-09)

Use a supervisor chat and one implementation chat initially. Add independent
review once a working slice exists. This limits coordination overhead within
30–40 available hours. The repository notes carry decisions between chats.

## 002 — Prove video and deployment early (2026-11-09)

The first working slice must establish real storage, browser playback, access
control and reproducible deployment. These are central to the brief and carry
more integration uncertainty than static screens. Follow with required feature breadth.

## 003 — Proposed compact architecture (2026-11-09)

Prefer a modular FastAPI application, PostgreSQL and separate FFmpeg worker.
Start with private persistent filesystem storage and a storage interface.
This reduces services and setup requirements. The tradeoff is single-host
storage and no claim of distributed scalability. Validate before finalizing.

## 004 — Preserve evidence from the beginning (2026-11-09)

Native conversations and actual AI configuration are deliverables, not optional
notes. Verify export/retrieval before substantial coding. Do not reconstruct
conversation logs or fabricate development history at submission time.

