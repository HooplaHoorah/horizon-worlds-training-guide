# Meta Horizon Worlds Developer Guide

This guide collects information from the **Learn** section of the Meta Horizon Worlds developer documentation.  It is intended to help new creators become familiar with the tools, workflows and terminology used in Horizon Worlds and to serve as a reference when building an entry for the Meta Horizon mobile competition.

## 1 Introduction

Meta Horizon Worlds lets creators build interactive 3D experiences that run on mobile, desktop and VR.  Worlds are created within the **Horizon Worlds ecosystem** using Meta’s desktop editor and scripting APIs rather than third‑party engines.  Creators can publish publicly accessible worlds and participate in competitions such as the **Mobile Genre Showdown – Reloaded** contest.  The platform encourages exploration and offers numerous resources, tutorials and community channels to help creators get started【867775088697630†screenshot】.

## 2 Getting Started

### 2.1 Tasks for new creators

The **Welcome creators!** section lists the core tasks involved in building and publishing a world.  New developers should:

* **Create a world** in the desktop editor, set up project tooling and choose a starting environment【867775088697630†screenshot】.
* **Add and manipulate assets** – objects, sounds, colliders and gizmos – and import custom models when needed【889338007507527†screenshot】.
* **Build interactivity** with entities and scripting; use code blocks and gizmos to create behaviours【889338007507527†screenshot】.
* **Preview and playtest** the world on mobile or VR, adjust variables and debug scripts in real time【864316467338504†screenshot】.
* **Publish** a public world that runs on mobile or mobile + VR (VR‑only worlds are not eligible for mobile contests) and ensure it complies with Meta’s Community Standards and performance guidelines【936468813332520†screenshot】.

The welcome page also points to additional resources such as performance tools, safety & privacy guidelines, the Horizon Creator Program and the official community Discord【936468813332520†screenshot】.

### 2.2 Installing the desktop editor

The desktop editor is a free Windows application used to build and publish worlds.  Prerequisites include a **Meta Horizons account**, **Windows 10 or later**, an **Intel i5‑4590 or better CPU** and **at least 8 GB of RAM**【702296320149761†screenshot】.  Developers must be **13 years or older** and agree to Meta’s supplemental terms and privacy policy【702296320149761†screenshot】.  Using a TypeScript‑capable IDE such as **Visual Studio Code** is optional but recommended【702296320149761†screenshot】.

To install the editor:

1. Download the installer (`Horizon-worlds-desktop-editor‑v2xx.msi`) from the Learn page and run it【702296320149761†screenshot】.
2. Launch the editor and sign in with your Meta account or create one on the Meta Horizons website【702296320149761†screenshot】.
3. (Optional) Install the **Meta Quest Link** app if you plan to test in VR【702296320149761†screenshot】.

The installation guide links to troubleshooting docs, an introduction to the desktop editor and the **Creator Program** sign‑up page (which offers monetization opportunities, community resources and live events【466433589941461†screenshot】).

## 3 Tool Overview

Meta groups its creation tools into several categories, each accessible through the desktop editor:

### 3.1 Desktop editor

The desktop editor is the primary tool for building cross‑platform worlds.  It lets you add shapes, gizmos, sounds and colliders; create quests, leaderboards and variable groups; write and debug TypeScript scripts; and publish your world【125025447792064†screenshot】.  The editor’s panels make it easy to update properties while the world is running and to test on mobile or VR without republishing.

### 3.2 TypeScript API

Scripts in Horizon Worlds are written in **TypeScript**, a statically typed superset of JavaScript.  Using TypeScript provides autocompletion, type checking and early error detection.  Scripts can be created in the editor and edited in VS Code; Horizon also provides a custom module system for sharing code【600701464595930†screenshot】.

### 3.3 Custom Model Import

Creators can import 3D models from external DCC tools.  Imported assets must be provided as **.FBX files** with optional **.PNG texture maps**.  Once imported, the assets appear in your personal asset library and can include static lighting and custom collision models【705060250920595†screenshot】.  Imported models must respect intellectual‑property rights and comply with Meta’s content policies.

