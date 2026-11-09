# Proposed architecture

Status: proposal to validate with an early deployment/video spike.

## Shape

- React + TypeScript frontend for the listed screens.
- One FastAPI backend, organized into accounts, videos, social features and moderation modules.
- PostgreSQL for relational metadata and durable processing job records.
- A separate worker using FFmpeg to validate/process video and create thumbnails.
- Private local media storage in a persistent Docker volume, accessed through an internal storage interface.
- Docker Compose for the application, worker, database and persistent storage.

These optional technology choices are ours; only FastAPI/Python, PostgreSQL,
Swagger and clean-Ubuntu one-command deployment are fixed by the brief.
Avoid a separate queue service initially; validate job claiming, retry and recovery
in the PostgreSQL-backed worker before committing to that design.

## Video lifecycle

Upload → validate → persist → queue → process → ready or failed.
Store processing state and failure details; expose useful status to the owner.
Use supported browser-playable output and byte-range delivery for seeking.
Bound upload size, processing time and resource use. Clean up failed partial files.
Claim jobs safely and recover interrupted processing without duplicate published results.

## Access policy to implement and test

- Guest: discover and watch public ready videos that are not hidden.
- User: guest access plus upload, social actions, reports, and authorized private viewing.
- Owner: manage own metadata/playlists and private grants; inspect own processing status.
- Moderator: review reports and hide videos. No blanket private-media viewing permission.
- Administrator: manage roles and moderation. No implicit private-media access without an explicit documented decision.

Hiding blocks playback for ordinary viewers regardless of prior grants; owner
and moderation inspection behavior must be documented. Apply one shared policy
to details, listings, search, channel/playlist entries, thumbnails and media.
Store media outside a public static web directory; never expose private files
through an unprotected storage URL.

Use secure password hashing and a browser authentication strategy selected after
reviewing current framework guidance. Cover authorization, session expiry,
cross-site request risks and input validation in that decision.

## Initial relational model

Users; videos; processing jobs; private access grants; likes; comments;
subscriptions; playlists; ordered playlist items; reports.
Specify ownership, foreign keys, uniqueness and deletion behavior before migrations.
Binary media lives in storage; metadata and storage references live in PostgreSQL.

## Verification priorities

Real PostgreSQL integration tests for ownership, grants, roles and job behavior;
browser tests for the main journey; playback/seek checks; restart persistence;
fresh Ubuntu deployment. Record measured results, not assumptions.

