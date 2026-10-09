# Changelog

All notable changes to **Neon Waves** (repo: `wave-dash`).
All changes so far are **local only** (`C:\temp\wave-dash`), not committed or pushed.

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
