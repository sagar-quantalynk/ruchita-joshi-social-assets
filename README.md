# Instagram launch assets

Generated 2026-05-20. All brand-aligned. All ready to upload.

## What's here

```
social-assets/
├── profile-photo.jpg         (1080×1080) Profile photo — upscaled brand logo
├── highlights/               (1080×1920 each — Instagram Story Highlight covers, 6 files)
├── posts/                    (1080×1350 each — Day N feed title cards, 14 files)
├── carousels/                (1080×1350 each — body slides for the carousel days, 24 files)
│   ├── day-01-slide-2..6     Five boundaries (one per slide, numbered watermark)
│   ├── day-03-slide-2..3     Akashic vs Soul Letter (two doorway concept cards)
│   ├── day-05-slide-2..4     Three rules for writing questions
│   ├── day-09-slide-2..3     A reading / therapy (two concept cards)
│   ├── day-10-slide-2..7     Six grief questions (big-quote variant)
│   └── day-14-slide-2..7     Six doorways (concept cards with price + duration)
└── templates/                Source HTML + CSS (regenerable)
```

## Carousel posting (Days 1, 3, 5, 9, 10, 14)

For each carousel day, Instagram lets you upload up to 20 images in a single post. The order matters — Instagram preserves it.

| Day | Title slide | Body slides | Total |
|---|---|---|---|
| 1 | `posts/day-01.png` | `carousels/day-01-slide-2..6.png` | 6 |
| 3 | `posts/day-03.png` | `carousels/day-03-slide-2..3.png` | 3 |
| 5 | `posts/day-05.png` | `carousels/day-05-slide-2..4.png` | 4 |
| 9 | `posts/day-09.png` | `carousels/day-09-slide-2..3.png` | 3 |
| 10 | `posts/day-10.png` | `carousels/day-10-slide-2..7.png` | 7 |
| 14 | `posts/day-14.png` | `carousels/day-14-slide-2..7.png` | 7 |

**Upload order:** select the title card FIRST, then the body slides in numeric order. Instagram defaults to the first selected image as the cover. Caption from `docs/04-social-calendar-14-days.html` for that day.

## Single-image days (Days 2, 4, 6, 7, 8, 11, 12, 13)

Use `posts/day-NN.png` as the feed image. Caption from the calendar.

## How to use

### Profile photo
Upload `profile-photo.jpg` when Instagram asks for it during profile setup, or via Edit Profile → Change photo.

### Story Highlights
Highlights are Instagram Stories that you've saved permanently. Setup flow:
1. Post each PNG from `highlights/` as a Story (one at a time, or all in sequence).
2. After each one posts, tap the Story → tap "Highlight" at the bottom → "+ New" → name it ("About", "Animals", etc.) → done.
3. The PNG you posted becomes both the cover AND the first slide of that highlight. You can later add more Stories to the same highlight (session photos, behind-the-scenes, real client moments).

### Feed posts
The 14 PNGs in `posts/` pair with the captions in `docs/04-social-calendar-14-days.html`. Each PNG is the day's "thesis quote graphic". For the days the calendar specifies a carousel (Days 1, 3, 5, 9, 10, 14), this graphic is the title slide; build the remaining slides in Canva using the same colour and font tokens (lavender bg, Cardo serif, JetBrains Mono labels, gold-deep accents).

For days the calendar specifies a single image + caption (Days 2, 6, 8, 12, 13), the quote graphic serves as a fallback when Ruchita doesn't have a real photo available.

## Regenerating

If she wants to edit the wording on any quote graphic:
1. Open the corresponding `templates/post-day-NN.html` file
2. Edit the thesis line and subline
3. Start the HTTP server: `cd templates && python3 -m http.server 8765`
4. Re-screenshot using any browser at 1080×1350 viewport, or rerun the original Playwright sequence

## Brand tokens (for future Canva templates)

| Token | Value |
|---|---|
| Background | `#E5DCEC` (lavender) with subtle gradient to `#DCC9E8` |
| Primary text | `#3D2E54` (ink) |
| Soft text | `#6E5E83` (ink-soft) |
| Accent | `#9D7B2C` (gold-deep) |
| Body font | Cardo (Google Fonts) |
| Display script | Allura (Google Fonts, for the wordmark only) |
| Label font | JetBrains Mono Medium (Google Fonts) |
| Cream tint | `#F4ECDC` |
