---
tags:
  - Command
  - Inline command
  - Version 1.0.0
---

# Video

Send video using it's url. This command is useful if you, for example, don't want to download the video on your device or want to download TikTok video without a watermark.

???+ note "Note"

    Note that video size must not exceed **50MB**. This limit is set by Telegram API. 
    For YouTube videos this is usually ~10m length videos since Mahiru uses best available 
    resolution. For TikTok this is almost any video with some rare exceptions.

Currently, supported platforms are:

- YouTube
- TikTok
- Instagram

### Arguments

**url, u**  `url` — Url to the video you want to send.
**description, d** `string (optional)` — Description to send with the video.

### Examples

#### Default
+ `/video https://youtube.com/watch?v=GFG4o32NzRc`
+ `/video --u: https://youtu.be/mgh07DuvAWM --description: NGL the edit is pretty cool.`

#### Inline
+ `@MahiruShiinaBot video: https://youtu.be/uKxyLmbOc0Q`
+ `@MahiruShiinaBot video: --url: https://youtu.be/G7v3T5pDj-M --d: Check out this awesome OP!`