# Wave Dash (Neon Waves): changes and ideas

All changes are local only in `index.html` (nothing pushed or committed).

## Controls
- Move **WASD / arrows** · Aim **mouse** · Shoot **hold left click** · Dash **Space / Shift**
- Ship ability **E / Q / right-click** · Pause **P / Esc** · Sound **M** · Music **N**
- Ship screen: **1/2/3** ship · **D** difficulty · **Tab** modifier · **Enter** launch · **Esc** back

## Round 6: WebGL (GPU) graphics
- The arena is now drawn with **WebGL via Three.js** (loaded from the jsDelivr CDN, version 0.160.0), so it runs on the graphics card.
- **Lighting and shadows:** a sun light casts soft shadows from ships, enemies and asteroids onto the arena; the ship carries its own colored light; big explosions flash light onto nearby objects.
- **3D models:** beveled metal ship hulls with glowing edges, a cockpit light and an engine flame; enemies are beveled 3D shapes with a bright core; asteroids are rough lit rocks.
- **Bloom glow** on bullets, lasers, cores and pickups; soft additive particles; parallax starfield over a painted nebula.
- HUD, damage numbers, telegraph lines and the crosshair stay on a crisp 2D layer on top.
- **Fallback:** press **G** to switch between 3D and the old 2D look (saved). If WebGL or the CDN isn't available (e.g. offline), the game automatically uses 2D.
- Needs an internet connection the first time for Three.js and fonts (the browser caches them).

## Round 5: simpler, fairer money, HUD outside the arena
**Money bug (the "interest" feeling):** Money Multiplier multiplied itself (x1.7 each time) and rerolls only cost +$10, so with Swarm (x1.5 money, x1.6 enemies) you could reroll and stack it until money exploded.
- Money Multiplier is now **Money Bonus**: adds +10–30%, capped at +60% total.
- Kills give **30% less money**; wave bonus lowered.
- Buying the **same upgrade again costs +30%** each time.
- **Reroll cost grows x1.6** each time in the same shop.
- Swarm and Easy no longer give extra money; Bullet Hell gives +25% (was +40%).
- **Interest:** if you leave the shop **without buying anything**, you get 10% of your money (max $20 + $5 per wave) at the end of the next wave. Buying even one item cancels it. The shop shows the amount.

**Simpler for new players:**
- Title screen: one **Play** button. Endless appears only after you finish the story.
- Ship screen: each card shows only HP and the E ability (passive is in the hover tooltip). Hard and the run modifiers stay hidden until unlocked.
- Shop: stats folded under "Your stats"; cards show "★ Unlocks synergy" when buying them completes one.
- Controls reminder at the bottom of the screen during waves 1–2 of your first run.

**HUD:** HP, money, dash, ability, wave and kills now sit in a bar **above** the arena, so they never cover the action.

**Also fixed:** shots now fire from the ship's center, so enemies right on top of you get hit.

## Round 4: maps
| Map | Hazard | Where |
|---|---|---|
| Neon Void | None | Story waves 1-5 |
| Asteroid Field | 7 random rocks block shots (yours and theirs) and movement | Story waves 6-10 |
| Lava Grid | Random tiles flash for 1.5s, then burn for ~3s | Story waves 11-15 |
| Blackout | You only see near your ship; enemies show a faint glow | Story waves 16-20 |
| Collapsing Arena | Safe circle shrinks during each wave, grows back between waves | Endless only |
| Warp Loop | Fly off one edge, come out the other side | Endless only |

- Endless picks a **random new map every 5 waves** (never the same twice in a row).
- The map name shows under the wave counter, and a banner explains it when it changes.

