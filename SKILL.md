---
name: pubz-style
description: >-
  Edit gaming videos in a hyper-edited, meme-dense Pubz-inspired style. Use for
  fast-paced gameplay comedy with hard cuts, punch-ins, bold captions, timed
  sound effects, meme overlays, running bits, and overstimulating retention edits.
license: MIT
metadata:
  author: kaczzabp
  version: 1.0.0
---

# Pubz-Style Gaming Edit

This skill turns raw gameplay into a coherent, joke-dense video in the spirit of
Pubz (@thepubz). It is **style-inspired, not a clone**. Keep the creator's own
voice and use original or licensed assets.

The style is not random effects. It is a gameplay story told through rapid hard
cuts, loud reactions, bold captions, timed meme overlays, and running bits.

## Use this skill when

- The user asks for a "Pubz style", "overstimulating", "brainrot", "editor was
  laced/fried/mentally unstable", or hyper-edited gaming video.
- Raw gameplay, facecam, and Discord audio need a comedy/retention edit.
- A long VOD needs to become a 6-15 minute highlight video.
- An existing cut needs a punch-in, caption, meme, and sound-design pass.

## Read first

- `references/style-guide.md` — full visual, audio, caption, and comedy rules.
- `references/research-notes.md` — what was observed in Pubz videos, with data.
- `references/premiere-workflow.md` — Premiere Pro and MCP workflow.
- `references/reference-analysis-template.md` — how to analyze new reference clips.
- `examples/edit-brief.md` — a ready-to-adapt brief.

## Non-negotiables

1. **Story first.** Every 30-60 seconds needs a setup, escalation, and payoff.
   Effects support the joke; they do not replace it.
2. **Hard cuts by default.** No default crossfades, soft wipes, or template
   transitions. Cut on action, mid-word, or on the beat.
3. **Captions on every spoken joke.** Short, bold, high-contrast, synced.
4. **Memes and SFX only when they land a joke.** Never wallpaper the timeline.
5. **Keep the game and voices intelligible.** If the viewer cannot follow the
   play or the punchline, the edit failed.
6. **Stop before destructive actions.** Show a beat sheet or change log before
   deleting clips, overwriting a project, or exporting.
7. **Keep it platform-safe.** Match the energy, not the edginess. No slurs,
   hate, targeted harassment, or sexual content involving minors.
8. **Use licensed or original assets.** Memes, music, and sound effects may be
   copyrighted; the user is responsible for clearing them.

## Density budget

Pubz-style editing is dense but not constant. Use this as a default:

| Layer | Working target | Hard limit |
|---|---|---|
| Visual change in action | every 1-2 seconds | do not exceed 1 change per 0.5s |
| Hold for a joke | 2-4 seconds | do not cut away from a punchline |
| Meme overlay | 1 per 20-30 seconds | 3 per minute at peak |
| Sound effect | 1 per 5-10 seconds | never stack more than 2 |
| Caption | 2-6 words per card | never a full paragraph |
| Simultaneous effects | 1-2 | never more than 3 |

If a section feels exhausting, remove effects before removing story.

## Workflow

### 0. Prep

- Duplicate the project or sequence. Never edit the only copy.
- Sync gameplay, facecam, and Discord audio. Label tracks clearly.
- Put gameplay on V1, facecam on V2, overlays on V3+, dialogue on A1/A2,
  game audio on A3, music on A4.
- Confirm frame rate, resolution, and audio sample rate before cutting.
- Ask for the target length, platform, and whether profanity should be bleeped.

### 1. Beat sheet (approval gate)

- Transcribe the recording or scan the audio for reactions, arguments, jokes,
  roleplay, and unexpected events.
- Pick 5-9 candidate bits. For each, write: in/out time, setup, escalation,
  punchline, callback potential, visual idea, audio idea.
- Build a cold open from the strongest 5-10 seconds, then a short context beat.
- Show the beat sheet to the user before cutting.

### 2. Rough cut

- Remove dead air, travel, inventory management, and repeated failed attempts
  that do not escalate.
