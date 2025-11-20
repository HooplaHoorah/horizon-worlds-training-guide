# Glam Scene Investigation (GSI) – Detailed Outline

This document expands upon the initial table‑of‑contents outline for **GSI: Glam Scene Investigation**.  It breaks each section into actionable components and suggests ways to leverage new features from the Meta Horizon Worlds Desktop Editor (MDE) v241.  Use this as your design spine when planning instructions for the World Development Environment (WDE) or when dividing work across a team.  Feel free to copy sections directly into your series bible or design docs.

## 1. Concept & Scope

### Brief Synopsis

*GSI: Glam Scene Investigation* is a mobile‑friendly episodic mystery game set in a hyper‑stylish universe where fashion faux pas and social disasters are treated like crimes.  Players take on the role of **Fashionista Sleuths** dispatched by an elite headquarters to investigate who committed a glam crime, what the offense was, and why it happened.  Each case plays like a self‑contained 5–8 minute episode with a clear beginning, middle and end, encouraging replayability and social engagement.

### Target Session Length

* **5–8 minutes per case.**  This is long enough to let players explore, interrogate suspects and deduce the correct answer without overstaying their welcome on mobile devices.  MDE v241’s new “record your world” feature (for MHCP participants) can help you capture playtests and confirm that sessions remain within this window.

### Audience & Tone

* **Mobile‑first.**  All UI should be readable on a portrait phone screen with large tap targets.  Avoid long paragraphs of text—think short tooltips, icons and voice‑over (VO) lines.
* **Casual sleuthing.**  The puzzles should be approachable and not rely on obscure knowledge.  Clues and motive options must be clear enough for players to feel clever without frustration.
* **Fashion humour.**  The tone is playful and camp: snarky commentary, over‑the‑top NPC personalities and dramatic reveals reminiscent of reality TV judging.  Crimes aren’t lethal; they’re reputational and etiquette‑related.

## 2. Core Loop Overview

### Dispatch & Briefing

1. **Case Incoming:** At the GSI HQ hub, players see a dispatch board or “case tablet.”  A new call lights up with a quick summary (location, stakes, suspected offense).  Use MDE’s UI panels to create an interactive card; clicking it teleports players to the case world.
2. **Difficulty Selection (optional):** Offer “Cozy” and “Sleuth” modes.  Cozy shows fewer red herrings; Sleuth presents extra clues and harder deductions.  You can implement difficulty toggles using variables and conditional spawners.

### On‑Scene Investigation

1. **Focused environment:** Each episode is set in a single, compact location designed for portrait orientation—e.g., a runway, wedding reception or influencer set.  Keep geometry simple (low poly) and use bold colour blocking to sell the glam aesthetic.
2. **Clue hotspots:** Place 8–10 interactive objects (dress tags, invitations, makeup kits, phones) in logical spots.  When tapped, they display a short VO/text bubble and add an entry to the Evidence Board.  Use MDE v241’s improved toolbar to quickly duplicate and re‑position hotspot prefabs.
3. **NPC placement:** Populate the scene with 3–4 suspects and a few bystanders.  NPCs have idle animations and speech bubbles to attract attention but remain within a tight area to minimise travel.

### Interrogation

1. **Approach & Talk:** As players approach a suspect, a large “Talk” button appears.  Pressing it triggers a VO line and on‑screen subtitle.  Limit each suspect to 2–3 base lines plus one conditional line unlocked by specific clues.
2. **Branching hints:** Some dialogue lines should contradict a clue or another NPC’s statement.  Track which clues a player has found and swap dialogue accordingly (e.g., if you discovered a torn hem, the Designer might nervously deflect).

### Deduction

1. **Evidence Board UI:** Return players to a dedicated area (or overlay panel) containing a three‑row matrix: **WHO**, **WHAT**, **WHY**.  Each row lists the discovered options; players tap one per row to fill in their report.
2. **Confidence / Submit:** After selecting all three elements, a “Submit Report” button appears.  Optionally display a confidence meter indicating how many clues the player found.  You could also use MDE’s new leaderboard feature here—e.g., track fastest correct deduction times.

### Verdict & Rewards

