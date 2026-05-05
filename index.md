# CycleStack YouTube Lead

**Personal automation tool for CycleStack YouTube channel uploads and analytics**

## What This App Does

CycleStack YouTube Lead is a personal-use automation application that:

1. **Uploads daily market briefing videos** (DBA series — "US Market Daily Briefing with AI") to the [CycleStack YouTube channel](https://www.youtube.com/@CycleStack)
2. **Schedules video publish times** via the YouTube Data API
3. **Fetches channel analytics** (views, retention, CTR) for the channel owner's local dashboard
4. **Manages video metadata** (title, description, tags) for pre-rendered videos

This is **not a public service**. The application is used exclusively by the channel owner ([shyu0732@gmail.com](mailto:shyu0732@gmail.com)) on their own CycleStack channel.

## OAuth Scopes Used

| Scope | Why we use it |
|---|---|
| youtube.upload | Upload pre-rendered mp4 files + thumbnails to own channel |
| youtube.readonly | Read own channel metadata for dashboard |
| yt-analytics.readonly | Fetch own video analytics for performance review |

## Privacy

This application does not collect, store, or share any user data with third parties. See the [Privacy Policy](./privacy-policy.html) for full details.

## Source Code

The application source is private. Production deployment uses Google Cloud Console OAuth with Render service-level environment isolation.

## Contact

**shyu0732@gmail.com**
