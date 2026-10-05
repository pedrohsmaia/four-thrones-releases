# Tripo in Four Thrones: the tool-track evidence

Written 2026-10-04 for the Tripothon S1 submission (tool track: Tripo). The handbook
disqualifies a tool-track entry that did not actually use the tool; this file lists where
Tripo sits in the pipeline and which shipped assets came out of it.

## The pipeline

1. **Reference art first.** Every asset starts as a painted reference in the project's hand-painted
   style (the style contract lives in `.claude/skills/gen-prop/WOTLK-STYLE.md`; the icon kit and the
   accepted reference sidecars define silhouette, palette and QC). Pedro approves the reference on the
   8777 Approvals board before any generation.
2. **Tripo makes the mesh.** Two routes, both Tripo models: Unity's AI generators (`com.unity.ai.generators`,
   "Tripo" mesh, retopology and texture jobs from inside the Editor) and the Tripo API through the
   authenticated `tripo` CLI (`image-to-model`, multiview front and rear references, polycount targets;
   `docs/ART_WORKFLOW.md` "Direct Tripo API through the existing CLI"). Request logs with task ids sit in
   `ArtSource/<batch>/request.json`.
3. **Blender rigs and animates** (`Tools/blender_rig_import.py`, the Uthana motion generator for walks and attacks),
   then the Editor bakes vertex-animation textures (`Assets/_Project/VAT`) so thousands of units draw in one
   instanced pass. Buildings skip the rig and go straight to prefabs under `Resources/GenProps`.
4. **Review in the game, not in a viewer.** Every result is rendered in the match camera and judged on the
   Approvals board; rejected results are regenerated with changed references.

## Shipped assets whose provenance names Tripo

Counted by searching the shipped `Resources/GenProps` prefabs, meshes and materials for the generator name
(Tripo node names and texture names survive in the imported GLB and prefab data).

**Buildings (12, the four factions' barracks, fortress and tower):** bld_ember_wotlk_barracks, bld_ember_wotlk_fortress, bld_ember_wotlk_tower, bld_grove_wotlk_barracks, bld_grove_wotlk_fortress, bld_grove_wotlk_tower, bld_necrotide_wotlk_barracks, bld_necrotide_wotlk_fortress, bld_necrotide_wotlk_tower, bld_vanguard_wotlk_barracks, bld_vanguard_wotlk_fortress, bld_vanguard_wotlk_tower

**Unit families (33; each a prefab plus avatar, material and skin assets, baked to vertex animation):** unit_ember_assassin, unit_ember_assassin_tripo, unit_ember_caster, unit_ember_champion, unit_ember_flyer, unit_ember_melee, unit_ember_ranged, unit_ember_siege, unit_ember_tank, unit_grove_assassin, unit_grove_caster, unit_grove_champion, unit_grove_flyer, unit_grove_melee, unit_grove_ranged, unit_grove_siege, unit_grove_warlord, unit_necrotide_assassin, unit_necrotide_caster, unit_necrotide_champion, unit_necrotide_flyer, unit_necrotide_melee, unit_necrotide_ranged, unit_necrotide_siege, unit_necrotide_tank, unit_special_grove, unit_vanguard_assassin, unit_vanguard_caster, unit_vanguard_champion, unit_vanguard_flyer, unit_vanguard_melee, unit_vanguard_ranged, unit_vanguard_tank

**Other:** FortressSpellsR2

## Generation batches during the competition window (September 15 to October 5)

`ArtSource` folders whose request logs, scripts or notes name Tripo, with the number of such files:

- `Animations`: 8
- `ApprovalRevisions20260916`: 3
- `ChampionSkills20260920`: 1
- `EmberfallAndScoreboard20260915`: 3
- `FortressSpells20260927`: 1
- `FortressSpells20260927R2`: 9
- `FortressSpells20260927R3`: 1
- `GroveBalance20260926`: 3
- `HeroSkills20260914`: 3
- `NecrotideProduction20260922`: 8
- `SkorveBow20260922`: 1
- `UnitPolish20260916`: 15
- `Units`: 2

**The studio batch of 2026-10-03** (`docs/TRIPO_BATCH_2026-10-03.json`): 65 image-to-model generations at
studio.tripo3d.ai from the approved reference images, 3200 credits down to 0 in one day,
"buildings first, then props, then units" on Pedro's order; the next step is bringing the best of them
through the rig and bake above.

- buildings (12): bld_ember_wotlk_barracks, bld_ember_wotlk_fortress, bld_ember_wotlk_tower, bld_grove_wotlk_barracks, bld_grove_wotlk_fortress, bld_grove_wotlk_tower, bld_necrotide_wotlk_barracks, bld_necrotide_wotlk_fortress, bld_necrotide_wotlk_tower, bld_vanguard_wotlk_barracks, bld_vanguard_wotlk_fortress, bld_vanguard_wotlk_tower
- props (29): env_bld_alchemist, env_bld_armory, env_bld_farm, env_bld_gold_mine, env_bld_war_camp, env_throne, env_stone_bridge, env_dock, env_pier, env_crane, env_port_cargo, env_bld_blacksmith, env_bld_mana_well, env_bld_market, env_bld_obelisk, env_bld_sawmill, env_bld_shrine, env_bld_watchtower, env_bld_armory, env_berm_rock, env_cliff_corner, env_cliff_wall, env_dock_stairs, env_ford_boulders, env_plaza_pillar, env_prop_ore_cart, env_tree_broadleaf, env_tree_conifer, env_tree_dead
- units (24): unit_ember_assassin, unit_ember_caster, unit_ember_champion, unit_ember_tank, unit_grove_caster, unit_grove_champion, unit_grove_warlord, unit_necrotide_assassin, unit_necrotide_caster, unit_necrotide_champion, unit_necrotide_tank, unit_vanguard_assassin, unit_vanguard_caster, unit_vanguard_champion, unit_vanguard_tank, unit_ember_melee, unit_ember_ranged, unit_grove_melee, unit_grove_ranged, unit_necrotide_melee, unit_necrotide_ranged, unit_vanguard_melee, unit_vanguard_ranged, unit_special_vanguard

## What to claim on the form

- Tool track: Tripo. Inventive use: a full production pipeline (reference to mesh to retopology to texture
  to a vertex-animation bake), not single props. Tool synergy: Unity AI generators, the Tripo API, Blender,
  Uthana motion. Contribution: every faction building and unit in the world.
- Do not select PICO, Heygears or World Labs: the project did not use them.
