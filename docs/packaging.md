# Packaging: titles, descriptions, thumbnails

## Titles

Plain words, second person: the moment plus a gentle offer. A title is an invitation, not a promise of a result.

- Use the moment ("morning," "after work," "tonight") and a verb of company ("sit with me," "recenter with me").
- Do not promise outcomes ("cure your anxiety," "fall asleep fast"), use ALL CAPS, or bait.
- Stay under about 60 characters so phones do not cut it off.

## Description template

    One plain sentence about what this is.
    One or two lines about the moment. "Made for the start of your day."

    Chapters (real timestamps from the finished file only)
    0:00 Hello
    ...

    Part of Relaxation Station, calm and simple videos from The Coffee Jesus.

    This is company, not care. If you are having a hard time, please reach out to someone you trust.
    If you are in crisis, call or text 988 in the US, or your local emergency number.

The last paragraph is the care line (D9, assumed). It is the host's call to keep, reword or drop.

## Thumbnails

**Every video ships with a thumbnail.** No exceptions. A video is not finished until its thumbnail exists,
has been checked at 320 px wide, and is saved at `episodes/NNN-slug/packaging/thumb-A.jpg`. (User rule,
2026-10-05.)

The series look, v0.1, untested. It is deliberately quieter than the RDA thumbnails: calm should look calm
in a feed.

1. **A real still from the video.** Eyes on the lens, a soft smile, the cup in frame. The eye contact is
   the product, so the face is the hero.
2. **One hook, one to three words, that does not repeat the title.** For example "Sit with me," "Hi, friend,"
   "Breathe." Set in Fraunces 700. Keep the font as a local file; do not fetch fonts at render time.
3. **Warm Coffee palette** from `thecoffeejesus/DESIGN.md`: cream ground, chocolate type, burnt orange or
   gold as the single accent. Soft window light, not a harsh glow.
4. **Same layout every time** so the series is recognizable in a feed: face right of center, hook on the left,
   cup low in the frame. Keep the bottom-right corner clear for YouTube's timestamp.
5. **Honest.** Show only what the video delivers: real eye contact, a real cup. No fake steam, no health
   badges, no "calm in 10 minutes."
6. **Check at 320 px wide** before shipping. If the hook or the eyes do not read there, it is not done.
7. Save as `thumb-A.jpg`, 1280 by 720, small enough to upload anywhere (under 2 MB). Extra bets are
   `thumb-B.jpg` and `thumb-C.jpg` for YouTube's thumbnail test.

Tools: the `/thumbnail` and `/packaging` skills in the _RDA repo can render these (point them at
`episodes/NNN-slug/packaging/`). A still from the video plus a text overlay is enough.

### Measured contrast

WCAG ratios computed from the hex values in `thecoffeejesus/DESIGN.md` on 2026-10-18. 4.5 is the text
minimum and 3 is the minimum for large text, which a thumbnail hook is.

| Pair | Ratio | Use |
|---|---|---|
| chocolate `#4a2c2a` on cream `#f5f0e6` | 11.0 | the default hook |
| cream on chocolate | 11.0 | the hook on a dark ground |
| gold `#fbbf24` on chocolate | 7.5 | an accent word |
| burnt orange `#e07b3c` on chocolate | 4.2 | large text only |
| cream on burnt orange | 2.6 | never use for text |
