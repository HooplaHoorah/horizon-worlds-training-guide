# Glam Scene Investigation (GSI) – Game Outline

## 1. Concept & Scope

- **Brief Synopsis**
- **Target Session Length** – e.g. 5–8 minute cases.
- **Audience & Tone** – mobile‑first, casual sleuthing with fashion humor.

## 2. Core Loop Overview

- **Dispatch & Briefing** – how cases are presented to the player.
- **On‑Scene Investigation** – exploring the location, finding clues.
- **Interrogation** – questioning NPCs.
- **Deduction** – filling out the Case Report (WHO / WHAT / WHY).
- **Verdict & Rewards** – debrief, ratings, cosmetics or badges.
- **Replay & Progression** – how replay works and how future cases unlock.

## 3. Hub World (“GSI HQ”)

- **Spawn / Lobby Layout** – central area for players to start.
- **Dispatch Board UI** – interactive panel listing available cases.
- **Leaderboards & Ratings** – customizable names/visibility (leveraging v241 features).
- **Portal / Case Teleporters** – doors to each case environment.
- **Optional Decoration & Lore** – posters, teaser screens for future episodes.

## 4. Case Template (reused for each episode)

1. **Episode Title & Synopsis** – short hook.
2. **Location & Layout** – a small, distinctive environment (runway, wedding reception, influencer set, etc.).
3. **Suspect Archetypes** – 3–4 NPCs with short bios and motives.
4. **Clue Placement** – list of hotspots, their descriptions, and what evidence they reveal.
5. **Interrogation Dialogues** – 2–3 lines per suspect plus conditional responses.
6. **Deduction Options** – candidate WHO / WHAT / WHY choices.
7. **Truth Pattern** – the correct answer and how clues point to it.
8. **End Sequence** – how the reveal is staged and what feedback the player receives.

## 5. Core Systems & UI Components

- **Evidence Board / Case Report UI** – interactive selection panel for WHO / WHAT / WHY.
- **NPC Interaction System** – simple “Talk” button that plays VO/text lines and reacts to found clues.
- **Clue Collection Mechanic** – tap‑to‑inspect hotspots that add entries to the Evidence Board.
- **Ratings & Rewards** – star ratings, badges, and leaderboard integration.

## 6. Art Direction & Audio

- **Visual Style Guide** – glam colors, clean lines, low‑polygon assets for mobile performance.
- **Character Design Notes** – silhouettes and fashion archetypes.
- **Sound & Music** – ambient loops, fashion show chatter, short stingers for reveals.

## 7. Implementation Roadmap

1. **Greybox the Hub & a Single Case** – create simple geometry placeholders and portals.
2. **Script the Core Loop** – state machine controlling case flow (intro, exploration, interrogation, deduction, verdict).
3. **Populate Clues & Dialogues** – add hotspots and NPCs with their lines.
4. **Build the Evidence Board UI** – test the WHO / WHAT / WHY selection and verdict logic.
5. **Polish Pass** – replace placeholders with styled assets; add lighting, effects, and audio.
6. **Integrate Leaderboards** – set up a “Best Sleuths” board with custom names & visibility.
7. **Playtest & Iterate** – run through the case on mobile; tweak readability, pacing, and clue clarity.
8. **Add Additional Cases** – reuse the template to build more episodes, adjusting locations and crimes.
