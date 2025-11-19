# DL Instructions

This document provides standardized instructions for downloading, syncing, and managing files across our workflow for the Meta Horizon 2025 contests.

## 1. Overview

We use a dual-location workflow combining:

- **GitHub repository** – code, documentation, world scripts, structured assets.
- **Dropbox shared folder** – large files, videos, rule PDFs, AI session exports, and working assets.

This DL (Download & Link) instructions file explains how to keep both locations in sync.

---

## 2. Downloading the Repo

To download or clone the main development repository:

```bash
git clone https://github.com/HooplaHoorah/horizon-worlds-training-guide.git
```

If you already cloned it:

```bash
git pull
```

---

## 3. Downloading From Dropbox

Shared folder:

```
https://www.dropbox.com/scl/fo/yf79lkanuiwhax2d1fx64/AEJX4JfA6O56rL6uXLbVJVM?rlkey=d0e702gwfq4rxmeysv901kboe&st=a8egl69k&dl=0
```

### Organization inside Dropbox

- **Rules/** – Official contest rules and Grok-generated summaries
- **Assets/** – Images, textures, audio, reference art
- **Videos/** – Demo captures, export renders
- **AI Sessions/** – Grok, Gemini, ChatGPT collaborative notes
- **World Design/** – UML diagrams, flowcharts, level layout sketches

Download the entire folder:

1. Click **Download → Download folder**, or
2. Sync to your device using the **Dropbox Desktop App**.

---

## 4. Keeping GitHub and Dropbox Synchronized

Use this pattern:

### What belongs in GitHub

- Markdown documentation
- TypeScript scripts for Horizon Worlds
- Unity/Quest source files
- Planning docs and roadmaps
- World logic
- README files

### What belongs in Dropbox

- Videos (>50MB)
- Sound effects generated from GenAI tools
- Prompt logs
- Uncompressed images
- Renders & screen captures
- Pitch decks

---

## 5. Updating the Repo (Workflow)

1. Make local changes.
2. Commit with clear messages:

```bash
git add .
git commit -m "Add DL instructions and sync notes"
git push
```

3. If files are too large for GitHub, put them in Dropbox and note their location in the GitHub doc that references them.

---

## 6. Versioning Notes

- GitHub = authoritative for code & docs.
- Dropbox = authoritative for large binaries & external assets.
- When both systems contain related files, always reference Dropbox with a link in the GitHub doc.

---

## 7. Contact & Collaboration Notes

- **ChatGPT** – primary repo doc generator and planner.
- **Grok** – supplemental rule analysis & alt-strategy drafts.
- **Gemini** – multimodal asset ideation.
- **Meta Creator Assistant** – Horizon-specific code generation and in-editor AI scripting.

All major decisions should be logged in:

```
contests/daily-logs/YYYY-MM-DD.md
```

---

## 8. Last Updated

Automatically revised during Meta Horizon Contest preparation cycle.