1. **Reveal Cut‑scene:** Show a short sequence where the GSI host breaks down the truth pattern.  Highlight the key clues that pointed to the culprit and play a stylish stinger (e.g., camera shutters, gasp sound).
2. **Rating & Cosmetics:** Award players a rating (e.g., 1–5 stars) based on accuracy and efficiency.  Unlock badges or titles tied to case types (e.g., “Runway Rescuer,” “Wedding Whisperer”).  MDE v241 allows you to customise leaderboard names and visibility; create a “Best Sleuths” board in the hub for players with high ratings.

### Replay & Progression

1. **Case Reset:** After the verdict, offer buttons to **Replay** (shuffling clue order and red herrings) or **Return to HQ**.  On replay, randomise some hotspots and dialogue ordering so the experience feels fresh.
2. **Unlock Next Cases:** Use variables to track which cases a player has solved.  Completed cases on the dispatch board could dim or display a “Solved” ribbon; new cases appear as players finish prior episodes.  MDE’s new “My Events” beta tab can be used later to schedule live case premieres.

## 3. Hub World (“GSI HQ”)

### Spawn / Lobby Layout

* Create an open‑plan HQ with a reception desk, stylish décor and a large dispatch board.  Use symmetrical layout to keep orientation clear on mobile.  Provide seating or small props to encourage socialising.

### Dispatch Board UI

* Build an interactive wall or holographic screen listing available cases as cards.  Each card shows: case title, one‑line hook and status (Locked, New, Solved).  Clicking a card teleports the player to the case world.  For scalability, group cards in rows and add scroll behaviour if you plan many episodes.

### Leaderboards & Ratings

* Leverage MDE v241’s customisable leaderboards by adding a **“Best Sleuths”** board.  Track metrics like number of correct cases solved, fastest solving time and highest average rating.  Use custom names (e.g., “Style Icons”) to fit your theme.  Provide an option to toggle visibility (private vs. public rankings).

### Portal / Case Teleporters

* Represent each case with a themed portal (e.g., a wedding arch, runway curtain).  To prevent clutter, portals could appear only when the corresponding dispatch card is selected.

### Optional Decoration & Lore

* Fill the HQ with posters teasing future episodes, fashion trophies, and Easter‑egg references to the larger GSI universe.  This gives returning players something new to notice.  Keep polygon counts low to maintain mobile performance.

## 4. Case Template

For consistency and rapid content creation, structure each episode using the following eight elements.  Store them in a template document so writers and level designers can fill in the blanks.

1. **Episode Title & Synopsis** – A catchy name and a one‑sentence hook (e.g., “Runway Ruin: The show‑stopping gown fails mid‑walk—accident or sabotage?”).
2. **Location & Layout** – Describe the environment and draw a simple map.  Mark where suspects stand, clue hotspots are placed and the exit/back button resides.  Note any decorative elements tied to the theme.
3. **Suspect Archetypes** – List 3–4 characters with names, fashion personas and potential motives.  Include a sentence on their relationship to the victim/event.
4. **Clue Placement** – Identify 8–10 interactive objects.  For each, specify what the player sees, what evidence it adds (text or icon) and which suspect/motive it implicates or exonerates.
5. **Interrogation Dialogues** – Write 2–3 base lines per suspect plus at least one line that only triggers if a specific clue has been found.  Keep lines short (1–2 sentences) and use distinctive voices.
6. **Deduction Options** – Enumerate the candidate WHO, WHAT and WHY options that appear on the Evidence Board.  Include at least one plausible red herring in each category.
7. **Truth Pattern** – Define the correct combination and explain why (e.g., “Stage Tech loosened the hem because they were jealous of the designer’s promotion”).  Mention the critical clues and contradictory statements.
8. **End Sequence** – Outline the reveal: any small animations, sound cues and final VO lines.  Note how ratings are calculated and what badge/title is awarded.

## 5. Core Systems & UI Components

### Evidence Board / Case Report UI

* Implement as a large panel with three rows labelled WHO, WHAT and WHY.  Each row contains icon‑based buttons representing discovered suspects, offenses and motives.  Buttons dim when selected; a “Submit” button activates once all three rows are filled.  Consider using colour coding (e.g., pink for suspects, gold for offenses, cyan for motives) for quick visual parsing.

### NPC Interaction System

* Use simple proximity detection to display a Talk button when a player is near an NPC.  The button triggers a sequence of dialogue lines; optionally show the NPC’s facial expression or audio reaction.  If a clue condition is met, swap in the conditional line.  Keep a flag per NPC to avoid repeating the same lines on subsequent interactions unless needed for hints.

