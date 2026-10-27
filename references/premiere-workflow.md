# Premiere Pro Workflow

This is the practical Premiere Pro + MCP version of the Pubz-style workflow. Tool
names differ between MCP servers. Use the discovery tools your server provides;
do not invent a tool name.

## Recommended bridge

Two active community options:

| Bridge | Why use it |
|---|---|
| [leancoderkavy/premiere-pro-mcp](https://github.com/leancoderkavy/premiere-pro-mcp) | Client-neutral, active, CEP panel, hundreds of tools, good default for OpenCode. |
| [hetpatel-11/Adobe_Premiere_Pro_MCP](https://github.com/hetpatel-11/Adobe_Premiere_Pro_MCP) | Smaller default tool surface via `search_tools`/`invoke_tool`, plus an installable skill. Installer is macOS-first; Windows needs a manual build. |

Neither is an official Adobe product. Test on a copy of a project.

## Setup: leancoderkavy bridge

Requirements:

- Premiere Pro 2020-2026 on Windows or macOS.
- Node.js 20.19 or newer.
- Premiere, the bridge, and OpenCode on the same computer.

Install:

```powershell
npm install -g premiere-pro-mcp
premiere-pro-mcp --install-cep
premiere-pro-mcp --doctor
```

Restart Premiere. Open a project, then:

```text
Window > Extensions > MCP for Adobe Premiere Pro
```

Start the bridge and confirm it reports a connection.

Register with OpenCode:

```powershell
opencode mcp add --global premiere-pro -- premiere-pro-mcp
```

This writes the server to the global OpenCode config. Start a new OpenCode
session after changing MCP configuration.

## Setup: hetpatel bridge

```powershell
npm install -g adobe-premiere-pro-mcp
premiere-pro-mcp --install-cep
premiere-pro-mcp --doctor
```

Restart Premiere, open `Window > Extensions > MCP Bridge (CEP)`, set the temp
directory, save, and start the bridge.

On Windows, the MCP entry normally points at the built server:

```text
command: node
args: ["C:\\path\\to\\Adobe_Premiere_Pro_MCP\\dist\\index.js"]
env: PREMIERE_TEMP_DIR=C:\\Users\\<you>\\AppData\\Local\\Temp\\premiere-mcp-bridge
```

Use the repository's current README for exact paths. The skill that ships with
that repo can guide the install:

```powershell
npx skills add hetpatel-11/Adobe_Premiere_Pro_MCP --skill premiere-pro-mcp
```

## First connection test

Ask OpenCode to run only read-only calls:

```text
Use premiere-pro to get the current project info, list sequences, and list
project items. Do not edit, delete, or export anything.
```

If that works, duplicate the sequence and make one test cut. Do not start with a
real edit.

## Track layout

Use a consistent layout:

```text
V4  meme overlays / GIFs / PNGs
V3  captions / titles
V2  facecam / picture-in-picture
V1  gameplay
A1  voice / Discord
A2  voice / Discord (second track)
A3  game audio
A4  music
A5  sound effects
```

Adjust to the project, but keep dialogue, game audio, music, and SFX separable.

## Tool mapping

Use the equivalent tools in your MCP server. Typical categories:

| Job | What to look for |
|---|---|
| Inspect project | get project info, list sequences, list project items, active sequence |
| Import media | import files/folders, create bins, set media metadata |
| Create sequence | create sequence from clips, duplicate sequence, set sequence settings |
| Rough cut | razor, ripple delete, trim, move, insert/overwrite |
| Punch-ins | set scale/position, add keyframes, transform effect |
| Captions | create captions, import SRT, style captions, graphics templates |
| Effects | apply effect, set effect parameters, keyframe effect |
| Audio | set clip volume, add gain, mute, duck music, add SFX |
| Markers | add marker, label marker, move playhead to marker |
| Export | set export preset, set output path, render/export |

If a category is missing, stop and tell the user. Do not guess a tool name or
write raw ExtendScript unless the user explicitly asks for that fallback.

## Workflow with approval gates

### Gate 1: read-only audit

1. Get project info.
2. List sequences.
3. List project items.
4. Confirm the active sequence.
5. Duplicate the sequence and name it `<original> — PUBZ PASS`.

Return a short summary. Do not edit yet.

### Gate 2: beat sheet

1. Transcribe or scan the recording.
2. Identify 5-9 bits.
3. Return the beat sheet table from `SKILL.md`.
4. Ask the user to approve, cut, or reorder.

Do not start the rough cut until the beat sheet is approved.

### Gate 3: rough cut

1. Build the selected ranges into the duplicate sequence.
2. Remove dead air and repeated non-escalating attempts.
3. Keep setups for every payoff.
4. Add markers for punch-ins, memes, SFX, and callbacks.
5. Return a change log and the new duration.

Stop before adding effects. Let the user review the story.

### Gate 4: style pass

Apply in this order:

1. Punch-ins and shakes.
2. Meme overlays.
3. Captions.
4. SFX and music.
5. Final audio mix.

After each pass, return a short change log. Do not stack all passes into one
unreviewable operation.

### Gate 5: export

1. Confirm resolution, frame rate, codec, bitrate, and output path.
2. Export a review file.
3. Watch it once without pausing.
4. Fix the three highest-impact issues.
5. Export the final master.

Never overwrite an existing export without confirmation.

## Suggested Premiere settings

- Sequence: match the gameplay source, usually 1920x1080 or 3840x2160 at 60 fps.
- Preview: 1/2 or 1/4 resolution while editing; full for QA.
- Export review: H.264, 1080p, 12-16 Mbps.
- Export master: H.264, source resolution, 20-40 Mbps, AAC 320 kbps.
- Loudness: keep dialogue around -12 to -6 LUFS short-term; true peak below
  -1 dBTP.

These are starting points, not rules. Match the user's platform and delivery
spec.

## Troubleshooting

| Symptom | Check |
|---|---|
| MCP server not listed | Restart OpenCode after editing config; run `opencode mcp list`. |
| Server starts but tools fail | Is Premiere open? Is a project open? Is the CEP panel started? |
| Wrong sequence edited | Re-run active sequence, list sequences, and confirm the duplicate name. |
| Captions drift | Re-sync after cuts; do not caption before the picture lock. |
| Export fails | Confirm output path, disk space, and that the sequence is not locked. |
| Premiere shows a modal dialog | Stop the agent, close the dialog manually, then reconnect. |
| CEP panel missing | Reinstall the CEP extension and restart Premiere. |

## Safety

- Work on a duplicate project or sequence.
- Keep the original media untouched.
- Do not delete, overwrite, relink, or export without explicit approval.
- Treat the bridge as full access to Premiere. Review the server's permissions and
  telemetry settings before use.
- The `hetpatel` bridge enables anonymous telemetry by default; set
  `PREMIERE_MCP_TELEMETRY=0` if you do not want it.
