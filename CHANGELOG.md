# Changelog

All notable changes to **Neon Waves** (repo: `wave-dash`).

## [2.6.0] - 2026-10-10 - Difficulty curve, distinct bosses, meta progression
### Changed
- **Difficulty curve follows progress:** enemy HP ramps gently in waves 1–9 and steeper later; damage taken uses a gentler early exponent and a steeper late one.
- **Endless gets really hard:** extra enemy HP multiplier past wave 20, faster spawning and airstrikes, and bosses gain HP, bullet damage, extra beams/minions per cycle.
- **Bosses feel different:** Overmind sprays many weak bullets and chasers; Laser Warden is slower with longer telegraphs but deadly beams (nerfed: weaker beams/shots, less contact damage and HP); Hive Queen fires faster weak spirals with bigger swarms; Neon Tyrant hits hardest (stronger rings, shots and beams, more HP).
### Added
- **Meta progression (first step):** every run earns permanent ✦ shards (more for waves, kills, bosses and victories, scaled by difficulty). Spend them on end-of-run screens on visual-only ship skins and tiny permanent perks (+max HP, +speed, +starting money, max 3 levels each). No new ships or modifiers, prices keep it slow.
### Changed
- **Easy is easier, Normal slightly softer:** Easy enemies have less HP, deal less damage, come in smaller waves and fire slower (+10% money kept). Normal is ~5% softer.
- **No black screen between waves:** the wave-clear cinematic is skipped, the shop opens instantly with a transparent overlay and only a 0.3s click lock; next wave starts ~0.4s after leaving the shop.
- **Heal packs:** green packs heal 10 (was 5), max 4 per wave and 2 on screen.
- **Run modifiers always visible** (no story unlock needed); Swarm is 40% more enemies with +20% money; Bullet Hell is +15% money (was +25%).
- **Less ship glow:** flatter ship cards, smaller in-game aura and engine flame, dimmer 3D edges and halo; Hard lock tooltip is fully opaque.
### Fixed
- Holding the mouse now keeps firing across waves, shops and boss cinematics.

## [2.5.0] - 2026-10-09 - Bigger arena, elites, drones
### Changed
- **Arena enlarged** from 960×600 to 1200×750 (about 56% more space). The view zooms out to fit; the HUD keeps its layout. Asteroid Field now has 10 rocks, and the Collapsing Arena starts and ends larger.
- **Elites are easy to spot and dangerous:** at least one in every normal wave from wave 3 (about 2 per 50 enemies), 65% bigger, pulsing gold aura, dashed gold ring, "ELITE" tag, and a gold halo in 3D. Contact damage doubled; elite gunners fire bigger gold shots that hit harder.
- **Orbiting Blade → Orbiting Drones:** the drones now look like small drones and also **destroy enemy shots** that touch them.
- Banner text is larger to match the bigger arena.
### Fixed
- The weakest enemies (Chasers and Splitlings) now show a health bar when damaged, like all other enemies.

## [2.4.0] - 2026-10-09 - Boss phase cinematics and damaged forms
### Added
- **Phase-change cinematic** (about 2.3 s, skippable after a moment with Space/click): the game pauses, the camera zooms on the boss, it shakes and sparks under a "⚠ CORE UNSTABLE ⚠" warning, then bursts into its new form with a shockwave and the phase name.
- **Damaged boss forms** in 3D and 2D: bosses are built from an inner housing plus a ring of armor plates. Plates break off and fly away as debris at each phase (25% / 50% / 75% gone), glowing cracks spread, the core grows and heats up (white → orange → white-hot), and a red aura pulses in the last stand.
- **New guns per phase:** 2, then 4, then 6 rotating gun barrels appear on the boss.
### Changed
- Phase effects (Hive Queen guards, Neon Tyrant teleport) now happen at the moment of transformation.