### Clue Collection Mechanic

* Each hotspot is a small collider or object with a glow/shimmer effect to attract attention.  Tapping it triggers a short VO/tooltip and adds an entry to the Evidence Board.  To avoid clutter, show the name of the clue and a small icon rather than long text.  Use a subtle sound when collecting to give feedback.

### Ratings & Rewards

* At the verdict stage, calculate a rating based on: (1) correctness of WHO/WHAT/WHY, (2) number of clues collected, (3) time taken (if you implement timers).  Translate the score into star ratings or titles such as “On‑Trend Detective” or “Runway Rookie.”  Use MDE’s leaderboard to persist top scores.

## 6. Art Direction & Audio

### Visual Style Guide

* **Palette:** Lean into rich jewel tones, metallic accents and neon highlights.  Avoid realistic textures; flat shading works better on mobile and emphasises silhouettes.
* **Geometry:** Use low‑poly models with exaggerated shapes to evoke couture fashion pieces (e.g., oversized hats, giant shoulder pads).  Props should feel glamorous but not heavy.
* **Lighting:** Soft ambient light with contrasting spotlights on key areas (e.g., clue hotspots, suspect positions).  Use colour gels to differentiate spaces within a scene.

### Character Design Notes

* **Silhouettes:** Each suspect archetype should be recognisable at a glance (e.g., the Rival Model has a tall, slender shape with angular poses; the Stage Tech has headphones and a utility belt).  Customise avatars with bold accessories rather than relying on high‑detail clothing.
* **Colour coding:** Assign signature colours to each suspect to help players track them during interviews and on the Evidence Board.

### Sound & Music

* **Ambient loops:** Create a subtle soundtrack appropriate to each case setting (fashion show crowd murmurs, wedding chatter, studio ambience).  Keep loops short and seamless.
* **Stingers & cues:** Use distinct sounds for clue collection, suspicion reveals, and verdict announcements.  Consider a camera shutter or applause sound for dramatic effect.
* **Voice‑over:** If possible, record VO for the GSI dispatch voice and suspect lines.  Use crisp, energetic reads with playful intonation to sell the humour.

## 7. Implementation Roadmap

### 1. Greybox the Hub & a Single Case

* In MDE, start with simple primitives to block out the HQ layout and your first episode environment.  Position dummy NPCs and hotspots without details.  Test navigation on mobile early to ensure spaces feel intuitive.

### 2. Script the Core Loop

* Build a state machine controlling the flow: **Intro → Exploration → Interrogation → Deduction → Reveal → Replay/Exit**.  Use variables to track progress and to enable or disable UI elements as needed.

### 3. Populate Clues & Dialogues

* Replace dummy hotspots with specific clues.  Write and test all NPC lines, ensuring conditional dialogue triggers correctly.  Use MDE’s text tools to keep messages within the screen width for portrait devices.

### 4. Build the Evidence Board UI

* Create the interactive case report panel.  Bind discovered clues to UI elements; ensure selection and submission work across multiplayer sessions.  Consider using containers or groups to manage row and column alignment.

### 5. Polish Pass

* Swap greybox assets for polished models following your style guide.  Add lighting, effects, ambient audio and decorative elements.  Incorporate the new leaderboard with custom names, and ensure the rating badges display properly.

### 6. Integrate Leaderboards

* Configure leaderboards to track desired metrics (e.g., highest ratings, fastest solve times).  Use the MDE v241 feature to name them thematically (“Style Icons,” “Top Sleuths”) and choose whether they are global, friends‑only or session‑based.

### 7. Playtest & Iterate

* Run through the case on actual mobile devices.  Note readability, navigation issues, and whether clue distribution feels balanced.  Adjust hotspot placement, dialogue pacing and UI sizing accordingly.

### 8. Add Additional Cases

* Once the template and systems are solid, expand the roster of episodes.  Use the template structure to fill in new case details (locations, suspects, crimes).  Introduce new mechanics slowly (e.g., timed challenges, multi‑stage puzzles) only after the core loop is stable.

---

This expanded outline should provide enough detail to begin drafting concrete WDE instructions and building out the first GSI case in the updated MDE.  Adapt and refine as you gather feedback from playtests and as new editor features become available.