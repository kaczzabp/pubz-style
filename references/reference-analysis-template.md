# Reference Analysis Template

Use this when you want to extend the skill with a new creator, a new video, or a
new style variant. Analyze at least three clips before changing the style guide.

## 1. Collect

For each reference:

- URL or local file
- Creator
- Upload date
- Duration
- Game/genre
- Target platform
- One-sentence description of the style

## 2. Measure the pace

Use a short sample: the first 90-120 seconds, plus one mid-video action section.

With FFmpeg:

```bash
ffmpeg -i sample.mp4 -vf "select='gt(scene,0.3)',showinfo" -f null - 2>&1 \
  | grep "pts_time" > scene-changes.txt
```

Count the lines and compute the intervals. Record:

| Metric | Value |
|---|---|
| Sample duration | |
| Scene changes at 0.2 | |
| Scene changes at 0.3 | |
| Scene changes at 0.4 | |
| Average interval | |
| Median interval | |
| Longest hold | |

Remember: scene detection counts punch-ins and overlays too, not only cuts.

## 3. Shot and caption audit

Watch the sample and fill this in:

| Timestamp | Shot / cut | Caption text | Caption style | Overlay / meme | SFX / music | Why it works |
|---|---|---|---|---|---|---|
| 0:00 | | | | | | |
| 0:05 | | | | | | |
| 0:10 | | | | | | |

Questions:

- How often is the caption on screen?
- Is the caption a full sentence or 2-6 words?
- Where is it placed? Does it move?
- What font weight, stroke, color, and highlight?
- Does it match Bagel Fat One? Compare `a`, `y`, `t`, and `e` before naming a
  different font.
- Are captions on every line, only jokes, or only loud lines?
- Does the caption ever cover gameplay UI?

## 4. Meme and SFX audit

| Timestamp | Meme / SFX | Trigger word or action | Duration | Does it land? |
|---|---|---|---|---|
| | | | | |

Count per minute:

- Meme overlays
- Sound effects
- Music drops
- Moments of silence
- Split-screen or PiP
- Punch-ins
- Shakes

## 5. Structure audit

List the beats:

| # | In | Out | Setup | Escalation | Punchline | Callback |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |

Look for:

- Cold open: what is the first line or image?
- Context: how quickly does the viewer know the goal?
- Running bits: what returns, and how does it escalate?
- Ending: callback, abrupt button, or generic outro?

## 6. Extract rules

Turn observations into rules only when they appear at least three times:

| Observation | Rule | Confidence |
|---|---|---|
| Cuts every ~0.8s in action | Use 1-2s visual changes in action | High |
| Captions are 2-4 words | Cap captions at 6 words | High |
| Meme every ~15s | Target 1 meme per 20-30s | Medium |
| Music cuts to silence before punchlines | Use silence before the biggest joke | Medium |

## 7. Update the skill

- Add confirmed rules to `references/style-guide.md`.
- Add evidence and caveats to `references/research-notes.md`.
- Do not add a rule from a single clip.
- Keep the creator's own voice and assets separate from the reference.

## 8. Test

Apply the updated skill to a 60-second test cut. Ask:

1. Does the cold open work without context?
2. Is the story legible with the sound off?
3. Are the captions readable at normal speed?
4. Is there a laugh or a payoff at least every 20-30 seconds?
5. Does it feel dense without feeling random?

If the answer to 5 is no, remove effects before adding more.
