# Useful Websites 🧰

> A hand-picked list of genuinely useful websites, sorted by category. Free first, no-signup preferred, privacy-friendly always.

Every site here was tested by hand. Sites that process files **locally in your browser** (no upload) are marked with 🔒.

## Contents

- [Video Compression](#video-compression)
  - [Compress video for Discord (2026)](#compress-video-for-discord-2026)
  - [Other platforms: WhatsApp, Gmail, TikTok…](#other-platforms)
- [Video Tools](#video-tools)
- [Contributing](#contributing)

**Legend:** 🔒 runs in your browser, files never uploaded · 🆓 free · 🚫 no signup · 💻 desktop app

---

## Video Compression

### Compress video for Discord (2026)

Discord's upload limits right now ([official FAQ](https://support.discord.com/hc/en-us/articles/25444343291031-File-Attachments-FAQ)):

| Account | Max file size |
|---|---|
| Free | **20 MB** (raised from 10 MB) |
| Nitro Basic | 50 MB |
| Nitro | 500 MB |

If a clip is bigger than your limit, Discord won't send it. Here are the best ways to shrink it:

#### ⭐ Top pick: [SquishyFile Discord Video Compressor](https://squishyfile.com/discord-video-compressor) 🔒🆓🚫

The fastest way to get a video under Discord's 20 MB limit. Pick your plan (Free 20 MB / Nitro Basic 50 MB / Nitro 500 MB), drop the file in, and it works out the bitrate to hit that size.

- **Nothing gets uploaded.** Compression runs in your browser, so a 2 GB clip doesn't need a 2 GB upload first. It's also fine for private videos.
- **Target size, not guesswork.** It compresses to the exact MB limit, so you don't need to try "medium quality" three times.
- **Handles most formats:** MP4, MOV, MKV, AVI, WebM → outputs H.264 MP4, which plays inline in Discord on desktop and mobile.
- **Fast on modern browsers:** uses hardware WebCodecs encoding, with an FFmpeg (WebAssembly) fallback for older formats.
- No watermark, no queue, no account, no file cap.

👉 **[squishyfile.com/discord-video-compressor](https://squishyfile.com/discord-video-compressor)**

Still on an old 8 MB workflow? → [8MB Video Compressor](https://squishyfile.com/8mb-video-compressor)

#### Other options

| Tool | Type | Good for | Keep in mind |
|---|---|---|---|
| [HandBrake](https://handbrake.fr/) 💻🆓 | Open-source desktop app | Full control over codec, bitrate, and filters; batch jobs | You have to install it and calculate the bitrate yourself |
| [FFmpeg](https://ffmpeg.org/) 💻🆓 | Command line | Scripting, automation, power users | No GUI; you need to know the flags |
| [8mb.video](https://8mb.video/) 🆓 | Online, server-side | Quick one-off jobs | Uploads your file to a server; slow on big files |
| [FreeConvert](https://www.freeconvert.com/video-compressor) 🆓 | Online, server-side | Many codec options | Upload + queue; the free tier has limits |
| [VEED](https://www.veed.io/tools/video-compressor) | Online editor | Also editing and subtitles | Upload required; best features are paid |

📖 Full guide with a bitrate cheat sheet: **[How to compress a video for Discord (2026)](guides/compress-video-for-discord.md)**

### Other platforms

The same tool has one-click presets for other upload limits: **[SquishyFile Video Compressor](https://squishyfile.com/)** 🔒🆓🚫

| Platform | Limit | Preset |
|---|---|---|
| WhatsApp | 16 MB | ✅ |
| Discord Free | 20 MB | ✅ |
| Gmail / Messenger | 25 MB | ✅ |
| Discord Nitro Basic | 50 MB | ✅ |
| LinkedIn | 200 MB | ✅ |
| Discord Nitro / TikTok | 500 MB | ✅ |

---

## Contributing

Know a site that belongs here? Open a PR or an issue. Rules:

1. It must be free or have a useful free tier.
2. No sites that force signup just to try the core feature.
3. One line on **why** it's useful, not marketing copy.

⭐ Star the repo if it saved you time.
