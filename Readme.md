# my mixtape

A personal music profile page — a glass-style "now playing" card with a
custom playlist, profile info, and social links, built as a single
self-contained HTML file.

**Live site:** https://lyzymusiclists.onrender.com

## Features

- Glassmorphic (frosted glass) UI over a custom GIF background
- YouTube-powered playback with play/pause, skip, shuffle, repeat, and
  a draggable seek bar
- Custom playlist with optional cover art and duration per track
- Autoplay on first visit (starts muted, unmutes on first tap — this
  is a browser rule, not something the page controls)
- Volume slider, favicon, and social links row
- Small animations throughout: ripple taps, marquee for long titles,
  crossfade between songs, floating music notes while playing, a
  glowing play button, mouse-tilt on the album art, and a staggered
  playlist entrance

## Editing your info

Everything personal lives near the top of the `<script>` block in
`index.html` — no build tools or dependencies needed:

| What | Variable |
|---|---|
| Playlist | `playlist` array — YouTube video ID, title, artist, optional `art` and `duration` |
| Background | `DEFAULT_BG_URL` |
| Profile photo | `AVATAR_URL` |
| Name & bio | `PROFILE_NAME`, `PROFILE_CAPTION` |
| Social links | `SOCIAL_LINKS` array |

Edit the values, save, commit, and push — that's it.

## Tech

Plain HTML, CSS, and vanilla JavaScript. No frameworks, no build step.
Music playback uses the official [YouTube IFrame Player API](https://developers.google.com/youtube/iframe_api_reference).

## Deployment

Hosted as a static site on [Render](https://render.com), auto-deployed
from this GitHub repo on every push to the main branch.

## License

All rights reserved — see [`LICENSE`](./LICENSE). This code is not
open source; please don't copy or redistribute it without permission.
