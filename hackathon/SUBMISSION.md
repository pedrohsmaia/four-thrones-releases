# Submission package: Four Thrones for Tripothon S1

Where to submit: **https://activity.tripo3d.ai/en/submit** ("Submit / View Project" on the
event page). It needs a sign-in with the Tripo account (the one used on the Tripo API
platform), saves progress, and closes on **October 5, 23:59 AoE (UTC-12)**, which is October
6 at 08:59 in Brasilia. "Start Building" on the event page is the participation form
(https://tripo-ambassador.typeform.com/to/ScfyutRF?typeform-lang=en); do that first if it
was never done. The portal has five steps; every block below is named by the step it
belongs to.

## Decisions (taken 2026-10-04)

1. **The gift line** (Pedro: "rts and auto battlers fans, make this"):
   *A gift for RTS and auto-battler fans.* It is in the tagline, the description and the
   first sentence of the video. The title screen stays as it is (Pedro's choice).
2. **Hosting:** the source repository stays private (Pedro: "do not make the repo public in
   any hypothesis, only the release"). The public copy is the releases-only repository
   https://github.com/pedrohsmaia/four-thrones-releases: the package branch (this folder, no source) and
   release v0.1.0-build37 with the two zips. Nothing else goes there.
3. **The macOS build** ships as built; it has never run on a Mac. Pedro tests it once
   (`xattr -cr FourThrones.app` after unzipping) or the form says "built, untested".

## Step 1, Team

Team name: Four Thrones. Members: Pedro Maia (pedrohsmaia1@gmail.com), solo, team lead.

## Step 2, Project

**Project title:** Four Thrones

**Tagline (the portal allows 100 characters; this is 80):** Four-player free-for-all
auto-battler RTS. A gift for RTS and auto-battler fans.

**Direction track:** Games. **Tool tracks:** Tripo only.

**Team:** solo; team lead Pedro Maia (pedrohsmaia1@gmail.com).

**Description (the portal allows 2,000 characters; this is 1928):**

Four Thrones is a four-player free-for-all auto-battler RTS. Four thrones sit on the corners of one map, lanes run between them, and every wave your barracks raise marches down its lane and fights on its own. You never move a soldier. You decide what to build and upgrade, when to hire a hero, where to cast a fortress spell, and when to fire the superweapon that ends a base. Four factions play four different games: the Vanguard's siege charges, the Grove's seed-reviving elites, the Emberlords' buildings that strike back as they burn, the Necrotide's horde that grows from its own dead. Each has three heroes with ranked skills, two faction researches, a unique unit and a superweapon, and a faction card at match setup lays all of it out before you commit.

It is a gift for RTS and auto-battler fans: the people who love the build order, the timing, the counters and the nerve of a four-way free-for-all, and who would rather watch a plan unfold than click four hundred times a minute. The experience is a lobby filling up, a whole evening deciding who stands last, and the one moment when a superweapon lands and a throne falls.

Under the hood the match is one deterministic simulation that never touches the engine: the same seed and the same command log give the same war on any machine, which makes the replay, the save file and the multiplayer protocol one thing. Multiplayer runs on a dedicated referee server: create a public or private room, add bots to the empty seats, hand friends the room code. Bots come at four difficulties for solo play, and a build-time self-check runs the player and fails the build if the units do not draw.

The world was built with Tripo. Every faction building and every unit mesh came out of Tripo, from painted references in one hand-painted style, was rigged in Blender and baked to vertex-animation textures so a thousand soldiers draw in one pass. Playable on Windows and macOS.

## Step 3, Media and Demo

- **Cover:** `hackathon/cover.jpg` (1920 x 1080, 0.5 MB). The shipped models themselves, rendered from their VAT clip sets with the in-game material (Editor/CoverRender.cs, transparent background): Elderroot, the Ashcrown Pyre Titan mid-swing, the Cannon Siege Tower, the Blight Bombard, Aldric with the sword raised, Vulmar airborne; over the plaza render, with the title, the one-line pitch and the four crests (the gift line is not on the image, Pedro 2026-10-05; it stays in the tagline, the description and the video). Pedro's rule for this image: the units as they are in the game, not their paintings. Composed by `scratchpad/cover/make_cover_v3.py` (session scratch).
- **Visual asset board (the form takes 3 to 8, upload these 8 in this order):** every frame below is the real player mid-match (bases, towers, barracks, armies), captured through the build's own self-check camera at 1920 x 1080; the HUD stills are the Raven HUD over the Emberlords base.
  1. `hackathon/cover.jpg`: key art, the shipped models over the plaza (1920 x 1080).
  2. `hackathon/board/01_world_overview.jpg`: environment, the whole map at 90 seconds: four bases, the river, the harbour, the neutral sites, the first armies on the lanes.
  3. `hackathon/board/07_emberlords_base.jpg`: environment, the Emberlords base at gameplay zoom: fortress, two towers, three barracks.
  4. `hackathon/board/02_plaza_centre.jpg`: key frame, four armies clashing on the central plaza at two minutes.
  5. `hackathon/board/03_harbour.jpg`: environment, the harbour arm with the ship, the pier and a column marching past.
  6. `hackathon/board/10_hud_in_play.jpg`: key frame, the HUD in play over the base (bases panel, minimap, action bar).
  7. `hackathon/board/12_hud_hero_selected.jpg`: key frame, a hero selected: its card and the research in progress.
  8. `hackathon/board/06_units_multiview.jpg`: multi-view, the four unique units and four heroes from two angles, rendered from the shipped models (2560 x 2720, two units per row at full height).
  Spares in `hackathon/board/`: the south-west corner (a neutral site and a marching column), the south edge (a second base), the fortress selection, the scoreboard, the victory screen, the title screen. There are no turntable GIFs.
- **Video:** the walkthrough link [URL] (VIDEO_SCRIPT.md).
- **Demo:** the playable builds (Windows x64 and macOS zips):
  https://github.com/pedrohsmaia/four-thrones-releases/releases/tag/v0.1.0-build37
- Repository link, if the form offers one: https://github.com/pedrohsmaia/four-thrones-releases
  (optional).

## Step 4, Awards and Declarations

**Tool contributions (Tripo):** paste the short form from TRIPO_USAGE.md: "Tripo produced
every faction building and unit mesh in the game, through Unity's AI generators and the
Tripo API, from painted references; 65 further generations on October 3. The pipeline is
reference, Tripo mesh, retopology and texture, Blender rig, vertex-animation bake, in-game
review."

**Third-party disclosure (paste):**

> Engine: Unity 6 (URP). Tools: Blender; Tripo and Unity AI generators (all 3D meshes and
> textures under Resources/GenProps, outputs ours under Unity's AI terms); Uthana (motion
> generation); Mixamo (13 animation clips, Adobe's Mixamo license); image generation for
> the icons and reference paintings (Nano Banana Pro, FLUX Klein), with a procedural icon
> frame drawn in code. Purchased assets: the Raven MOBA UI kit (HUD and menus) and the
> water surface shader and material of Synty Studios' POLYGON Nature Biomes. Font: DejaVu
> Sans (free license). Audio: every sound effect is synthesized in-house with numpy (no music, no
> third-party audio). Claude Code was used as a coding assistant.

**Prior-work declaration (paste):**

> Four Thrones is a pre-existing project: development started on 2026-07-02, and by
> September 14 the deterministic simulation, the map, the four factions' basic units
> and buildings, the bot opponents and a first HUD existed. I declare it as secondary
> development. Everything below was built between September 15 and October 5, 2026
> (199 commits, listed in increment-commits.txt): the hero skill kits and the champion
> system (17 skills, ranked), the twelve fortress spells (three per faction), the
> Necrotide horde engine, the Raven HUD skin with the new action bar, tooltips and
> cards, the main menu, settings, match setup with the faction card, the rooms
> multiplayer on a dedicated EC2 referee server with a public server directory, the
> Windows and macOS builds with a build-time self-check, the FFA balance suite (over
> 10,000 simulated matches) and the adjusted balance patch of build 37, the unit and
> building regeneration with Tripo, and the Tripo studio batch of October 3. Open-source
> and AI tools used: Unity 6, Blender, Tripo, Unity AI generators, Uthana motion
> generation, Claude Code as a coding assistant.

**Rights:** accept (IP stays with the author; Tripo gets a non-exclusive promotional license).

## Step 5, Review

Run the checklist below, submit, and revise until the deadline if anything changes.

## Public build log post (optional, also the social media prize)

> Four Thrones for #Tripothon: a 4-player auto-battler RTS where every building and unit
> was made with @tripoai. Deterministic sim, dedicated servers, four factions. [gift
> line]. Build 37 is out: [link] (one screenshot of the plaza or the room screen)

## Checklist before pressing submit

- [ ] Participation form done; signed in at https://activity.tripo3d.ai/en/submit; Games track; tool track Tripo.
- [ ] The release published at its public home (never the source repository); the link opens in a private window.
- [ ] Video 1 to 2 minutes, uploaded, link works.
- [ ] Visual asset board: the eight images listed in the Media step, in that order (hackathon/board holds twelve stills; no GIFs).
- [ ] Secondary development declaration pasted.
- [x] Gift line in the tagline, the description and the video script.
- [ ] Submitted before October 5, 23:59 AoE (October 6, 08:59 in Brasilia); revise later if needed.
