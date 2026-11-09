# Requirements and acceptance checklist

Baseline: all three pages of the linked TZ-YouTube-kopiya.docx were read in the
supervisor chat. The parent sources/тз.pdf is preserved as reference; its text
layer is empty, and equivalence to the linked document has not been independently verified.

The brief says ten days from receipt. Receipt date and recruiter clarification
are pending. Repository creation is not an established deadline trigger.
Planning budget: approximately 30–40 hours, to be adjusted once dates are known.

Every item below is OPEN. Acceptance details are our interpretation of how to
prove the brief; they must not be represented as extra recruiter requirements.

| ID | Requirement from brief | Acceptance evidence |
| --- | --- | --- |
| F01 | Home feed with video thumbnails | Seeded public ready videos render and open; private/hidden videos are excluded according to access policy. |
| F02 | Player, likes, comments | Real uploaded video plays and seeks; signed-in user can like and comment; behavior persists after reload. |
| F03 | Channel videos, playlists, subscription | Channel shows creator content; owner manages a playlist; another user can subscribe/unsubscribe. |
| F04 | Search by title | Known title query finds matching accessible videos and handles no results. |
| F05 | File upload, progress, metadata | Upload real file, show transfer progress and separate processing status, save title/description, expose a playable result. |
| F06 | Login and registration | Register, login, logout; protected actions reject unauthenticated users. |
| F07 | Reports and hiding videos | User reports a video; moderator sees report and hides video; viewers lose access. |
| F08 | User, moderator, administrator roles | A documented permission matrix is enforced by the API, including administrator-only role management. |
| F09 | Private videos only for owner-authorized people | Owner grants/revokes access; unauthorized metadata, thumbnails and media requests fail; revocation affects later requests. |
| S01 | Uploading, storing and serving video is central | Durable storage survives service restart; media delivery supports browser playback and seeking. |
| T01 | Python + FastAPI + PostgreSQL | Actual application and persistent data use the prescribed stack. |
| T02 | Swagger at /docs | Running service exposes usable generated API documentation. |
| T03 | Simple frontend | All listed screens connect to real backend behavior. |
| D01 | One-command deployment on clean Ubuntu | Rehearsal on a clean VM starts app, database, storage and background processing with documented prerequisites. |
| D02 | Register → upload → watch → like/comment immediately after deployment | Browser journey succeeds against the deployed system. |
| D03 | README, docs, automated tests, demo seed script | Reviewer can follow instructions, run tests and seed users/videos/comments. |
| A01 | All code through AI; prompts submitted | Original tool-generated project conversations collected, including coding and review sessions. |
| A02 | Complete agent configuration | Actual rules, agents, skills, settings and MCP configurations used are inventoried and included as applicable. |
| G01 | Full Git repository and all commits in ZIP | Unzipped .git opens; log shows meaningful incremental development; no fabricated/squashed history. |

## Evaluation dimensions

Feature breadth; similarity to YouTube; deployment reliability; architecture;
database design; AI configuration/workflow; security; meaningful Git history.
No scoring weights are given.

## Release gates we choose

- No known unauthorized private-video or hidden-video access.
- Critical behavior has meaningful passing tests, including negative cases.
- Clean-Ubuntu deployment and main browser journey demonstrated.
- Demo data uses small generated or properly licensed media.
- Native conversation collection and configuration inventory verified.
- ZIP checked after extraction, including hidden .git directory.

## Scope boundaries

Livestreaming, advertising, monetization, advanced recommendations, and multiple
resolution ladders are not explicitly required. Defer them unless all listed
requirements and release gates are satisfied with time remaining.

