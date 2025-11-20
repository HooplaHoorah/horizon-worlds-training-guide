# Meta Horizon Contests 2025 – Overview

> Single source of truth for our team (ChatGPT + Grok + Gemini + Horizon Creator Assistant) to win at least one of the 2025 Meta contests.

## 1. Contests We’re Entering

### 1.1 Meta Horizon Creator Competition: Mobile Innovation

- **Devpost page:** (insert link)
- **Platform:** Horizon Worlds (mobile-first, VR optional)
- **Key dates**  
  - World Broadcast ID deadline: **Dec 1, 2025 – 10:00am PT**  
  - Submission deadline: **Dec 8, 2025 – 5:00pm PT**
- **Prize pool:** $1.5M total.
- **Requirements (high level)**
  - Brand-new world published between **Nov 3 – Dec 8, 2025**
  - Must run on **mobile** (phone / tablet); VR optional
  - World must be **public**
  - Owner must be in the **Meta Horizon Creator Program**
  - Submission package:
    - ≤3-minute **mobile demo video**
    - 200–300 word written description
    - Choose up to **3 special categories**
  - Strong bonus for using built-in **GenAI tools** (code, textures, audio, metadata, NPCs).

- **Special categories we’ll probably target (tune later)**
  - Best Portrait Mode Implementation
  - Best Use of Tap-to-Move
  - Best Potential World Broadcast Implementation
  - Best Social Experience
  - Best Memorable NPC Implementation
  - Best New User Onboarding Experience
  - Best Coziness-Themed World / Winter-Holiday-Themed Addition

---

### 1.2 Meta Horizon Start Developer Competition 2025

- **Devpost page:** (insert link)
- **Platform:** Quest apps (Unity / Unreal / Native Android / React Native / Spatial SDK / Immersive Web SDK)
- **Key date**
  - Submission deadline: **Dec 9, 2025 – 12:00pm PT**
- **Prize structure (high level)**
  - Tracks: Entertainment, Lifestyle, Casual Gaming, Social Gaming
  - Big cross-track bonuses for:
    - Best Hand Interactions
    - Best Passthrough Camera Access + AI
    - Best Spatial SDK / Immersive Web SDK apps

- **Requirements (high level)**
  - Join the **Meta Horizon Start Program**
  - Upload APK to the **Competition** release channel
  - <3-minute **Quest demo video**
  - Must run at **≥60 FPS** on Quest 3/3S

*(For full, line-by-line rules, see [meta-horizon-2025-full-rules.md](meta-horizon-2025-full-rules.md).)*

---

## 2. Cross-Contest Strategy

We build **one core experience** and express it two ways:

1. **Horizon Worlds world – Mobile Innovation contest**
   - Cozy winter / social hub world
   - Tuned for **portrait mode + tap-to-move**
   - Memorable **NPC cast** using Horizon NPC archetypes and Creator Assistant
   - Uses GenAI texture/audio tools for polish
   - Target categories: portrait, tap-to-move, social experience, cozy/winter theme, memorable NPCs, onboarding, and possibly broadcast integration.

2. **Quest app – Start Developer Competition**
   - Port the same core idea into Unity or another supported stack
   - Add:
     - **Hand-tracking interactions** for primary verbs
     - **Passthrough + AI companion** for ambient guidance and effects
   - Target track: **Casual Gaming** or **Social Gaming**, plus special awards (hand interactions, passthrough + AI, Spatial / Immersive Web SDK where applicable).

---

## 3. Multi-LLM Collaboration Plan

We’re explicitly a **four-AI stack**:

- **ChatGPT (this repo)**  
  Repo docs, code skeletons, Horizon scripting help, planning.
- **Grok**  
  Contest research double-checks, alt-concepts, spicy script rewrites.
- **Gemini**  
  Multimodal ideation (storyboards, UI flows) and Quest-side code suggestions.
- **Horizon Creator Assistant / in-editor LLM**  
  TypeScript snippets, NPC behaviors, GenAI asset prompts **inside** the editor.

**Working agreement**

1. **Single source of truth for rules & dates**
   - The file [meta-horizon-2025-full-rules.md](meta-horizon-2025-full-rules.md) in this directory is canonical for rules.  
   - This overview file is a short summary of the rules and strategy.

2. **Where things live**
   - **GitHub repo** – training guides, design docs, scripts, code samples, build notes.
   - **Dropbox folder** – PDFs, exports of AI chats, video scripts, pitch decks, raw assets.

3. **Daily flow (during sprint)**
   - Optional daily log in `contests/daily-logs/` (see roadmap).
   - Summarize key decisions from Grok / Gemini / in-editor chats back into this repo or the Dropbox doc.

---

## 4. Next Planning Files

Planned (and safe to stub now):

- `contests/meta-horizon-2025-roadmap.md` – timeline + task breakdown.
- `contests/meta-horizon-2025-assets.md` – NPCs, environments, GenAI prompt library.
- `contests/daily-logs/YYYY-MM-DD.md` – one file per heavy workday during the push.
