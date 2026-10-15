# claude-skills

Claude Code skills and agents, each installable with one command.

## video-watch

Lets Claude Code actually watch a video from YouTube, TikTok, Instagram, X or a local file: it downloads the video, transcribes it (captions first, then local faster-whisper), extracts frames and reads them. Comes with the `video-analyst` agent, which does the watching in its own context.

Install (macOS, Linux, or Windows through Git Bash):

```bash
curl -fsSL https://raw.githubusercontent.com/amadejdemsar-create/claude-skills/main/video-watch/install-video-watch.sh -o install-video-watch.sh
bash install-video-watch.sh
```

What the installer does, and nothing else:

1. Moves an existing `~/.claude/skills/video-watch` or `~/.claude/agents/video-analyst.md` to `~/.claude/backups/`.
2. Writes the skill to `~/.claude/skills/video-watch/` and the agent to `~/.claude/agents/video-analyst.md`.
3. Installs uv, ffmpeg and yt-dlp (Homebrew on macOS, apt on Linux, winget on Windows) and a local faster-whisper environment inside the skill folder. No API keys, no accounts.

Then restart Claude Code, paste a video link and write "watch this video and summarize it".

Pipeline scripts are vendored from [bradautomates/claude-video](https://github.com/bradautomates/claude-video) (MIT); see `CREDITS.md` inside the installed skill.
