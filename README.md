# B-Roll Finder — Claude Code Skill

A Claude Code skill for video editors and producers.

Paste a script → AI finds B-roll sources → downloads videos → generates a source credits doc.

---

## What It Does

| Phase | Action |
|-------|--------|
| 1. Script Analysis | AI reads your script and extracts scenes that need B-roll |
| 2. Source Search | Searches YouTube, news outlets (Reuters, AP, BBC), and image libraries |
| 3. Interactive Loop | Add keywords, change source type, or paste URLs directly |
| 4. Auto Download | Downloads selected YouTube videos in 4K MP4 |
| 5. Source Doc | Generates `sources.md` with titles, links, and ready-to-use credit lines |

---

## Installation

### Step 1: Install Claude Code

Download from [claude.ai/code](https://claude.ai/code) and follow the setup guide.

### Step 2: Install yt-dlp

Open Terminal and run:

```bash
brew install yt-dlp
```

> If you don't have Homebrew: go to [brew.sh](https://brew.sh) and follow the one-line install at the top.

### Step 3: Install the skill

```bash
git clone https://github.com/JYNIDA/broll-finder.git ~/.claude/skills/broll-finder
```

That's it.

---

## How to Use

Open Claude Code and type either:

```
/broll-finder
```

or just:

```
b-roll 찾아줘
```

Then paste your script when prompted. Claude walks you through the rest.

---

## What You Can Do During Search

- **Add a keyword**: type any keyword and Claude asks what type (YouTube / news article / photo)
- **Paste a URL directly**: Claude auto-detects the source and adds it to the download list
- **Request more results**: "장면 2 더 찾아줘", "Reuters 영상도 찾아줘"
- **Finalize**: say "이걸로 할게" or "다운로드 시작" when ready

---

## Output

- **Videos**: saved to `~/Desktop/Cowork/B-Roll/[episode name]/`
- **Source doc**: `sources.md` in the same folder — includes title, link, channel name, upload date, and a formatted credit line for each video

---

## Requirements

- macOS (tested on macOS 14+)
- Claude Code (any plan)
- `yt-dlp` (free, open source)
- Notion MCP (optional — for auto Notion upload)

---

## Updating

When a new version is released, run:

```bash
cd ~/.claude/skills/broll-finder && git pull
```

---

## Notes

- YouTube downloads are for editorial reference and B-roll use. Verify licensing before broadcast use.
- Instagram Reels may require login cookies — Claude will notify you if this is the case.
