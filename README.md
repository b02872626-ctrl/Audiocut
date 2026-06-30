# AudioCut 🎵

A lightweight, single-page **audio cutting & marking tool**. Import an audio file, scrub the
waveform, drop single-point markers or start→end range clips, label them (title, category,
tags, notes, color), and play each clip back from a card list. Everything is saved locally in
your browser, keyed by filename.

Also works as a **Telegram Mini App**.

## Features
- Waveform display with click + drag-to-scrub seeking
- Single-point markers and range clips
- Per-clip mini player: play/pause, ±5s, draggable progress scrubber
- Search across title / category / tags / notes
- Keyboard shortcuts: `Space` play/pause, `←/→` skip 5s, `M` marker, `[` set start, `]` set end
- Auto-save to `localStorage` by filename

## Deploy
Static site — no build step. The app is a single `index.html`.

**Vercel:** import this repo; framework preset = **Other**, build command = none,
output directory = `.` (root). Done.

## Telegram Mini App
1. Deploy to get an HTTPS URL (e.g. `https://audiocut.vercel.app`).
2. In [@BotFather](https://t.me/BotFather): `/newapp` (or `/mybots` → Bot Settings →
   Menu Button) and set the Web App URL to your deployed URL.

## Tech
Plain HTML/CSS/JS + [WaveSurfer.js](https://wavesurfer.xyz/) (loaded from CDN). No bundler.
