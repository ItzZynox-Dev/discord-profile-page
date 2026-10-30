# Discord Profile Page

**English** | [فارسی](README.fa.md)

A single-file, dependency-free personal profile page with a **live Discord status**: avatar, avatar decoration, badges, online/idle/DND state, and what you're playing or listening to on Spotify. Dark theme, responsive, no build step.

## Features

- Live Discord presence, name, avatar, avatar decoration and badges via the [Lanyard](https://github.com/Phineas/lanyard) API (refreshes every 20 s)
- Social link cards (Telegram, YouTube, X/Twitter, Instagram, TikTok, GitHub, Twitch, LinkedIn, Website)
- Tech-stack panel with inline SVG icons
- Fully responsive, one `index.html` file, no framework

## Quick start

1. **Join the Lanyard server** → <https://discord.gg/lanyard>. Lanyard only tracks users who are in this server, so without this step the status will not load.
2. Enable Developer Mode in Discord (*Settings → Advanced → Developer Mode*), right-click your own name and choose **Copy User ID**.
3. Open `index.html` and edit the config block at the top of the `<script>`:

   ```js
   const DISCORD_ID = "YOUR_DISCORD_USER_ID";

   const PROFILE = {
     displayName: "Your Name",
     pageTitle:   "My Profile",
     about:       "Write a short introduction about yourself here…",
   };
   ```

4. Update the `socials` array: set `value` (the text shown) and `link`. Set `link: ""` to hide a card.
5. Edit or remove entries in the `stack` array to match your skills.
6. Open `index.html` in a browser to preview it.

## Optional: extra badges

Nitro, Server Booster and Quest/Orb badges are not exposed by Discord's public API. Add them manually in `STATIC_BADGES` (the file contains step-by-step instructions on how to find each badge hash).

## Deploy for free with GitHub Pages

1. Fork this repo (or push your copy to a new repository).
2. Go to **Settings → Pages**.
3. Under *Build and deployment*, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. Your page will be live at `https://<username>.github.io/<repo>/` within a minute or two.

## Notes

- The page loads fonts from Google Fonts and data from `api.lanyard.rest` and `cdn.discordapp.com`, so it needs an internet connection.
- If the status shows an error, open the browser console (F12) for details. The most common cause is not having joined the Lanyard server.

## Credit (required)

The footer shows **"Created by [ItzZynox](https://github.com/ItzZynox-Dev)"**. This credit is part of the license and is verified by the page's script: if it is removed, edited or hidden, the page will stop working. Please keep it intact.

## License

[MIT with Attribution Requirement](LICENSE) — free to use, modify and share, as long as the footer credit stays.
