# Production: record anywhere

An episode should be possible in the morning, the afternoon or the evening, at home or on the road, with
what fits in a bag.

## The kit

- A phone (or any camera) and something stable to lean it on. 1080p is plenty.
- A hot drink: coffee, and a second cup of tea in frame if you like.
- Soft light from a window, to one side of the face. No harsh overhead light.
- Optional, and the best upgrade: a clip-on or wired mic close to the mouth. A calm video lives or dies on
  its audio.
- One index card with the beats (the run sheet), placed right beside the lens.

## Two-minute setup

1. Lens at eye level and close enough that the eyes read. Look at the lens, not at yourself on the screen.
   Optional trick: tape a small photo of a friend's face next to the lens and talk to them.
2. Window to one side, or turn 45 degrees toward it. Nothing bright behind you.
3. Quiet the room: fans, AC, the fridge, notifications. Phone on do-not-disturb.
4. Soft things around you help (curtains, a bed, a couch). Bare hard rooms echo. A hotel room with the
   curtains closed works well.
5. Frame the head and shoulders plus the cup, with a little air above the head.
6. Record ten seconds, play it back on headphones, and check the voice and the eyes. Then go.

## Recording

- One take, top to bottom. Do not stop for a flub. Laugh, sip, keep going. The sips and the laughs are part
  of the show.
- Begin with a breath of silence on the lens before "Hello." Stay on the lens for a breath after the last word.
- If you blank, sip.

## Finish

1. **Trim the head and the tail.** That is all. No jump cuts, no music, unless you decide otherwise.
2. **Loudness:** `python /path/to/_RDA/tools/master_audio.py episode.mp4` brings it to -16 LUFS integrated
   and -1.5 dBTP and copies the video untouched (needs ffmpeg). Learned in RDA: YouTube turns loud videos
   down and never turns quiet ones up, so a quiet export stays quiet.
3. **Listen** to the first minute on headphones at low volume. No hiss, no harsh S sounds, no loud start.
4. **Chapters** (optional): only from real timestamps in the finished file.
5. **Thumbnail.** Required. See `packaging.md`.

## Upload

Title, description, thumbnail, playlist "Relaxation Station" (create it with the first upload), audience set
to not made for kids. The YouTube Studio phone app is enough for all of it.
