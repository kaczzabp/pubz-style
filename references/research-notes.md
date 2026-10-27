# Research Notes

Research date: 2026-10-27

Subject: Pubz (@thepubz), a gaming YouTuber whose recent videos use
hyper-edited, meme-dense, "overstimulating" comedy.

This file records what was observed, how it was measured, and what is still an
assumption. It is not an official statement from Pubz and does not claim to know
his exact software or workflow.

## Sources

Primary channel:

- https://www.youtube.com/@thepubz
- https://www.youtube.com/@thepubz/videos

Representative videos:

- "Skybasing but the editor was LACED" — https://www.youtube.com/watch?v=z196C-q4MQs
- "Fortnite but it's OVERSTIMULATING" — https://www.youtube.com/watch?v=YGEt_5sQnrA
- "Minecraft Bedwars **POST LOBOTOMY**" — https://www.youtube.com/watch?v=W2RZ4exoDTs
- "Counter Strike but the editor was FRIED" — https://www.youtube.com/watch?v=7FPl6hdzvaw
- "GTA Races but the editor is mentally unstable" — https://www.youtube.com/watch?v=8QexTdcver4
- "GTA Sumo but it's just brainrot" — https://www.youtube.com/watch?v=N8rRLkR2KLg
- "Fortnite Brainrot **UNSOBER EDITION**" — https://www.youtube.com/watch?v=-QTQmIiY36k
- "10 minutes of perfectly cut clips" — https://www.youtube.com/watch?v=LYebjNu2_4Q

## Channel snapshot

From the public videos page and metadata on 2026-10-27:

- About 113K subscribers.
- About 130 videos on the channel.
- The 34 most recent videos on the videos tab range from roughly 6 to 22
  minutes, excluding the "BEST OF" compilations, which run 46-62 minutes.
- Recent titles lean heavily on self-aware editor jokes: "editor was LACED",
  "editor was FRIED", "editor is mentally unstable", "POST LOBOTOMY",
  "OVERSTIMULATING", "brainrot", "UNSOBER EDITION".

Representative recent uploads:

| Title | Duration | Views* |
|---|---:|---:|
| MLB took over my channel and DELETED IT | 12:51 | 99K |
| don't drink and do minecraft challenges... | 19:05 | 251K |
| GTA Races but the editor is mentally unstable | 12:55 | 225K |
| 10 minutes of perfectly cut clips | 10:25 | 105K |
| Bedwars but we smoked too much... | 15:05 | 229K |
| Counter Strike but the editor was FRIED | 16:47 | 389K |
| Fortnite but it's OVERSTIMULATING | 22:23 | 425K |
| Minecraft Bedwars **POST LOBOTOMY** | 7:19 | 624K |
| Skybasing but the editor was LACED | 18:46 | 1.5M |
| GTA Sumo but it's just brainrot | 9:35 | 202K |

\*Views are a snapshot and will change.

## Method

Two 90-120 second samples were downloaded at 360p for analysis:

1. "Fortnite but it's OVERSTIMULATING" — first 90 seconds.
2. "Skybasing but the editor was LACED" — first 120 seconds.

FFmpeg scene detection (`select='gt(scene,THRESHOLD)'`) was used to count large
visual changes at thresholds 0.2, 0.3, and 0.4. A contact sheet was generated
every five seconds to inspect captions, overlays, framing, and game UI.

This measures **visual change**, not only editorial cuts. A punch-in, meme
overlay, or flash also registers as a scene change. The numbers are therefore an
upper bound on cut rate and a useful measure of visual density.

## Scene-change results

| Sample | Threshold | Changes | Average interval | Median interval |
|---|---:|---:|---:|---:|
| Fortnite (90s) | 0.2 | 132 | 0.66s | 0.40s |
| Fortnite (90s) | 0.3 | 92 | 0.95s | 0.53s |
| Fortnite (90s) | 0.4 | 53 | 1.65s | 0.73s |
| Skybasing (120s) | 0.2 | 99 | 1.20s | 0.90s |
| Skybasing (120s) | 0.3 | 59 | 2.03s | 1.30s |
| Skybasing (120s) | 0.4 | 35 | 3.46s | 2.20s |

