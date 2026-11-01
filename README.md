# Loop — video community

A responsive creator-video discovery experience for **yt-replica**. Static frontend, backed by Supabase Auth, Postgres and Storage.

## Features
- Search and category discovery with a responsive sidebar and video cards
- Email account signup/sign in, creator channels and profile basics
- Video uploads to the public `videos` Storage bucket
- Like, follow and comment actions for database videos
- Notifications panel and shareable video links
- Curated demo feed so the homepage looks alive before creators upload

## Hosting
Netlify build command: leave blank. Publish directory: `.`. These settings are in `netlify.toml`.

Connect **Arslan-Dev918/yt-replica** to a Netlify site and deploy the `main` branch.

## Supabase
The app is wired to the `videohub` Supabase project in Mumbai. The browser uses its publishable key, protected by row-level security. Never put a service-role key in frontend code.

Database tables: `profiles`, `channels`, `videos`, `video_likes`, `comments`, `channel_subscriptions`, and `notifications`. Video files use the public `videos` storage bucket (100 MB limit). Schema and access policies are applied to the connected Supabase project.

For local preview, serve this directory with any static web server; opening `index.html` directly may limit browser APIs such as clipboard access.
