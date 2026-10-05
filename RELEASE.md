## Four Thrones, build 37: the Tripothon S1 entry

A four-player free-for-all auto-battler RTS in the Survival Chaos lineage: you build and upgrade, your army marches and fights on its own. Four factions with their own engines, three heroes each, a unique unit per faction, fortress spells, superweapons, bots at four difficulties, sound effects, and online rooms on a dedicated server. A gift for RTS and auto-battler fans.

### Downloads

- **Windows x64**: unzip `FourThrones-build37-Windows-x64.zip`, run `FourThrones/FourThrones.exe`. This build passed its own self-check (the player starts a match, units load and draw) before it was published.
- **macOS (Universal)**: unzip `FourThrones-build37-macOS-universal.zip`, then in Terminal run `xattr -cr FourThrones.app` once (the app is unsigned) and open it. Built on Windows with the Mac Build Support module; not yet verified on a Mac.

### Playing

- **Play** opens Match Setup: click a faction button to cycle factions; the card beside the box shows that faction's engine, heroes, unique unit, superweapon, researches and troops. Set the bots' difficulties and start.
- **Multiplayer** lists the official server when it is online. Create a public room, or a private one with a password, add bots to empty seats, share the room code with friends, and start when everyone is ready.
- Hover anything in the HUD for its card; hold Shift for the formulas.

### What is in this repository

The game's full source history is kept privately. This repository carries the release package only: these notes and `hackathon/` (the submission texts, the conformity check against the handbook, the Tripo usage evidence, the walkthrough script and the list of the commits that make up the hackathon increment).

### Third-party content, declared

Unit, building and prop meshes generated with Tripo (through Unity's AI generators and the Tripo API) from our own painted references; icons generated in a hand-painted style with our own frame compositor; thirteen Mixamo animation clips; the Raven MOBA UI kit (purchased) for the HUD; DejaVu Sans; the sound effects are synthesized by our own scripts. No Synty assets ship in this build.
