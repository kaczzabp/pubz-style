# Pubz-Style Style Guide

A practical breakdown of the editing language used by Pubz (@thepubz), translated
into rules an editor or agent can apply. This is a style study, not a claim about
the creator's exact workflow or software.

## Style in one sentence

A coherent gameplay story told through rapid hard cuts, loud reactions, bold
captions, timed meme overlays, and running bits — dense, self-aware, and
intentionally exhausting, but never random.

## Style fingerprint

| Dimension | Default |
|---|---|
| Format | 16:9 YouTube gameplay comedy, usually 6-22 minutes |
| Pacing | Very fast; visual changes roughly every 0.5-2 seconds in action |
| Cuts | Hard cuts, mid-word cuts, match cuts, abrupt scene changes |
| Camera | Punch-ins, crash zooms, shakes, split-screen, picture-in-picture |
| Captions | Bagel Fat One; bold white with black stroke; short phrases; keyword highlight |
| Memes | Frequent but timed; reaction images, cartoons, distorted faces, GIFs |
| SFX | Dense layer of impacts, whooshes, record scratches, meme sounds |
| Music | High-energy tracks, abrupt drops, silence before punchlines |
| Comedy | Self-aware, meta, absurd escalation, roleplay, running bits |
| Structure | Cold open, gameplay goal, escalating bits, callback ending |
| Tone | Loud, crude, playful, intentionally "fried" or "laced" |

## What the research found

From the channel page and recent uploads (October 2026):

- The channel has roughly 113K subscribers and 130 videos.
- Recent titles include "Fortnite but it's OVERSTIMULATING", "Skybasing but the
  editor was LACED", "Minecraft Bedwars **POST LOBOTOMY**", "Counter Strike but
  the editor was FRIED", and "GTA Races but the editor is mentally unstable".
- Video lengths in the recent 34-video page range from about 6 to 22 minutes,
  with the "best of" compilations much longer.
- YouTube chapters divide videos into 6-13 gameplay/bit beats, not traditional
  three-act scenes.

Two short samples were analyzed with FFmpeg scene detection:

| Sample | Duration | Scene changes at 0.3 threshold | Median interval |
|---|---:|---:|---:|
| Fortnite but it's OVERSTIMULATING | 90s | 92 | 0.53s |
| Skybasing but the editor was LACED | 120s | 59 | 1.30s |

At a more sensitive 0.2 threshold, the same samples had 132 changes in 90s
(median 0.40s) and 99 changes in 120s (median 0.90s). Scene detection counts
large visual changes, including cuts, punch-ins, and overlays, not only cuts.
Even so, the pace is clearly much faster than a standard let's-play edit.

Visual observations from extracted frames:

- A black disclaimer card with a highlighted "JOKES" warning opens at least one
  video.
- Gameplay is saturated and high-contrast, with the game UI left visible.
- Captions are large, bold, white, and heavily outlined, often at bottom center:
  "funny?", "you ready?", "see it now!", "are you serious?", "BUILD!".
