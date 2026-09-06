# tiktok-yt-automation-10 — "Cat Chaos Lab"

Daily automated re-upload: TikTok source → YouTube Shorts.

- **Source:** TikTok `@bro.and.dickens` (chaotic / funny cat content)
- **Target channel:** "Cat Chaos Lab" (@catchaoslab-l4u) on `dkdhaker00011@gmail.com`
- **Format:** Shorts, `popular_only` (most-viewed unposted clip)
- **Schedule:** 2 uploads/day at **16:00 & 23:00 UTC** (12 PM & 7 PM US Eastern) — self-scheduled via GitHub Actions `schedule:` cron
- **SEO:** English AI titles/description/tags via Gemini (audio + frames), Anthropic then template fallback; unique-title guard
- **Edit:** loudnorm, light sharpen/colour, small cat-lab corner badge (`assets/brand_badge.png`)
- **Category:** 15 (Pets & Animals)

## Secrets (GitHub → Settings → Secrets → Actions)
- `CHANNEL_10_CLIENT_SECRET` — base64 of the OAuth desktop client JSON
- `CHANNEL_10_TOKEN` — base64 of the minted token JSON (scopes: youtube.upload + youtube.force-ssl)
- `GEMINI_API_KEY` — for AI SEO

## Manual run
Actions → "Channel 10 - Daily Upload SLOT 1/2" → Run workflow (`dry_run` / `force` inputs).
