# Decisions

One entry per decision worth remembering: what was decided, where it came from, why, and what would make
us revisit it. Newest first. Reversed decisions stay, marked as such, because the reason they were reversed
is information too. The narrative is in `docs/history/`.

Source tags: **user** means the host said it (`docs/origin.md` or a later message). **assumed** means the
session chose a first guess so work could keep moving. Assumed decisions are the host's to flip.

---

### D10 · Visual work is judged by looking at it (2026-10-19)

**Decided:** anything people watch (a scene, a thumbnail, an overlay) is checked by rendering it at the
viewer's screen size and reading the image, not only by tests that the controls work.
**Source:** user ("idk what control tests you're running to make it "good" but they're not working"); the
method is assumed.
**Why:** the jungle river passed 20 of 20 control checks while the water was banded, the trees looked like
rocks and the river ended at a bare horizon.
**Revisit:** never as a rule; the method can change.

### D9 · A care line in every description (2026-10-18)

**Decided:** descriptions end with: this is company, not care; reach out to someone you trust; in crisis,
call or text 988 in the US or your local emergency number.
**Source:** assumed.
**Why:** the audience is people decompressing, and some will be struggling. The show offers company, not
treatment, and the description is the quiet place to say so.
**Revisit:** the host's call to keep, reword or drop it.

### D8 · No tools yet (2026-10-18)

**Decided:** the repo is documents and templates only. No scripts.
**Source:** assumed, from "keep it simple, silly."
**Why:** an episode is one take and a few files. A tool would be upkeep without a payoff yet. The one useful
tool, loudness mastering, already exists in `_RDA/tools/master_audio.py`.
**Revisit when:** there are three episodes. Then a small `tools/station.py` (new, status, with the thumbnail
check) will pay for itself, as `rda.py` does in RDA.

### D7 · Every video ships with a thumbnail, in a quiet warm look (2026-10-18)

**Decided:** the RDA rule applies here: an episode is not done without `packaging/thumb-A.jpg`, checked at
320 px wide. The series look is warm and calm (Coffee Jesus palette, a real still with eye contact, one
short hook), not RDA's loud dark look.
**Source:** the rule is **user** (2026-10-05). The look is assumed.
**Why:** a thumbnail decides whether a video gets watched. Calm content should look calm in a feed, and the
eye contact is the product.
**Revisit:** with click-through data from the first few episodes. The look is v0.1 and untested.

### D6 · About ten minutes (2026-10-18)

**Decided:** the default episode is about ten minutes.
**Source:** assumed. The host named no length.
**Why:** long enough to settle through the Pour, short enough to record in one take and watch on a break.
**Revisit:** after three episodes, using average view duration and retention from YouTube Studio.

### D5 · Beats, not a script (2026-10-18)

**Decided:** each episode has a run sheet: ten beats, the host's anchor lines where they exist, and
direction. The host ad-libs inside the shape.
**Source:** user ("I'm just ad-libbing"). The ten-beat shape is assumed, drawn from the sample monologue.
**Why:** a full script would cost the eye contact and the easy tone. Beats keep the shape and the freedom.
**Revisit:** if ad-libbing gets repetitive, add more seeds, not more script.

### D4 · One take, no music, by default (2026-10-18)

**Decided:** record top to bottom, trim only the head and the tail, no jump cuts, no music.
**Source:** assumed, from "super simple."
**Why:** presence is the product, and jump cuts break it. One take is also what makes recording on the road
possible.
**Revisit:** after the first episode is heard back. A very quiet bed might help, or might fight the voice.

### D3 · Empathy, not ASMR (2026-10-18)

**Decided:** the show offers empathy and company, and nothing else. It is not ASMR: a normal soft voice, no
whispering, no triggers. No advice, no selling, no health claims.
**Source:** user ("offering someone empathy, no more, no less," "not going to be ASMR"). The ban on health
claims is assumed.
**Why:** it keeps the show honest and the host's job easy.
**Revisit:** not the empathy. The edges can move.

### D2 · Same host, same channel; "Relaxation Station" is the series name (2026-10-18)

**Decided:** episodes go on The Coffee Jesus channel with the host's own face and voice. "Relaxation Station"
is a playlist and series name, not a new channel or persona.
**Source:** user ("I don't have to invent a new persona"). Using the repo's name as the series name is assumed.
**Why:** no new identity to build, and the existing audience can find it.
**Revisit:** if the end game wants its own home.

### D1 · This repo is the home base (2026-10-18)

**Decided:** `relaxation_station` holds the format, the episodes, the packaging rules, and the record.
**Source:** assumed, following RDA's D12.
**Why:** the repo was empty and named for the project, and one home beats scattered notes.
**Revisit:** never as a whole.
