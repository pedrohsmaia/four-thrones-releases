# Conformity check: Four Thrones against the Tripothon S1 rules

Checked on 2026-10-04 against hackathon/HANDBOOK.md (handbook of September 30 and the
official site). Verdict first: **Four Thrones is eligible as a Games-track entry, with
Tripo as its tool track, provided the submission declares the project as secondary
development and ships the three deliverables by October 5.** Nothing in the rules
blocks it; two things decide how it scores: the declared "work increment" (judges score
only that) and the "A Gift for ______" framing (20% of the direction score, 10% of the
tool score).

## Requirement by requirement

| # | Rule (source) | Four Thrones | Status | Who does what |
|---|---|---|---|---|
| 1 | Registered on the official website; one direction track; team lead submits (2.3, 3.2) | Solo entry; Pedro is the team lead | **Open** | Pedro: "Start Building" on developers.tripo3d.ai/en/events/tripothon-s1 (the participation form), then "Submit / View Project" (https://activity.tripo3d.ai/en/submit, Tripo account sign-in), Games track, tool track Tripo |
| 2 | Direction track fit: Games, "story-driven / interactive puzzle / emotional experiences" (handbook), "playable worlds, mechanics, narrative systems, AI-assisted game development" (site) | A playable 4-player free-for-all auto-battler RTS with four factions, bots and online rooms: squarely "playable worlds, mechanics"; the emotional side comes from the gift framing | OK | SUBMISSION.md gives the framing |
| 3 | Tool track only if the tool was actually used; disqualified from that track otherwise (2.2, 8.2) | Tripo generated the twelve faction buildings, the unit meshes of all four factions and the fortress-spell props, through Unity's AI generators and the Tripo API, between September 14 and October 3 (TRIPO_USAGE.md). PICO, Heygears and World Labs: not used | OK for Tripo only | Select Tripo; do not select the other three |
| 4 | Theme "A Gift for ______" (1.1; 20% of the score) | Not stated anywhere in the game or the docs yet | **Open** | Pedro picks the gift line (three proposals in SUBMISSION.md); optionally a one-line dedication on the title screen |
| 5 | Deliverable: complete playable demo, "Web / H5 / App / executable" (3.1) | Windows x64 and macOS Universal players, build 37; Windows passes the build self-check (units load and draw); macOS built from Windows, unsigned (`xattr -cr` needed), untested on a Mac | **Met** (hosting decided) | The source repository stays private; the zips are release v0.1.0-build37 of the releases-only public repository https://github.com/pedrohsmaia/four-thrones-releases; test the Mac build once |
| 6 | Deliverable: 1 to 2 minute walkthrough video, inside the world, core features, not a trailer; voiceover recommended (3.1) | Not recorded | **Open** | Pedro records; VIDEO_SCRIPT.md has the shot list and the voiceover |
| 7 | Deliverable: visual asset board, 3+ high-res screenshots or GIFs: key stills, multi-view turnarounds, environment frames (3.1) | hackathon/board/: world overview, plaza, harbour, corner and edge frames, the HUD in play, selections, scoreboard, title; no unit turnarounds yet | Mostly done | Add a unit turnaround sheet if time allows (Gallery scene); otherwise the stills satisfy "3+" |
| 8 | Optional public build log on social media; bonus consideration; #Tripothon and @tripoai (3.1, 4.5) | None posted | Optional | One post with the plaza render and the room screen would do |
| 9 | Revisions allowed until the deadline; the final version is judged (8.5) | | OK | Submit early on October 4 or 5, revise if the Mac build changes |
| 10 | Team of 1 to 3; solo welcome (2.3, 8.3) | Solo | OK | |
| 11 | Code of conduct: respect originality; "core business logic and asset integration must be completed during the competition period" (7.1) | The sim, the factions and most art predate September 15 (the project started on 2026-07-02). Allowed under 7.2 as secondary development, which must be declared | OK with the declaration | SUBMISSION.md carries the declaration |
| 12 | Secondary development: declare the foundation and the new additions; judges score only the increment; false declaration disqualifies (7.2) | Foundation: everything up to September 14. Increment since September 15: 199 commits (increment-commits.txt): hero skill kits and the champion system, fortress spell kits, the Raven HUD skin and the action bar, the main menu, settings and match setup, rooms multiplayer on a dedicated EC2 referee with a public server directory, the player builds with a build-time self-check, the FFA balance suite and the adjusted patch (build 37), the Tripo unit and building regeneration, the faction card | OK | Paste the declaration from SUBMISSION.md; keep increment-commits.txt as evidence |
| 13 | IP: rights stay with the author; Tripo gets a free non-exclusive promotional license (7.3) | Pedro owns the game | Pedro's call | Accept by submitting |
| 14 | AIGC: no unauthorized media (7.3) | 3D: Tripo and Unity AI generators (paid, licensed). Icons: generated, composited in a bought icon frame kit. HUD: the bought Raven MOBA UI kit. Environment: bought Synty packs plus generated props. Fonts: project fonts. Audio: no audio assets in the project | OK; confirm two licenses | Pedro: confirm the icon kit and the Raven UI kit licenses allow redistribution inside a game build (they are standard Asset Store or marketplace purchases, which do) |
| 15 | Prohibited content (7.3) | Fantasy war, no real-world targets | OK | |
| 16 | Deadline: online submissions close October 5, late entries rejected (1.2) | The portal states October 5, 23:59 AoE (UTC-12): October 6, 11:59 UTC, 08:59 in Brasilia | **Hard** | Submit on October 5; the portal saves progress, so start the form early and revise |

## How the judging criteria read against the project

- **Creativity 30%.** The pitch: an auto-battler RTS in the Survival Chaos lineage,
  rebuilt as a pure deterministic simulation, where one command log is the replay, the
  save and the multiplayer protocol; four factions with engines rather than stat bumps;
  a world whose buildings and units were generated with Tripo in one hand-painted
  style. Say this plainly in the description.
- **Completeness 25%.** The loop is complete: title, setup with the faction card, a
  full match against bots with heroes, spells, towers and superweapons, elimination
  and victory, plus online rooms. The Windows build verifies itself at build time. The
  weak spot is the untested macOS build: test it or ship Windows only.
- **Theme alignment 20%.** Decided by the gift line and whether the game shows it. A
  dedication on the title screen and the first sentence of the video carry it.
- **Viral potential 15%.** Superweapon moments and the four-way free-for-all are the
  clips; the build log post is the cheapest way to earn this.
- **Commercial value 10%.** A finished indie RTS with dedicated servers; say what comes
  next (ranked rooms, more factions, Steam).
- **Tool track (Tripo).** Inventive use 35%: Tripo as a production pipeline (reference
  art to mesh to retopology to texture to a vertex-animation bake), not single props;
  synergy 25%: Unity AI generators, the Tripo API, Blender rigging, Uthana motion;
  contribution 20%: every faction building and unit; theme 10%; breakout 10%.

## Gaps that the submission must not hide

1. The project predates the hackathon by ten weeks. Declare it (12); the increment is
   large and real, so this costs nothing beyond honesty.
2. The macOS build has never run on a Mac. Either Pedro tests it on his Mac before
   submitting or the submission lists Windows as the playable build and macOS as
   "built, untested".
3. The game has no in-game statement of the gift yet. A one-line dedication on the
   title screen is a ten-minute change if Pedro wants it in the build.