- Keep the setup for every payoff. A punchline without setup is noise.
- Cut mid-word or mid-sentence when it creates energy, but keep the joke legible.
- Use J-cuts and L-cuts to overlap reactions and dialogue.
- Target 6-12 minutes for a 30-60 minute recording unless told otherwise.
- End on a callback or an abrupt button, not a long outro.

### 3. Punch-in pass

- Punch in 105-125% on reactions, kills, and important lines.
- Anchor the zoom on the face or action, not the center of the frame.
- Add a 1-2 frame position/scale shake on impacts. Do not shake every cut.
- Use split-screen or picture-in-picture for big reactions and simultaneous
  gameplay/facecam moments.
- Add speed ramps only when they serve a joke or impact.

### 4. Meme overlay pass

- Add an overlay only when the line needs a visual punchline.
- Time the overlay to the word that triggers it, not the start of the clip.
- Keep overlays inside the safe area; never cover the kill feed, ammo, or the
  player's crosshair.
- Remove the overlay before it overstays. A meme that lingers stops being funny.
- Prefer original art, licensed assets, or the user's own meme library.

### 5. Caption pass

- Caption every spoken line that matters to the joke or story.
- Use 2-6 words per card; break at natural phrase boundaries.
- Default style: bold white text, heavy black stroke, bottom center, slight
  shadow. Highlight the keyword in one accent color.
- Use all caps for screams and impact lines; use mixed case for deadpan lines.
- Do not caption every breath or use a full transcript wall.
- Check sync after every cut; captions drift when the timeline changes.

### 6. SFX and audio pass

- Layer sound effects under the reaction, not over the dialogue.
- Use whooshes for fast moves, impacts for hits, record scratches for bad beats,
  and silence before a punchline.
- Duck music under dialogue and game callouts.
- Keep game audio audible; it sells the play.
- Use a limiter on the master. Do not clip the screams.
- Cut music to silence for one beat before the biggest joke when it helps.

### 7. QA and export

- Watch once without pausing. If you reach for the timeline, fix the problem.
- Check the first 5 seconds: is there a reason to keep watching?
- Check every caption against the audio.
- Check for dead air, repeated jokes, overused memes, and audio peaks.
- Confirm export settings and output path with the user before rendering.
- Export a review file first, then the final master after approval.

## What good looks like

- A cold open that lands before the viewer knows what the video is.
- A clear gameplay goal, even when the bits escalate into nonsense.
- Running bits that return with escalation, not repetition.
- Captions that make quiet lines funny and loud lines legible.
- Memes that feel like a response to the moment, not a sticker on top.
- Audio that is loud when it matters and silent when the joke needs air.
- An ending that pays off a setup from earlier in the video.

## What to avoid

- Random meme spam with no connection to the line.
- Constant screen shake that makes gameplay unreadable.
- Captions that cover the crosshair or the kill feed.
- Cutting away from a punchline before it lands.
- Reusing the same sound effect every 10 seconds.
- Explaining the joke in a caption.
- Copying Pubz's actual jokes, thumbnails, or assets.
- Edgy content that targets a real person or group.

## Tool use

- Use the NLE/MCP tools that are actually available. Start read-only:
  project info, sequence list, project items, active sequence.
- Never invent a tool name. If the available MCP server lacks an operation, say
  so and fall back to manual instructions.
- Duplicate the sequence before editing. Keep the original untouched.
- For Premiere Pro, read `references/premiere-workflow.md`.
- For DaVinci Resolve, the same workflow applies; use the available Resolve MCP
  tools for timeline, color, Fusion, and render operations.

## Output format

When planning, return a beat sheet:

| # | In | Out | Setup | Escalation | Punchline | Visual | Audio | Callback |
|---|---|---|---|---|---|---|---|---|

When editing, return a change log:

| Time | Change | Tool | Why |
|---|---|---|---|

When reviewing, return:

1. What works
2. What is slow or confusing
3. What is overdone
4. The three highest-impact fixes
