# Privacy Policy

**Application**: CycleStack
**Effective Date**: May 5, 2026
**Last Updated**: May 7, 2026
**Contact**: shyu0732@gmail.com

## 1. Overview

CycleStack is a personal automation tool used by the CycleStack channel owner ([@CycleStack](https://www.youtube.com/@CycleStack)) to upload pre-rendered video episodes (Late-Cycle Scoreboard / Daily Briefing / Cycle Filter Framework series) and read channel analytics. This application is **not a public service** — it operates exclusively on the channel owner's own YouTube channel.

## 2. Information We Access

The application uses Google OAuth 2.0 with the following scopes:

| Scope | Purpose |
|---|---|
| `youtube.upload` | Upload pre-rendered video files (mp4) and thumbnails (PNG) to the owner's CycleStack channel with private visibility + scheduled publish time |
| `youtube.readonly` | Read channel metadata (subscriber count, video count) **and read top-level comments on the owner's own videos** for the owner's sentiment analysis dashboard |
| `yt-analytics.readonly` | Fetch view counts, retention curves, and CTR metrics for the owner's videos |

The application **does not access**:
- Other users' channels or videos
- Private user information from third parties

The application **does access**:
- Top-level comments on the channel owner's own videos (read via `commentThreads.list`) for the owner's sentiment analysis dashboard. Commenter usernames are visible (as they are public on YouTube) but are not shared with any third party.

## 3. How We Use Information

- **Video upload**: Pre-rendered mp4 files with metadata (title, description, tags) defined entirely by the channel owner. No user-generated content is processed by the application. Uploads use `private` visibility with `status.publishAt` scheduled — the owner alone controls when each video becomes public.
- **Analytics**: View counts, retention, CTR, and comment sentiment fetched read-only and used for the owner's local dashboard. Not shared with third parties.
- **Authentication**: OAuth 2.0 refresh tokens stored locally on the owner's machine (`.env`) and on a private Render service environment (`cyclestack-worker`, service-level environment variables — isolated from the shared Render env group). The application never transmits tokens externally.

## 4. Data Storage

- **OAuth refresh tokens**: stored in private environment files (`.env`) on the owner's local machine and on a private Render service environment (`cyclestack-worker` service-level variables). Refresh tokens may be displayed in the local terminal once during initial authorization (`oauth_init.py` first run); the application itself never transmits tokens externally.
- **Video files (mp4)**: stored locally on the owner's machine before upload. Retention managed by the owner.
- **Analytics data** (views, retention, CTR, comment sentiment): fetched periodically (typically weekly) and stored in a private database (Neon Postgres) for the channel owner's longitudinal performance analysis. Retained indefinitely for the owner's own use. **Not shared with any third party.**
- **No personal data of viewers** (beyond publicly-visible commenter usernames on the owner's own videos) is collected or stored.

## 5. Data Sharing

This application **does not share any data with third parties.**

## 6. Data Retention

- OAuth tokens persist until manually revoked via [Google Account permissions](https://myaccount.google.com/permissions).
- Local video files managed by the owner directly.
- Analytics data persisted in private database; retention managed by the channel owner. Deletion request: contact shyu0732@gmail.com.

## 7. User Rights

The channel owner can:
- Revoke this application's access at any time via [Google Account permissions](https://myaccount.google.com/permissions)
- Delete uploaded videos at any time via [YouTube Studio](https://studio.youtube.com/)
- Request deletion of any cached data by contacting shyu0732@gmail.com

## 8. Children's Privacy

This application is not intended for use by individuals under 13. The CycleStack channel content is marked as not made for kids.

## 9. Changes to This Policy

We may update this Privacy Policy. The "Last Updated" date indicates when changes were made. Material changes will be communicated via the channel owner's contact email.

### Change log

- **2026-05-07** — Application name updated from "CycleStack YouTube Lead" to **"CycleStack"** (Google OAuth app name uniqueness policy compliance — brand-only naming required). Scope list and operational scope clarified (BR / DBA / EP series upload + scheduled publish + own-channel comment read for dashboard). No new data collection added.
- **2026-05-05** — Initial publication.

## 10. Contact

For privacy-related questions or data deletion requests:
**shyu0732@gmail.com**