- The caption face matches **Bagel Fat One** (Google Fonts, SIL OFL 1.1). See
  [Caption system](#caption-system) for evidence, fallbacks, and styling.
- Meme images and cartoon faces are composited over gameplay and characters.
- Sniper scopes, crash zooms, and tight crops are used as punctuation.
- The edit is comfortable cutting in the middle of a line or a movement.

Transcript observations from "Fortnite but it's OVERSTIMULATING":

- Constant overlapping dialogue, screaming, laughter, and interruptions.
- Meta-editing jokes: a player says "use me as a transition or something"; another
  describes a "Sigma edit, like inspirational quote and then the good thing
  happens and then bass drop".
- Roleplay bits appear without setup and are committed to deadpan: "Glory to
  Yaku. I must keep Agartha safe."
- Absurd mundane conversations run underneath action, e.g. an OLED monitor fact
  during a crude story.
- The humor comes from escalation and commitment, not from the game alone.

## Structural template

Use this for a 6-12 minute video:

1. **Cold open (0:00-0:15).** The strongest reaction, fail, or absurd line. No
   logo, no intro, no "what's up guys".
2. **Context (0:15-0:45).** Who is playing, what the goal is, who is in the call.
   Keep it under 30 seconds.
3. **First bit (0:45-2:00).** A clean setup, escalation, and punchline. Establish
   the video's comic rhythm.
4. **Escalation block (2:00-6:00).** 3-5 bits of increasing absurdity. Rotate
   between gameplay tension and call banter.
5. **Running-bit return (6:00-8:00).** Bring back an earlier phrase, character, or
   fail with a new twist.
6. **Peak (8:00-10:00).** The biggest play, argument, or roleplay payoff.
7. **Button (last 10-20 seconds).** Callback, abrupt cut, or deadpan line. Do not
   explain the video or ask for likes for 30 seconds.

For a 20+ minute video, repeat the escalation block with new bits, but keep one
central running joke that returns.

## Visual language

### Cuts

- Hard cut by default. Cut on action, on the beat, or mid-word.
- Use match cuts when two actions line up; use them as a joke, not decoration.
- Cut away from a reaction only after the reaction has landed.
- Use a flash frame or a one-frame black frame sparingly for impact.
- Avoid default crossfades, soft wipes, and "cinematic" template transitions.

### Punch-ins and zooms

- Punch in 105-125% on a reaction, kill, or important line.
- Anchor the zoom on the face or the action. Do not zoom to the center by default.
- Use a fast zoom (3-5 frames) for a punchline, a slower push for tension.
- Add a 1-2 frame shake on impacts: kills, explosions, slams, screams.
- Do not shake the entire video. Shake is punctuation.

### Split-screen and overlays

- Use split-screen for simultaneous facecam/gameplay reactions or two players.
- Use picture-in-picture for a reaction while the gameplay stays readable.
- Keep the game's crosshair, ammo, and kill feed visible.
- Put meme overlays inside the safe area, not over the UI.
- Remove the overlay before it overstays. A meme should hit and get out.

### Color and texture

- Keep the game's look recognizable; add contrast and saturation rather than a
  heavy cinematic grade.
- Use a subtle vignette or glow only if it helps focus.
- Avoid heavy film grain, letterboxing, and "movie trailer" looks unless the bit
  calls for it.
- Use glitch, VHS, or deep-fried effects as a joke, not as the default finish.

## Caption system

### Font

The caption face matches **[Bagel Fat One](https://fonts.google.com/specimen/Bagel+Fat+One)**
(Google Fonts, SIL OFL 1.1, by Kyungwon Kim and JAMO). It is a single-weight,
very heavy rounded display face. The match is based on four caption lines from
two videos; see `references/research-notes.md` for the method and caveats.

Fallbacks, in order:

1. **Lilita One** — same genre, lighter and more geometric.
2. **Cherry Bomb One** — heavier and wider.
3. **Baloo 2 ExtraBold** — softer and lighter.
4. **Modak** — much heavier; use for impact words only.
5. **Arial Rounded MT Bold** — system fallback; its `a` is double-storey, so it
   reads differently.

Do not substitute a default sans (Arial, Roboto, Montserrat) unless the user
asks for it. The rounded, heavy silhouette is most of the look.

### Treatment

Two treatments appear in the reference videos:

| Treatment | Use | Look |
|---|---|---|
| Plain | Default dialogue and narration | White fill, heavy black stroke, soft black shadow |
| Styled | Punchlines, threats, stylized bits | White fill, violet-blue glow or stroke, black shadow |

Details:

- **Size:** the white glyphs are roughly 8-11% of frame height in the sampled
  720p frames (about 60-75px). Match the proportion, not a fixed point size.
- **Stroke:** heavy; about 4-6px at 720p, scaled with the type.
- **Glow:** violet-blue, around `#6D3AC4`; keep it outside the white fill so
  the words stay crisp.
- **Shadow:** short, soft, black; do not use a long directional drop shadow.
- **Placement:** bottom center, around 65-80% of frame height. Keep clear of the
  kill feed, crosshair, ammo counter, and subtitles.
- **Case:** Pubz mostly uses lowercase or sentence case, even on loud lines. The
  energy comes from size, color, and timing. All caps is an option for a single
  impact word, not the default.
- **Line count:** one line where possible; two short lines only when the phrase
  needs it.
- **Tracking:** tight. Do not add wide letter spacing; the sampled lines match
  the font's natural spacing within about 5%.

### Rules

- Caption every spoken line that matters to the joke or story.
- 2-6 words per card. Break at natural phrase boundaries.
- Highlight one keyword with an accent color only when the line needs it.
- Do not caption every breath, every "um", or the entire transcript.
- Check sync after every cut. Captions drift when the timeline changes.
- If Bagel Fat One is missing, install it before styling. A fallback is better
  than a generic sans, but it will not look the same.

## Meme system

A meme overlay should do one of these jobs:

1. **Translate** a line into a visual punchline.
2. **Exaggerate** a reaction that is already funny.
3. **Call back** to an earlier moment.
4. **Break the fourth wall** about the edit itself.

If it does none of those, cut it.

Rules:

- Time the overlay to the triggering word, not the start of the clip.
- Hold for 0.5-2 seconds; longer only if the meme is the joke.
- Do not stack three memes on one line.
- Prefer the user's own library or licensed assets.
- Keep a "meme bank" organized by reaction: confusion, victory, defeat, shock,
  disgust, fake confidence, awkward silence.

## Sound design

- Layer SFX under the reaction, not over the dialogue.
- Categories: whoosh, impact, record scratch, anime wow, crowd gasp, boing,
  explosion, cash register, dial-up, error, silence.
- Use silence before a punchline. One beat of nothing is funnier than more noise.
- Duck music under dialogue and game callouts.
- Keep game audio audible; it sells the play.
- Use a limiter on the master. Screams should be loud, not clipped.
- Cut the music on the punchline when the joke needs to land dry.

## Comedy mechanisms

### 1. Escalation

Start normal, repeat with a small twist, then push to an absurd extreme. Three
beats is usually enough. The fourth repeat needs a new angle or it dies.

### 2. Commitment

Commit to the bit. If a player adopts a voice or character, stay in it longer
than feels comfortable, then break it at the right moment.

### 3. Deadpan contrast

Put a calm, mundane line under chaos. The contrast is the joke. Do not add a
laugh track or a caption explaining it.

### 4. Meta-editing

Let a line comment on the edit, then execute it: "use me as a transition",
"this is where the bass drops", "put a meme here". Use this sparingly; it is a
seasoning, not the whole video.

### 5. Running bits

Set up a phrase, character, or fail early. Return to it at least twice with
escalation. Pay it off near the end. A running bit is stronger than a new meme.

### 6. Callback ending

End on the earliest joke, now transformed. Do not end on a generic outro.

## Pacing map

| Section | Cut rhythm | Effects | Captions | Audio |
|---|---|---|---|---|
| Cold open | 0.5-1.5s | 2-3 punch-ins, one meme | every line | loud, immediate |
| Context | 2-4s | minimal | key lines only | clean dialogue |
| First bit | 1-2s | punch-ins, 1-2 SFX | every joke | music starts |
| Escalation | 1-2s | memes, shakes, split-screen | dense | layered |
| Running bit | 1-3s | callback visual | keyword highlight | silence before payoff |
| Peak | 0.5-2s | maximum 2 effects at once | every line | loud, then drop |
| Button | hold 2-4s | none | final line | silence or sting |

## Do / don't

**Do**

- Cut the boring parts, not the setup.
- Let the game audio breathe when the play is tense.
- Use captions to make quiet lines funny.
- Build a meme bank and a SFX bank before editing.
- Watch the cut once without pausing before exporting.
- Keep a backup of the original project.

**Don't**

- Add a meme every two seconds just because the style is dense.
- Use the same sound effect as a crutch.
- Cover the crosshair, kill feed, or ammo counter.
- Explain the joke in a caption.
- Copy Pubz's actual jokes, thumbnails, or assets.
- Use slurs, hate, or targeted harassment for shock value.

## Reference analysis

When the user provides new reference clips, analyze them with
`references/reference-analysis-template.md`. Look for:

- scene changes per minute
- average shot length
- caption style and placement
- meme frequency and type
- SFX categories and density
- music drops and silences
- recurring phrases and running bits
- how the cold open and ending work

Update this guide only after the pattern appears in at least three clips. One
clip is an anecdote; three is a style.
