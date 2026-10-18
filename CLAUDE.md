# CLAUDE.md, relaxation_station

Home base for **Relaxation Station**: calm, simple videos on The Coffee Jesus channel, where the host
looks at the camera and keeps the viewer company in a slow, kind voice. Empathy, no more and no less. No
new persona, no big production. Keep it simple, silly.

**New session? Read this file, then `docs/format.md`, then the latest entry in `docs/history/`, then skim
the `checklist.md` in each folder under `episodes/`.** That is enough to pick up where the last session stopped.

## How we work

- Ideas arrive at random and out of order. When the user shares one, park it first: add a line to
  `docs/ideas.md` in the form `- YYYY-MM-DD  the idea`. Then talk about it.
- When something happens off camera (recorded, trimmed, uploaded, a number read from YouTube Studio), tick
  or note it in that episode's `checklist.md`, so the record matches reality.
- At the end of a working session, add or extend an entry in `docs/history/` (what we did, why, what we
  found, what we got wrong) and add anything worth remembering to `docs/decisions.md`.
- The user does not want PRs watched. Never subscribe to PR activity or schedule PR check-ins unless they
  ask. If the harness auto-subscribes, unsubscribe.
- No em dashes or en dashes anywhere: docs, scripts, on-screen text, commit messages. User preference.
  Use a period, a colon or a comma.
- **Every video gets a thumbnail.** An episode is not done until `packaging/thumb-A.jpg` exists, follows
  `docs/packaging.md`, and has been checked at 320 px wide. User rule, set on 2026-10-05 in the RDA repo.
- Keep it simple. Before adding a document, a tool or a step, ask whether the host would miss it.

## Hard rules, the series

Rules marked **user** are the host's own words (see `docs/origin.md`). Rules marked **assumed** are the
session's first guess and the host's to change. `docs/decisions.md` has the reasoning.

- **Empathy, not advice.** The video offers company and a gentle pace. It does not diagnose, treat, coach,
  fix, sell or lecture. (user)
- **Not ASMR.** A normal soft speaking voice. No whispering, tapping or triggers. (user)
- **Same host, same channel.** No new persona and no new channel. "Relaxation Station" is a playlist and a
  series name. (user; the name is assumed)
- **Slow, eye contact, kind.** The host looks at the lens and takes their time. (user)
- **One take by default.** Invisible edits only: trim the head and the tail. No jump cuts, no music, unless
  the host asks. (assumed)
- **No health claims.** Never say a video will treat or reduce anxiety, insomnia or anything else. The
  promise is "sit with me." (assumed)
- **Care line.** Descriptions say this is company, not care, and point to emergency help. (assumed)
- **Honest packaging.** The title and thumbnail promise only what the video delivers. (assumed)
- **Nothing estimated is written as measured.** Lengths, timestamps and viewer numbers come from the file
  or from YouTube Studio. A run sheet's times are a plan and say so.

## Layout

```
README.md                    the front door
CLAUDE.md                    this file
docs/format.md               the promise, the shape of an episode (the Pour), the Turn, delivery
docs/production.md           record anywhere, finish, upload
docs/packaging.md            titles, descriptions, thumbnails
docs/origin.md               the idea in the host's words, verbatim
docs/ideas.md                inbox and open questions
docs/decisions.md            numbered decisions
docs/history/                one entry per session
episodes/_template/          run-sheet.md, packaging.md, checklist.md
episodes/NNN-slug/           one folder per episode, same three files
episodes/NNN-slug/packaging/ thumb-A.jpg (and B, C if you test)
```

Raw footage, renders and audio work files are never committed (`.gitignore` covers them). Thumbnails are.

## Related repos

- `_RDA`: the challenge series. Source of the thumbnail rule, `tools/master_audio.py` (loudness to -16 LUFS,
  needs ffmpeg), and the `/packaging` and `/thumbnail` skills. Those skills expect `videos/<project>/packaging/`;
  here the folder is `episodes/NNN-slug/packaging/`.
- `thecoffeejesus`: the site and brand. `DESIGN.md` holds the Warm Coffee palette and the Fraunces and Nunito type.
