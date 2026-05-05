# Privacy Policy

**Application**: CycleStack YouTube Lead
**Effective Date**: May 5, 2026
**Last Updated**: May 5, 2026
**Contact**: shyu0732@gmail.com

## 1. Overview

CycleStack YouTube Lead is a personal automation tool used by the CycleStack channel owner ([@CycleStack](https://www.youtube.com/@CycleStack)) to upload daily market briefing videos and read channel analytics. This application is **not a public service** — it operates exclusively on the channel owner's own YouTube channel.

## 2. Information We Access

The application uses Google OAuth 2.0 with the following scopes:

| Scope | Purpose |
|---|---|
| youtube.upload | Upload pre-rendered video files (mp4) and thumbnails (PNG) to the owner's CycleStack channel |
| youtube.readonly | Read channel metadata (subscriber count, video count) for the owner's analytics dashboard |
| yt-analytics.readonly | Fetch view counts, retention curves, and CTR metrics for the owner's videos |

The application **does not access**:
- Other users' channels or videos
- Comment data beyond the owner's own video comments
- Any private user information from third parties

## 3. How We Use Information

- **Video upload**: Pre-rendered mp4 files with metadata (title, description, tags) defined entirely by the channel owner. No user-generated content is processed.
- **Analytics**: View counts, retention, CTR fetched read-only and displayed in the owner's local dashboard. Not shared with third parties.
- **Authentication**: OAuth 2.0 refresh tokens stored locally on the owner's machine and on a private Render service (cyclestack-worker, service-level environment variables). Never transmitted to third parties.

## 4. Data Storage

- **OAuth refresh tokens**: stored in private environment files (.env) and Render service-level environment variables. Not transmitted externally.
- **Video files (mp4)**: stored locally on the owner's machine before upload. Retention managed by owner.
- **Analytics data**: fetched on-demand, displayed in real-time. Not persisted in a database.
- **No personal data of viewers** is collected, stored, or processed.

## 5. Data Sharing

This application **does not share any data with third parties**.

## 6. Data Retention

- OAuth tokens persist until manually revoked via [Google Account permissions](https://myaccount.google.com/permissions).
- Local video files managed by the owner directly.
- Analytics data not persisted.

## 7. User Rights

The channel owner can:
- Revoke this application's access at any time via [Google Account permissions](https://myaccount.google.com/permissions)
- Delete uploaded videos at any time via [YouTube Studio](https://studio.youtube.com/)
- Request deletion of any cached data by contacting shyu0732@gmail.com

## 8. Children's Privacy

This application is not intended for use by individuals under 13. The CycleStack channel content is marked as not made for kids.

## 9. Changes to This Policy

We may update this Privacy Policy. The "Last Updated" date indicates when changes were made. Material changes will be communicated via the channel owner's contact email.

## 10. Contact

For privacy-related questions or data deletion requests:
**shyu0732@gmail.com**