## [2.3.2] - 2026-10-09 - Locked Hard option
### Changed
- **Hard** is always shown on the ship screen. While locked it is greyed out with a 🔒, can't be selected, and hovering it shows "You must finish the game on Normal difficulty".

## [2.3.1] - 2026-10-09 - Polish
### Fixed
- **Flicker on normal kills:** the kill screen-shake moved the camera so the glowing arena border slid in and out of view, which looked like the lights flickering. Normal kills no longer shake the screen; elites and bosses still do. The border now sits slightly inside the arena so shakes can't hide it.
- Title menu labels now line up (icons sit in a fixed-width column).
### Changed
- Normal kills show a local "pop" instead: an expanding ring in the enemy's color plus white sparks.
- Hit flash on enemies is softer, so the screen doesn't pulse brighter on every hit.
- Health packs glow much less.

## [2.3.0] - 2026-10-09 - Title menu and settings
### Added
- **Main menu** on the title screen: Start Game, Endless (once unlocked), Achievements, Settings, Exit Game.
- **Settings screen:** sound on/off, effects volume, music on/off, music volume, screen shake, graphics 3D/2D. All saved.
- **Exit Game:** closes the window when the browser allows it, otherwise shows a "Thanks for playing" screen.
- **Version number** (`Neon Waves v2.3.0`) at the bottom of the title screen only.
### Changed
- Achievements and Enemy Codex now share one screen with two tabs.

## [2.2.0] - 2026-10-09 - Bosses, elites, juice and goals
### Added
- **Boss phases** at 70%, 40% and 10% HP for all 4 bosses, each with new attacks (faster rings, more beams, royal guards, bullet streams, Tyrant teleports). A big hit can't skip a phase; a short invulnerable moment and a "Phase 2 / Phase 3 / Last Stand" banner mark each change. Ticks on the HUD boss bar show the thresholds.
- **Elite enemies** in normal waves (about 2 per 50 enemies, from wave 3, never in boss waves): 2.6x HP, bigger, gold ring and ★, +50% contact damage, 1.6x money. Elite gunners fire 3-way shots; elite splitters split into 3.
- **Cinematic boss intro:** letterbox, warning, camera zoom on the boss, name and subtitle, music dips. Space/click skips.
- **Visual juice:** screen shake scales with what exploded; brief hit-stop on elite kills, boss phases and boss kills; soft flash on critical hits; WebGL shockwave ripple with color split around big explosions.
- **Achievements** (17, saved forever) with a list screen on the title.
- **Run rating** Bronze, Silver, Gold, S, SS, SSS from progress, damage taken, accuracy and speed, shown on victory and death screens.
- **Secret medals** (9 hidden goals inside a run), shown as toasts and on the end screen.
- **Enemy Codex:** each enemy unlocks an entry (what it does, strength, how to beat it, times defeated) once defeated.
- **K** toggles screen shake.

## [2.0.0] - 2026-10-09 - GPU graphics
### Added
- WebGL renderer (Three.js 0.160.0 from the jsDelivr CDN), so the game draws on the graphics card.
- Sun light with soft shadows from ships, enemies and asteroids; the ship carries its own colored light; big explosions flash light.
- 3D models: beveled metal ship hulls with glowing edges, cockpit light and engine flame; 3D enemy shapes with bright cores; rough lit asteroids.
- Bloom glow on shots, lasers and pickups; additive particles; parallax starfield over a painted nebula.
- **G** switches between 3D and the classic 2D look (saved).
### Changed
- HUD, damage numbers, danger markers and crosshair are drawn on a 2D layer on top of the 3D arena.
### Fixed
- Arena border no longer blooms into a bright haze over the whole screen.
### Notes
- The game falls back to 2D automatically if WebGL or the CDN isn't available (e.g. offline).

