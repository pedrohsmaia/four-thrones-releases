# Demo walkthrough video: shot list and voiceover (1:40 to 1:55)

The handbook wants "a 1 to 2 minute walkthrough that takes the user inside your world
(not a trailer cut). Must include core feature demos; voiceover is recommended."
Record real play at 1920 x 1080, 60 fps (OBS, game capture), speak over it in one take.
No music is needed; the game's own sound is fine. Do not cut faster than three seconds
a shot: judges must see the features working, not a montage.

| Time | On screen | Voiceover (plain, first person) |
|---|---|---|
| 0:00 to 0:08 | Title screen over the live backdrop war; the version number bottom left. | "This is Four Thrones, a four-player free-for-all auto-battler. It is my gift for RTS and auto-battler fans." |
| 0:08 to 0:25 | Play > Match Setup. Click the faction button of seat 1 twice: the faction card beside the box changes (engine, heroes, unique unit, superweapon, troops). Pick bot difficulties. | "You build and upgrade; your army marches and fights on its own. Four factions, each with its own engine: here the card shows the passive, the three heroes, the unique unit and the superweapon." |
| 0:25 to 0:50 | Start. First minute of play: the base, the first wave leaving the barracks, upgrade a barracks, buy a tower perk, hover the fortress HP on the stat bar. | "Every match is a deterministic simulation: the same seed and the same commands give the same war, which is what lets replays, saves and multiplayer share one mechanism." |
| 0:50 to 1:10 | Hire a hero; cast a fortress spell on the lane; a hero skill goes off; the kill feed and the base scoreboard react. | "Heroes level in the lane. Fortress spells spend the fortress's own mana. Everything you see in the world was modelled with Tripo and painted in a hand-painted style, from the buildings to the units." |
| 1:10 to 1:25 | Fortress level 3; forge the superweapon; fire it on an enemy base; the announcement banner; a base falls. | "At fortress three each faction unlocks its superweapon. The Necrotide's Last Muster, the Emberlords' Inferno: match-ending if you time them." |
| 1:25 to 1:45 | Main menu > Multiplayer: the server list shows the official server online; Create Room (name, public or private with a password); in the room add two bots, set their factions; a friend joins (or show the seat list filling); Start. | "Multiplayer runs on a dedicated referee server: create a public or private room, add bots to the empty seats, invite friends with the room code, and the server runs the same simulation for everyone." |
| 1:45 to 1:55 | Back in the match, pull the camera out over the whole map, then the end screen (or a base elimination). | "Four thrones, one left standing. Thank you for playing." |

## Recording checklist

- Build 37 (the version shows on the title screen), fresh launch, 1920 x 1080 borderless.
- Settings: Interface scale 100%; camera speed 1.0.
- Have a second machine or a friend ready for the room shot; otherwise show the room
  with bots only and say so.
- Keep the cursor visible; it is the walkthrough's pointer.
- Export as MP4 (H.264, 1080p); the submission form takes a link, so upload to YouTube
  (unlisted) or Drive and paste the link.


## As produced, 2026-10-05: `hackathon/video/walkthrough.mp4` (1:45, 1920 x 1080, 30 fps, voiceover)

Not recorded by hand: the player records it. `FourThrones.exe -ft-walkthrough <dir>` (WalkthroughRecorder.cs)
plays the title over the backdrop war, the Multiplayer and Create Room screens, Match Setup with the faction
card changing, then a match with every seat a Hard bot while the camera follows a script: the base at 30
seconds, the first wave down the lane, the first hero (selected, its card on the bar), the fortress and its
spells, the superweapon (the runner's dev free-fire switch arms seat 0's so it fires on camera), and the
whole map from above. Frames are JPGs at 30 frames per second of game time; `make_walkthrough.py` lays the
seven voiceover lines (edge-tts, Christopher) at their shots and muxes the MP4. The game's own sound is not
in the video; the narration is the only audio.

| Shot | Time |
|---|---|
| title | 0.0 to 9.5 s |
| multiplayer | 9.5 to 18.5 s |
| createroom | 18.5 to 26.5 s |
| setup | 26.5 to 29.5 s |
| setup_cycle1 | 29.5 to 32.5 s |
| setup_cycle2 | 32.5 to 35.5 s |
| setup_cycle0 | 35.5 to 39.5 s |
| setup_diff | 39.5 to 41.5 s |
| base | 41.5 to 46.5 s |
| base_pan | 46.5 to 53.5 s |
| lane | 53.5 to 61.5 s |
| hero | 61.5 to 73.5 s |
| fortress | 73.5 to 81.5 s |
| super | 81.5 to 95.5 s |
| overview | 95.5 to 105.5 s |

| Line | Narration |
|---|---|
| title | This is Four Thrones, a four-player free-for-all auto-battler. My gift for RTS and auto-battler fans. |
| multiplayer | Play against bots, or online. Multiplayer runs on a dedicated referee server: create a public or private room, add bots to the empty seats, share the room code with friends, and the server runs the same simulation for everyone. |
| setup | In Match Setup you pick your faction and the bots' difficulty. Four factions, each with its own engine. The card shows the passive, the three heroes, the unique unit and the superweapon. |
| base | You build and upgrade; your army marches and fights on its own. Every match is one deterministic simulation: the same seed and the same commands give the same war, so replays, saves and multiplayer are one mechanism. |
| hero | Heroes are hired at the fortress and level up in the lane. Fortress spells spend the fortress's own mana. Everything in the world, from the buildings to the units, was modelled with Tripo and painted by hand. |
| super | At fortress level three each faction unlocks its superweapon. Time it right, and it ends a base. |
| overview | Four thrones on the corners of one map, one left standing. Thank you for playing. |