### 3.4 NPCs

Non‑player characters (NPCs) are AI‑controlled entities that can enrich your world.  Horizon offers four archetypes:

| Archetype      | Typical role                                                   |
|---------------|---------------------------------------------------------------|
| **Utility**   | Provide information, sell goods or act as guides【686723547173827†screenshot】. |
| **Storyteller**| Deliver narrative and background context【686723547173827†screenshot】. |
| **Antagonist**| Serve as enemies or obstacles【324334183347804†screenshot】. |
| **Ally**       | Assist or accompany players【324334183347804†screenshot】. |

NPCs are scripted using AI behaviours and can be configured through the editor.

### 3.5 Performance tools

The **Performance tab** displays real‑time metrics for your world (e.g., frame time, physics cost, audio cost).  You can set target values; if a metric exceeds its target, a red dot appears as an alert.  The tab supports scrubbing and tracing, and performance data can be exported for analysis using **Perfetto**【680177325716122†screenshot】.

### 3.6 Generative AI tools

Horizon includes a suite of Gen AI tools that assist with content generation:

1. **Gen AI code tool** – An AI‑powered chat assistant built into the editor.  It can answer questions about the Horizon API and TypeScript, generate scripts and act as a tutor.  Two models are available: **Llama** (general Q&A) and **Specialist** (trained on the API and TypeScript)【737248398031343†screenshot】.
2. **Gen AI Creation Audio tool** – Generates sound effects or ambient audio tracks.  You can choose from sample prompts or craft your own, then download the audio for use in your world【919265386294849†screenshot】.
3. **Gen AI Asset Metadata tool** – Creates titles, descriptions and tags for imported 3D models; it can also apply or edit generated tags【919265386294849†screenshot】.
4. **Gen AI Texture Generation tool** – Produces textures for 3D objects and lets you assign them to meshes, save them to your asset library and generate textures from “wild” objects【161383628032269†screenshot】.

These tools speed up content creation and help non‑experts produce scripts, audio and art assets.

> **Note:** All of the Gen AI tools described above are integrated directly into the **Horizon Desktop Editor**.  You access them through the desktop editor’s interface rather than a standalone website, and they store generated outputs in your local project’s asset library.  There is currently no web‑only version of these tools, so you must be logged into the desktop editor to generate code, audio, metadata or textures【782422281166655†screenshot】.

## 4 Creating Your First World

### 4.1 Tutorial overview

The **Create your first world** tutorial is split into two parts.  The **Overview** explains that part 1 teaches you to create a new world, place and manipulate assets and preview the world on mobile, while part 2 introduces custom model import and scripting【28960424423443†screenshot】.  Prerequisites include having a Meta Horizons account, installing the desktop editor and being comfortable with TypeScript【28960424423443†screenshot】.

The overview also links to other world tutorials (e.g., Build your first game, Camera API examples, Spawning and pooling) which you may explore later【77613856770770†screenshot】.

### 4.2 Part 1 – Building the scene

Part 1 guides you through creating a simple shooting game set in a graveyard【363608379365090†screenshot】.  Key steps include:

1. **Create a new world** – From the Creation Home page click **New World**.  When the editor opens, rename your world and save it【560200653944636†screenshot】.  Meta Horizon Worlds automatically saves your progress as you work【887441586642693†screenshot】.
2. **Place assets** – Open the **Asset Library**, select **Public Assets**, search for “Unfinished Graveyard” and drag it into the **Scene** panel【706139995668170†screenshot】.  Adjust the asset’s position and rotation using the **Properties** panel or the transform gizmo【504906376199085†screenshot】.
3. **Preview and test** – Use the **Play** controls to preview your world and test interactions.  Step 3 of the tutorial shows how to playtest on mobile; part 1 also demonstrates basic camera navigation and hierarchy management.

### 4.3 Part 2 – Importing models and scripting

Part 2 extends the game by importing a custom **rifle** model and writing your first script.  It walks you through:

