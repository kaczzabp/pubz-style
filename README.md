# Pubz-Style — an OpenCode skill for hyper-edited gaming videos

An OpenCode/agent skill for editing gameplay in the spirit of **Pubz**
([@thepubz](https://www.youtube.com/@thepubz)): fast hard cuts, punch-ins, bold
captions, timed meme overlays, layered sound effects, running bits, and an
intentionally overstimulating pace.

It is **style-inspired, not a clone**. It does not include Pubz's videos, jokes,
artwork, or assets, and it does not assume which editor he uses.

## What this is

A Markdown skill plus reference files:

- `SKILL.md` — the rules and seven-pass workflow an agent loads.
- `references/style-guide.md` — detailed visual, audio, caption, and comedy rules.
- `references/research-notes.md` — what was observed in Pubz videos, with data.
- `references/premiere-workflow.md` — Premiere Pro + MCP setup and workflow.
- `references/reference-analysis-template.md` — how to analyze new reference clips.
- `examples/edit-brief.md` — a ready-to-fill brief.

A skill is instructions, not software. It gives an agent a consistent definition
of the style. It still needs an editor and, for actual timeline control, a bridge
such as a Premiere Pro MCP server.

## Install

### Option A: clone into the OpenCode global skills directory

Windows:

```powershell
git clone https://github.com/kaczzabp/pubz-style.git "$HOME\.config\opencode\skills\pubz-style"
```

macOS/Linux:

```bash
git clone https://github.com/kaczzabp/pubz-style.git ~/.config/opencode/skills/pubz-style
```

Start a new OpenCode session. The skill should appear in the advertised skills
list. Ask:

```text
Use pubz-style to plan an edit for this gameplay recording. Show me a beat sheet
first. Do not cut anything yet.
```

### Option B: copy the folder

Clone anywhere, then copy `SKILL.md` and `references/` into:

```text
%USERPROFILE%\.config\opencode\skills\pubz-style\
```

The directory name should match the skill name: `pubz-style`.

### Hide it from the always-on list

If you want to save the description tokens, add this to the frontmatter of
`SKILL.md`:

```yaml
metadata:
  opencode/autoinvoke: false
```

Then load it explicitly with `@pubz-style` or let `router` handle it.

## Requirements

- **Editor:** Premiere Pro 2020-2026, or DaVinci Resolve Studio.
- **Bridge for actual editing:** one of:
  - [leancoderkavy/premiere-pro-mcp](https://github.com/leancoderkavy/premiere-pro-mcp)
  - [hetpatel-11/Adobe_Premiere_Pro_MCP](https://github.com/hetpatel-11/Adobe_Premiere_Pro_MCP)
  - [samuelgursky/davinci-resolve-mcp](https://github.com/samuelgursky/davinci-resolve-mcp)
- **Runtime:** Node.js 20.19+ for the Premiere bridges; Python 3.10+ for the
  Resolve bridge.
- **Assets:** your own meme, SFX, and music library. The repo ships none.

Without a bridge, the skill can still produce a beat sheet, shot list, caption
plan, and manual edit instructions.

## How to use

1. Install the skill.
2. Install and connect your editor bridge (see `references/premiere-workflow.md`).
3. Open a **copy** of the project.
4. Give the agent a brief like `examples/edit-brief.md`.
5. Approve the beat sheet before the rough cut.
6. Review each pass: rough cut, punch-ins, memes, captions, audio.
7. Export a review file, then the final master.

Example prompts:

```text
Use pubz-style to turn this 45-minute Fortnite VOD into a 9-minute video. Find
the strongest 8 bits, show me a beat sheet, and stop.
```

```text
Apply the Pubz style pass to sequence "Episode 12 — PUBZ PASS". Punch-ins,
captions, 8 meme overlays, and SFX. Keep the game audio audible. Stop before
export.
```

```text
Audit this cut for dead air, weak hooks, overused memes, and captions that cover
the crosshair. Give me the three highest-impact fixes.
```

## Research snapshot

Research date: 2026-10-27.

- Pubz has roughly 113K subscribers and 130 videos.
- Recent titles include "Fortnite but it's OVERSTIMULATING", "Skybasing but the
  editor was LACED", "Minecraft Bedwars **POST LOBOTOMY**", and "Counter Strike
  but the editor was FRIED".
- Two short samples were measured with FFmpeg scene detection:
  - Fortnite (90s): 92 visual changes at threshold 0.3, median 0.53s.
  - Skybasing (120s): 59 visual changes at threshold 0.3, median 1.30s.
- Captions are bold white with black stroke; meme overlays are composited over
  gameplay; the game UI stays visible.
- The videos are structured as 6-13 gameplay/bit chapters, not a traditional
  three-act story.

Full method, caveats, and links: `references/research-notes.md`.

## Important limitations

- **No existing skill knows Pubz automatically.** This one encodes observations
  and a workflow. It will not replicate his taste without human review.
- **Comedy is the hard part.** The agent can cut, caption, zoom, and place assets;
  it cannot reliably choose the funniest moment or time a joke.
- **MCP tools vary.** Different Premiere/Resolve servers expose different tools.
  The skill tells the agent to discover, not invent, tool names.
- **Copyright.** Memes, music, and reference clips may be protected. Use licensed
  or original assets. Do not redistribute Pubz's content.
- **Safety.** The source style includes offensive jokes. This skill matches the
  energy, not the edginess. No slurs, hate, targeted harassment, or sexual
  content involving minors.

## Repository layout

```text
pubz-style/
├── SKILL.md
├── README.md
├── LICENSE
├── .gitignore
├── references/
│   ├── style-guide.md
│   ├── research-notes.md
│   ├── premiere-workflow.md
│   └── reference-analysis-template.md
├── examples/
│   └── edit-brief.md
└── assets/
    ├── README.md
    ├── memes/
    ├── sfx/
    └── music/
```

## License

MIT. See `LICENSE`.

The skill text is original. Pubz's name is used for style identification only;
this project is not affiliated with or endorsed by Pubz.