## [1.4.0] - 2026-10-09 - Simpler game, fair money, HUD bar
### Fixed
- **Money exploit:** Money Multiplier multiplied itself and rerolls were cheap, so money grew without limit (worst in Swarm).
- Shots fire from the ship's center, so enemies on top of you get hit.
### Changed
- Money Multiplier became **Money Bonus**: +10–30% per buy, capped at +60% total.
- Kills give 30% less money; wave-clear bonus lowered.
- Buying the same upgrade again costs +30% each time; reroll cost grows x1.6 per reroll.
- Swarm and Easy no longer give extra money; Bullet Hell gives +25% (was +40%).
- HUD (HP, money, dash, ability, wave, kills) moved to a bar **above** the arena.
- Title screen has one **Play** button; Endless appears only after finishing the story.
- Ship cards show only HP and the E ability (passive in the tooltip).
- Hard and run modifiers stay hidden until unlocked.
- Shop stats folded under "Your stats".
### Added
- **Interest:** leave the shop without buying anything to earn 10% of your money (max $20 + $5 per wave) at the end of the next wave.
- Shop cards show "★ Unlocks synergy" when buying them completes one.
- Controls reminder during waves 1–2 of a first run.

## [1.3.0] - 2026-10-09 - Maps
### Added
- 6 maps: Neon Void, Asteroid Field (rocks block shots and movement), Lava Grid (tiles flash then burn), Collapsing Arena (safe zone shrinks), Warp Loop (edges wrap), Blackout (only see near your ship).
- Story uses one map per 5-wave chapter (Void, Asteroids, Lava, Blackout); Endless picks a random new map every 5 waves.
- Map name in the HUD and a banner explaining each new map.

## [1.2.0] - 2026-10-09 - Story, Endless, difficulty, polish
### Added
- **Story mode:** 20 waves, a boss every 5 waves.
- New final boss **Neon Tyrant** (lasers, bullet rings, reinforcements).
- Victory screen: continue in Endless, start a new game one difficulty higher, or main menu.
- **Endless mode**, unlocked after finishing the story once.
- **3 difficulties:** Easy, Normal, Hard (Hard unlocks after finishing the story on Normal).
- Wave-clear cinematic (letterbox, fireworks, wave summary) and a 1-second shop click lock.
- New sound design (filter, echo, compressor, noise explosions, chords) and generative background music; **M** mutes, **N** toggles music.
### Changed
- Sharper rendering at screen pixel density; removed scanlines; soft glowing particles and stars; neon outlines; gradient ships; Orbitron title font; glass-style menus.

## [1.1.0] - 2026-10-09 - Ships, content, balance
### Added
- 3 ships, each with a passive and an active ability (E / right-click): Striker (Bullet Storm), Phantom (Phase Blink), Bulwark (Aegis).
- 5 new enemies: Splitter, Splitling, Shielded, Healer, Blinker.
- 2 new bosses: Laser Warden, Hive Queen.
- 6 new upgrades: Ricochet, Homing, Critical Hits, Lifesteal, Dash Strike, Frost Shots.
- 5 synergies: Railgun, Smart Rounds, Cryo Pulse, Blood Crits, Blade Dancer.
- 3 run modifiers: Swarm, Glass Cannon, Bullet Hell.
- Stats panel in the shop; best wave, kills and time saved.
### Changed
- Dash upgrade capped and dash shield shortened.
- Exploders no longer pay money when they blow up on you.
- Dashing while standing still goes toward the cursor.

## [1.0.0] - 2026-10-09 - Bug fixes and English
### Changed
- Translated all text and comments from Hebrew to English; page is now left-to-right.
### Fixed
- Boss minions now spawn at the boss.
- Health packs are no longer wasted at full HP.
- End-of-wave magnet only pulls drops, not health packs.
- Space/Enter can't restart a run from a focused button.
- Firing can't get stuck on after an interrupted touch.
- Fallback for browsers without canvas `roundRect` (older Safari).

## [0.1.0] - Original
- Single-file Hebrew canvas game: waves, one ship, shop upgrades, one boss.
