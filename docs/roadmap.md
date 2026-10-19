# Roadmap: from the videos to the end game

Written 2026-10-19, after reviewing four repos the host shared (OpenUI, awesome-design-patterns,
freellmapi, repowise) and running one of them (repowise) on throwaway copies of `_RDA` and
`johnnyautoseed`. This is a proposal, not a decision: nothing here goes in `decisions.md` until the host
says so. Every time is an estimate. The end game is the host's to name; this plan reads it between the
lines and is built so that phases 0 and 1 pay off even if that reading is wrong.

## The reading of the end game (assumed)

The videos are a comforting role play in the host's own voice. The end game, as read: the same company,
two-way. A person can sit with the host's voice, be listened to, and see a calm screen (a breath, a check-in,
a few wishes) from a phone, any time. It could also be the capstone project of the Johnny Autoseed training
("a local full-stack AI application"), built in the open. If the real end game is different, phases 0 and 1
stand and phases 2 to 4 change.

## The parts

| Part | Role | Where it lives |
|---|---|---|
| Relaxation Station videos | the voice, the shape (the Pour, the Turns), the audience | this repo, The Coffee Jesus channel |
| `_RDA` pipeline | cut, loudness, thumbnails, upload | `_RDA/tools` and its skills |
| repowise | the map: keeps docs honest, helps the coding agent build | the dev machine only (AGPL) |
| freellmapi | fuel for prototypes: free-tier models behind one local address | the host's machine, personal use only |
| OpenUI | the face: the model describes a calm screen, the app draws it | the app repo, not created yet |
| awesome-design-patterns | background reading | nowhere in the pipeline |

## Phase 0: ship three episodes (now to about three weeks)

Goal: prove the comforting role play has an audience before writing any app code, and bank the voice
reference. Cost: nothing.

1. Record 001 from the cue card. Trim the head and tail, set loudness with `_RDA/tools/master_audio.py`,
   make the thumbnail from a still, upload to the playlist.
2. Record 002 (The Listen, after work) and 003 (The Wishes, morning): one episode per Turn.
3. A week after each upload, write views, average view duration, returning viewers and what the comments
   say into that episode's `checklist.md`, with the date read.

Gate: three published episodes, each with a thumbnail, and the numbers written down. If watch time is poor,
fix the format first. The app would inherit the problem.

The host does: record, upload. Claude does: packaging, thumbnails from stills, checklists, history.

## Phase 1: tidy the maps (one afternoon)

Goal: the documents the coding agent reads first are true. Cost: nothing.

1. On a throwaway clone, run `repowise init --yes --no-prose --no-editor-setup --no-hook` on
   `johnnyautoseed` and `_RDA`, then `repowise doc-drift`. The trial on 2026-10-19 took 85 and 22 seconds.
2. Fix the stale rows the trial found: 28 in `CODEBASE_MAP.md`, 1 in the Johnny Autoseed `CLAUDE.md`,
   1 in the `_RDA` `CLAUDE.md` (`docs/ideas.md`), 3 in `brand.md`. Strike them through the way the page map
   already marks retired entries.
3. Decide whether to keep the tool. If yes: add `.repowise/` to each `.gitignore` (the index is 11 MB and
   rebuilds in seconds) and one line to each `CLAUDE.md`: run `repowise doc-drift` at the end of a session.
   Never install its global Claude Code hooks, and never ship it inside a product (AGPL).

Gate: a clean doc-drift run on both repos.

## Phase 2: a prototype companion (two or three weekends)

Goal: a ten-minute session with the host's voice and a calm screen, on the host's own machine, that feels
like the videos. Cost: free-tier models, or a few dollars on one paid key.

1. Map first. Run repowise on a clone of OpenUI so Claude Code can answer "how do I define a component
   library" without reading its 3,859 files.
2. Fuel. Get free keys from two or three providers, run freellmapi locally, point the prototype at
   `http://localhost:3001/v1`. Prototype only; never public traffic.
3. Scaffold: `npx @openuidev/cli@latest create --name relaxation-station-app`.
4. Five calm components and nothing else, so the model cannot draw anything off-brand: Breath (a timer),
   CheckIn (three gentle questions), Wishes, Cup (a sip), Meeting (the pretend agenda). Warm Coffee palette.
5. The voice: a system prompt built from `docs/origin.md` and the Pour in `docs/format.md`. The Turns
   become modes.
6. Rails from day one: "company, not care" inside the app; a deterministic crisis path (a word list routes
   to 988 and local numbers, never left to the model); no health claims (in the prompt and checked on the
   way out); nothing a person says is stored unless they ask for it.

Gate: the host runs a full session alone and says it sounds like them. Then three friends.

## Phase 3: let the two feed each other (ongoing)

- Each new Turn is written once and used twice: a video and an app mode.
- Episode comments say what people needed. That becomes the next mode.
- Optional: build the app in the open, as Johnny Autoseed training material or an RDA-style challenge. The
  host's call, since it is a different kind of video from the calm ones.

## Phase 4: ship (when phase 2 earns it)

1. Swap the fuel for a paid model with commercial terms and a data policy. freellmapi stays on the dev machine.
2. A repair step for broken screens. OpenUI's own production numbers: about 7 percent of first passes fail
   validation, and nine in ten of those are repairable.
3. Hosting on Cloudflare, the deploy path the host already runs for two sites.
4. A privacy policy and terms with a legal read, and the care line in the app and in the store listing.
5. A launch video, with a thumbnail. Every video gets a thumbnail.

## What not to do

- Public traffic on freellmapi. Its own docs say single user, personal.
- Any "treats anxiety" or "helps you sleep" language, anywhere.
- Memory of what people share, by default.
- repowise inside the product (AGPL).
- A persona other than the host.

## Open questions for the host

1. Is the reading of the end game right?
2. Does the app carry the host's recorded voice (clips from the episodes) or a synthetic one? A cloned voice
   is its own decision, with its own rights questions.
3. Build in the open, or quietly until it works?