## How the randomness works
- **No seed:** the game uses the browser's random numbers, so every run is different.
- **Enemy count** per wave is fixed (about 6 + 3 per wave, more after wave 8, times difficulty and modifier).
- **Enemy types** are rolled from a weighted table: new types join at set waves and their weight grows each wave. Bosses are fixed every 5th wave.
- **Spawns** come from a random spot on a random screen edge.
- **Shop cards:** rarity is rolled first (common gets rarer and legendary more likely each wave), then a random upgrade you can still use at that rarity, with no duplicates. The first shop always offers Auto Fire.
- **Drops:** 4% of kills drop a heal orb; a health pack appears at a random spot every 10s (max 2).
- **Small timers** are randomized too: dasher charges, blinker teleport spots, crit rolls, asteroid layout and lava tiles.

## Round 3: modes, difficulty, cinematics, graphics, sound
1. **Story mode**: 20 waves, a boss every 5 waves (Overmind, Laser Warden, Hive Queen, Neon Tyrant).
2. **Victory screen** after wave 20: continue this run in **Endless**, start a **new game one difficulty higher**, or go to the menu.
3. **Endless mode** in the main menu, unlocked after finishing the story once (any difficulty).
4. **3 difficulties**: Easy, Normal, Hard. **Hard unlocks after finishing the story on Normal.**
5. **New final boss, Neon Tyrant**: sweeping lasers, full bullet rings and dasher/exploder reinforcements.
6. **Wave-finish cinematic**: letterbox bars, "Wave X cleared" / "Boss defeated", money and kills earned, fireworks. Lasts about 2.5s (4s after bosses).
7. **Shop click lock**: for 1 second after the shop opens, clicks and keys are ignored (shop shows greyed out), so you can't buy or skip by accident.
8. **Graphics**: canvas renders at screen pixel density (sharp, not pixelated), removed scanline overlay, soft glowing round particles and stars, neon double-stroke enemies, gradient ships, soft thruster flame, rounded HP bars, Orbitron title font, blurred glass menus with fade-in.
9. **Sound**: softer synth sounds routed through a filter, echo and compressor; noise-based explosions; chords for wave clear, boss defeat, synergies and victory; UI clicks; **background music** (synthwave loop that gets faster and darker during boss fights).

Unlock progress is saved in the browser (`localStorage`).

## Round 2: ships, content, balance
- **3 ships** with passive + active abilities: Striker (Bullet Storm), Phantom (Phase Blink), Bulwark (Aegis).
- **New enemies**: Splitter, Splitling, Shielded, Healer, Blinker.
- **New upgrades**: Ricochet, Homing, Critical Hits, Lifesteal, Dash Strike, Frost Shots.
- **5 synergies**: Railgun, Smart Rounds, Cryo Pulse, Blood Crits, Blade Dancer.
- **Run modifiers**: Swarm, Glass Cannon, Bullet Hell.
- **Balance**: Dash upgrade capped, shorter dash shield, exploders don't pay when they blow up on you, dash toward cursor when standing still.
- Stats panel in the shop; best wave / kills / time saved.

## Round 1: bug fixes
1. Translated everything to English (left-to-right layout).
2. Boss minions spawn at the boss.
3. Health packs aren't wasted at full HP.
4. End-of-wave magnet only pulls drops.
5. Space/Enter can't restart a run from a focused button.
6. Firing can't get stuck on.
7. Fallback for older Safari (`roundRect`).

## Tested
- Scripted run of the full 20-wave story on Normal: all 4 bosses, the cinematics, the victory screen, Endless and Hard unlocks, and continuing into wave 21+ in Endless. No console errors.

## Ideas for later
- **Maps** (pick per run or rotate per boss chapter):
  - Asteroid field with rocks that block shots.
  - Shrinking arena.
  - Wrap-around edges.
  - Lava grid with damaging tiles that move each wave.
  - Dark map where you only see around your ship.
- **Story flavour**: short text intro before each boss chapter; each chapter (5 waves) uses its own map and color theme.
- **Elite enemies**: rare tougher variant that drops a free upgrade.
- **Mid-wave events**: meteor shower, gold rush (double money).
- **Meta progression**: permanent currency to unlock ship skins or a 4th ship.
- **Touch controls** for phones (virtual joystick + buttons).
- **Settings menu**: volume sliders, screen shake on/off.
- **Daily challenge** with a fixed seed and a local leaderboard.