Interpretation:

- The Fortnite sample is denser than the Skybasing sample, but both are far
  faster than a standard gameplay video.
- At a conservative 0.3 threshold, the median visual change is about one every
  half-second to 1.3 seconds.
- The style is not a constant stream of cuts; there are holds of 3-9 seconds for
  jokes, tension, or gameplay. The density is uneven on purpose.

## Visual observations

From the contact sheets:

- A black disclaimer card opens at least one video. The word "JOKES" is
  highlighted in red, followed by a warning that some viewers may find the
  content offensive.
- Captions are large, bold, white, and heavily outlined. Examples: "funny?",
  "you ready?", "see it now!", "are you serious?", "BUILD!", "alright i'll-",
  "one day shipping".
- Captions sit at bottom center or near the speaker, and often use a comic-style
  font with a black stroke.
- Meme overlays include cartoon faces, distorted characters, and reaction images
  composited over gameplay.
- The game UI remains visible. The edit does not hide the fact that it is a game.
- Framing is aggressive: tight crops, sniper scopes, crash zooms, and low angles.
- Color is saturated and high-contrast, but the game's original look is still
  recognizable.

## Transcript observations

From the auto-generated transcript of "Fortnite but it's OVERSTIMULATING":

- Dialogue is overlapping, loud, and frequently interrupted by laughter and
  screaming.
- The video explicitly jokes about its own editing:
  - "Use me as a transition or something."
  - "That was like so Sigma. Like that was like a Sigma edit, like inspirational
    quote and then the good thing happens and then bass drop."
- Roleplay bits appear without explanation and are played straight:
  - "Glory to Yaku. I must keep Agartha safe."
- Absurd mundane conversations run under the gameplay, e.g. an OLED monitor fact
  during a crude story.
- The comedy depends on commitment and escalation, not just rapid cuts.

## Chapter structure

YouTube chapters on the sampled videos show 6-13 beats, each roughly one to two
minutes:

- "Skybasing but the editor was LACED": High stakes rocket launch / Base defense
  and rescue / Sneaky tactics and jokes / Failed rocket maneuvers / Endgame
  resource scarcity / Chaotic banter and defeat / New match and teammate drama /
  Poor engineering disasters / Rapping about John Pork / Anarchy Acres chaos /
  Final stand attempts / Race to the finish line.
- "Fortnite but it's OVERSTIMULATING": Early match chaotic action / Squad
  conflicts and banter / Tech talk and humor / New round begins / Navigating the
  storm / Final squad push / Landing in lucky landing / Intense firefight /
  Skybase strategy / Skybase collapse and retreat / Endgame showdown / Victory
  and outro.
- "Minecraft Bedwars **POST LOBOTOMY**": Initial bed wars chaos / Securing
  resources / Team coordination and chaos / Mid-game combat strategy / Clutch
  moments and gambling / Post-game stories and antics.

This supports a beat-based structure rather than a traditional three-act story.
Each chapter is a comedic or gameplay unit with its own setup and payoff.

## What is confirmed

- Pubz's recent videos use very fast visual pacing and dense captioning.
- Meme overlays, game UI, loud reactions, and meta-editing jokes are part of the
  style.
- The videos are structured as gameplay/bit chapters, not just highlight reels.
- The channel openly labels the style with words like "overstimulating",
  "brainrot", "laced", "fried", and "post lobotomy".

## What is not confirmed

- Which NLE or plugins Pubz uses. This skill does not assume Premiere or Resolve.
- Exact cut counts. Scene detection is an approximation.
- The full distribution across all 130 videos. Only two short samples were
  measured.
- Whether the style is stable over time. The channel's older videos may use a
  different pace.

## Style-transfer caution

The goal is to reproduce the **pacing, structure, and energy**, not Pubz's
specific jokes, artwork, thumbnails, or copyrighted assets. Use original writing
and licensed assets. Keep the creator's own voice.

The source videos include offensive jokes and disclaimers. This skill should
match the energy without reproducing slurs, hate, targeted harassment, or sexual
content involving minors.
