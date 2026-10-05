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


## As produced, 2026-10-05 (second cut): `hackathon/video/walkthrough.mp4` (1:51, 1920 x 1080, 30 fps, voiceover)

Pedro's notes on the first cut: no multiplayer section, no "deterministic simulation" line, and no
"hand-painted" claim (the textures come from Nano Banana); after the factions, explain how the game
works in simple words: the map and the bases, the win condition, upgrades, units and heroes.

Not recorded by hand: the player records it. `FourThrones.exe -ft-walkthrough <dir>` (WalkthroughRecorder.cs)
plays the title over the backdrop war and Match Setup with the faction card changing, then starts a match
with every seat a Hard bot while the camera follows a script: the whole map from above, down into the
player's base, the fortress and barracks cards, the first wave down the lane, the first hero (selected),
the superweapon (the runner's dev free-fire switch arms seat 0's so it fires on camera), and the map from
above again. Frames are JPGs at 30 frames per second of game time; `make_walkthrough.py` lays the nine
voiceover lines (edge-tts, Christopher) at their shots and muxes the MP4. The game's own sound is not in the
video; the narration is the only audio.

| Shot | Time |
|---|---|
| title | 0.0 to 9.0 s |
| setup | 9.0 to 12.0 s |
| setup_cycle1 | 12.0 to 15.0 s |
| setup_cycle2 | 15.0 to 18.0 s |
| setup_cycle0 | 18.0 to 21.0 s |
| setup_diff | 21.0 to 23.0 s |
| map | 23.0 to 35.0 s |
| base | 35.0 to 49.0 s |
| upgrades_fortress | 49.0 to 55.0 s |
| upgrades_barracks | 55.0 to 61.0 s |
| lane | 61.0 to 73.0 s |
| hero | 73.0 to 85.0 s |
| super | 85.0 to 99.0 s |
| end | 99.0 to 110.0 s |

| Line | Narration |
|---|---|
| title | This is Four Thrones, a four-player free-for-all auto-battler. My gift for RTS and auto-battler fans. |
| setup | In Match Setup you pick your faction and the bots' difficulty. Four factions, each with its own engine. The card shows the passive, the three heroes, the unique unit and the superweapon. |
| map | Four thrones, one on each corner. Lanes connect them through the plaza in the middle. Destroy the other three fortresses, and the last throne standing wins. |
| base | This is your base: the fortress in the middle, the barracks around it, towers on the flanks. Gold comes in over time; what you upgrade, and when, is the whole game. |
| upgrades | Upgrade a barracks and its waves get stronger. Upgrade the fortress and it unlocks higher barracks levels, your unique unit, and at level three, the superweapon. |
| lane | The barracks send their waves down the lanes on their own. There is no micro: the army does the fighting while you build. |
| hero | Heroes are hired at the fortress. They walk the lanes, level up and cast their skills. Lose one, and it comes back after a while. |
| super | Each faction also has a unique unit and a superweapon. Time the superweapon right, and it ends a base. |
| end | Buildings, units and props were modelled with Tripo and textured with Nano Banana. Four thrones, one left standing. Thank you for playing. |
