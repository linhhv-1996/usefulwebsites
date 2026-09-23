# How to Compress a Video for Discord (2026 Guide)

> **TL;DR:** Discord Free caps uploads at **20 MB**. The quickest fix is [SquishyFile's Discord Video Compressor](https://squishyfile.com/discord-video-compressor): pick "Free 20 MB", drop your clip in, and download an MP4 that fits. It runs in your browser, so nothing gets uploaded.

← [Back to the list](../README.md)

## Discord upload limits in 2026

| Account | Limit |
|---|---|
| Free | **20 MB** |
| Nitro Basic | 50 MB |
| Nitro | 500 MB |

Discord raised the free limit from 10 MB to 20 MB ([source](https://support.discord.com/hc/en-us/articles/25444343291031-File-Attachments-FAQ)). A lot of older guides still say 8 MB, 10 MB, or 25 MB. For free accounts, **20 MB** is the number that counts now.

## Why your clip is too big

File size depends on just two things:

```
file size = bitrate × duration
```

A phone recording at 1080p/60fps often runs at 15–20 Mbps, which is about **2 MB per second**. Ten seconds of footage and you've already used the whole free limit. Resolution, frame rate, and codec only matter because they change how much bitrate you need to look decent.

## Method 1: Compress in the browser (recommended)

**[SquishyFile Discord Video Compressor](https://squishyfile.com/discord-video-compressor)**

1. Open the page and choose your plan: **Free (20 MB)**, Nitro Basic (50 MB), or Nitro (500 MB).
2. Drag in your video (MP4, MOV, MKV, AVI, WebM…).
3. Hit compress, then download the MP4 and drop it into Discord.

Why this beats most "online compressors":

- **No upload step.** Server-based tools make you upload the full-size file first. That's the slow part, and your video ends up on someone else's server. SquishyFile encodes on your own device.
- **Hits the exact size.** It calculates the bitrate from the duration, so you get one pass instead of guessing.
- **Discord-friendly output.** H.264 MP4 previews inline on desktop, web, iOS, and Android.
- No watermark, no signup, no file-size cap, no daily limit.

## Method 2: HandBrake (desktop)

[HandBrake](https://handbrake.fr/) is free and open source. It's a good choice if you want full control or need to batch many files.

1. Load the video and pick the **Fast 720p30** preset.
2. Under **Video**, choose **Avg Bitrate** and enter the value from the cheat sheet below.
3. Tick **2-pass encoding** for better accuracy, then start the encode.

The catch: you need to install it and work out the bitrate yourself.

## Method 3: FFmpeg (command line)

For a 60-second clip aimed at 20 MB:

```bash
ffmpeg -i input.mp4 -c:v libx264 -b:v 2400k -pass 1 -an -f mp4 /dev/null && \
ffmpeg -i input.mp4 -c:v libx264 -b:v 2400k -pass 2 -c:a aac -b:a 128k -vf scale=-2:720 output.mp4
```

(On Windows, use `NUL` instead of `/dev/null`.)

## Bitrate cheat sheet for 20 MB

Formula (with ~5% headroom for container overhead):

```
video kbps ≈ (target MB × 8192 × 0.95) ÷ seconds − audio kbps
```

| Clip length | Video bitrate | Audio | Suggested resolution |
|---|---|---|---|
| 15 s | ~10,000 kbps | 128k | 1080p60 |
| 30 s | ~5,000 kbps | 128k | 1080p |
| 60 s | ~2,450 kbps | 128k | 720p–1080p30 |
| 90 s | ~1,600 kbps | 128k | 720p |
| 2 min | ~1,150 kbps | 128k | 720p |
| 3 min | ~770 kbps | 96k | 540p / 480p |
| 5 min | ~420 kbps | 96k | 480p |

For a 50 MB limit (Nitro Basic), multiply the video bitrate by about 2.5.

SquishyFile does this math for you. The table is for when you're using HandBrake or FFmpeg.

## Tips to keep quality up

- **Trim first.** Cutting 10 seconds of dead air saves more space than any codec setting.
- **Drop to 30 fps** unless it's fast gameplay. That frees up bitrate for sharpness.
- **Lower the resolution before you lower the bitrate too far.** A clean 720p looks better than a blocky 1080p.
- **Stick with H.264 for Discord.** HEVC/H.265 and AV1 files are smaller, but they don't always preview inline on every client.

## FAQ

**Does Discord compress videos for me?**
No. If a file is over your limit, Discord just refuses the upload. You have to shrink it first.

**What's the free limit in 2026: 8, 10, 20, or 25 MB?**
It's **20 MB** for free accounts. 8 MB was the old limit, 10 MB came after that, and 25 MB is Gmail/Messenger (and a figure from older Discord articles).

**How long a video can I send under 20 MB?**
At 720p, about 1.5–2 minutes looks good. Past about 3 minutes, you'll need 480p or lower.

**Can I compress on my phone?**
Yes. [squishyfile.com](https://squishyfile.com/discord-video-compressor) works in mobile Chrome and Safari, with no app to install.

**Is it safe for private videos?**
With SquishyFile, the file never leaves your device. With server-based compressors, read their privacy policy first.

---

Related: [WhatsApp 16 MB](https://squishyfile.com/) · [Gmail 25 MB](https://squishyfile.com/) · [MP4 to GIF](https://squishyfile.com/mp4-to-gif) · [8 MB compressor](https://squishyfile.com/8mb-video-compressor)