* **Importing custom models** – You import a 3D asset (e.g., a rifle), place it on a pedestal and make it grabbable.
* **Attaching scripts** – You create a TypeScript script that spawns projectiles, counts points and displays a score when skeletons are hit【94463043809516†screenshot】.
* **Testing in VR** – After scripting, you playtest the game in VR to experience the interactions in a headset.

The tutorial emphasises that only one script can be attached per entity and that scripts can run in either **Default** (server) or **Local** (client) execution modes【887441586642693†screenshot】.

## 5 Additional Tutorials and Resources

The Learn page links to many other tutorials covering topics such as building your first game, adding UI elements, developing for web and mobile, using the camera API, spawning and pooling objects, and creating text and analytics.  These tutorials follow similar step‑by‑step formats and build on the basics covered above【77613856770770†screenshot】.

## 6 Guides for Creators from Other Platforms

### 6.1 Roblox creators

For developers familiar with Roblox, Meta provides a guide comparing Horizon Worlds to Roblox Studio.  Key points include:

* **UI and Terminology differences** – Horizon’s **Hierarchy window** corresponds to Roblox’s **Explorer**, **Scene window** to the **Viewport**, **Assets window** to the **Toolbox**, and the **Asset Library** to the **Creator Store**【162721397772128†screenshot】【554483141494053†screenshot】.
* **Scripting differences** – Roblox distinguishes **client**, **server** and **module** scripts, whereas Horizon scripts are labelled only by their execution mode (Default/server or Local/client)【388691487571856†screenshot】.  Horizon scripts are written in TypeScript instead of Luau and must be assigned an owner when running on the client.
* **Project structure and assets** – Horizon uses **entities** instead of parts and **asset templates** instead of packages/models【554483141494053†screenshot】.  The asset library exposes both your own and public assets created by the community【906058587061684†screenshot】.
* **Networking and events** – Client and server execution are clearly separated; network events allow communication between different instances.  Scripts can call local or network events to trigger behaviour【681399795811306†screenshot】.

### 6.2 UEFN (Unreal Editor for Fortnite) creators

A similar guide exists for creators migrating from UEFN.  It highlights that the **Horizon Desktop Editor** replaces the Epic Games Launcher and UEFN editor, bundling world management, documentation and tutorials into one tool【69373105609560†screenshot】.  Notable differences include:

* **Lightweight editor** – The desktop editor is under 2 GB and supports weekly updates; players do not need to wait for the world to download because content is streamed【69373105609560†screenshot】.
* **Editor comparisons** – A table compares UEFN views with Horizon components (e.g., **Outliner** → **Hierarchy**, **Content Browser** → **Asset Library**, **Main Menu** → **Main Menu + Creator Tools**)【60940473903272†screenshot】.
* **Terminology and engine concepts** – UEFN’s **Actor** or **GameObject** corresponds to a **Horizon entity**; **prefabs** map to **asset templates**; **devices** to **gizmos**; and the scripting language **Verse** to Horizon’s **TypeScript**【501516516035738†screenshot】.
* **Networking and ownership** – Horizon requires creators to manage script ownership; default scripts run on the server and have no client visibility, while local scripts run on the client and must assign an owner before executing locally【146161862990547†screenshot】.
* **Gameplay structure** – Only one script may be attached per entity, and there is no customizable player object.  Developers must implement their own systems for game modes, scoring and player management【146161862990547†screenshot】.
* **Events and communication** – Horizon uses local and network events for object communication.  Events exist only in code and are not specific to any object; the **update event** must be registered if an entity requires regular updates【681399795811306†screenshot】.

## 7 Next Steps

To continue your training:

1. **Explore the documentation** – Dive into the **Desktop Editor** section to learn about panels and tabs, performance analysis, gizmos, custom models and mobile/web deployment.
2. **Complete additional tutorials** – Build different types of games, experiment with NPCs and generative tools, and test cross‑platform performance.
3. **Join the community** – Participate in the Horizon Creator Program for access to monetization opportunities, workshops and a vibrant Discord community【936468813332520†screenshot】.

By following this guide and leveraging the official tutorials, you will become proficient in Horizon Worlds development and be well prepared to craft an engaging world for the Meta Horizon mobile competition.
