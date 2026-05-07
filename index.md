# CycleStack

**Personal channel automation tool for the CycleStack YouTube channel**

## What This App Does

CycleStack is a personal-use automation application that:

1. **Uploads pre-rendered videos** (BR series — Late-Cycle Scoreboard / DBA series — US Market Daily Briefing with AI / EP series — Cycle Filter Framework) to the [CycleStack YouTube channel](https://www.youtube.com/@CycleStack)
2. **Schedules video publish times** via the YouTube Data API (`status.publishAt`)
3. **Fetches channel analytics** (views, retention, CTR, comment sentiment) for the channel owner's local dashboard
4. **Manages video metadata** (title, description, tags) for pre-rendered videos
5. **Reads top-level comments** on the channel owner's own videos for the owner's local sentiment analysis dashboard

This is **not a public service**. The application is used exclusively by the channel owner ([shyu0732@gmail.com](mailto:shyu0732@gmail.com)) on their own CycleStack channel.

## OAuth Scopes Used

| Scope | Why we use it |
|---|---|
| `youtube.upload` | Upload pre-rendered mp4 files + thumbnails to own channel (private + scheduled publish) |
| `youtube.readonly` | Read own channel metadata + top-level comments on own videos for dashboard |
| `yt-analytics.readonly` | Fetch own video analytics (views / retention / CTR) for performance review |

**Own channel only** — no other channels are accessed.

## Privacy

This application does not collect, store, or share any user data with third parties. See the [Privacy Policy](./privacy-policy.html) for full details.

## OAuth Verification Demo

OAuth Consent Flow Demo + Upload Episode Demo (private + scheduled) recordings available — see internal spec at `docs/legal/oauth-demo-video-spec.md` (production repo, audit-trail).

## Source Code

The application source is private. Production deployment uses Google Cloud Console OAuth with Render service-level environment isolation (`cyclestack-worker` service).

## Contact

**shyu0732@gmail.com**

---

*Last Updated: 2026-05-07*
