# Roadmap

Where **Neon Waves** is going. Status: ✅ done · 🔜 next · 💡 later.
Full history is in [CHANGELOG.md](CHANGELOG.md).

## ✅ Done (v1.0 – v2.2)
- English translation and bug fixes
- 3 ships with passive + active abilities
- 10 enemy types, 4 bosses, 21 upgrades, 5 synergies, 3 run modifiers
- Story (20 waves) + Endless, 3 difficulties with unlocks
- 6 maps with hazards
- Wave-clear cinematics, sound effects and music
- Fair economy (capped bonus, interest only when you skip buying)
- Simpler menus, HUD bar above the arena
- WebGL graphics with lighting, shadows and bloom (2D fallback)
- v2.2: boss phases, elite enemies, boss intros, visual juice, achievements, run rating, secret medals, enemy codex

## 🔜 Next (v2.1 – stabilize)
1. **Balance pass on the new economy:** play full story runs on each difficulty and tune prices and enemy HP.
2. **Save the code to git:** commit the work locally, then push / open a PR when you say so.
3. **Settings menu:** volume sliders, music on/off, screen shake on/off, graphics 3D/2D, glow strength.
4. **Bundle Three.js locally** so 3D works offline.
5. **Performance options:** shadow quality and particle amount for slower PCs.

## 💡 Later (v2.x – content)
- **Story chapters:** short text intro before each boss chapter, with its own colors and music.
- **Elite enemies:** rare tougher variants that drop a free upgrade.
- **Mid-wave events:** meteor shower, gold rush (double money).
- **More bosses and maps** for Endless.
- **Ship skins and a 4th ship.**

## 💡 Later (v3.x – reach)
- **Touch controls** for phones and tablets (virtual joystick + buttons).
- **Gamepad support.**
- **Meta progression:** permanent currency between runs to unlock skins, ships and modifiers.
- **Daily challenge** with a fixed seed and a local leaderboard.
- **Language option** (English / Hebrew).
- **Accessibility:** colorblind-friendly palette, reduced flashing.
- **Publishing:** host as a web page (e.g. itch.io); later consider a desktop build (Godot) if we outgrow the browser.

## 📋 Ideas backlog (proposed 2026-10-09, with Claude's opinion)
Effort: **S** small · **M** medium · **L** large. ⭐ = recommended first.

| # | Idea | Opinion | Effort | Notes |
|---|---|---|---|---|
| 1 | ✅ **Boss phases** at 70% / 40% / 10% HP | Great | M | Biggest fun boost per hour of work. Each of the 4 bosses gets new attacks per phase. |
| 2 | ✅ **Elites in normal waves** (2 per ~50 enemies, 2–3x stronger, a bit more money) | Great | S | Fits the existing spawn code. Glowing outline so they read clearly. |
| 3 | ✅ **Cinematic boss intro** (music dips, camera focus, name card) | Great | S | Builds on the wave-clear cinematic. |
| 4 | ✅ **Visual juice** (shake by explosion size, crit flash, distortion around big blasts) | Great | S–M | Distortion is easy now that we have WebGL. Respect a "screen shake off" setting. |
| 5 | ✅ **Achievements** (e.g. no damage for all 20 waves) | Great | M | Gives long-term goals; each unlocks a skin. Saved in the browser. |
| 6 | ✅ **Run rating Bronze → SSS** (time, damage taken, accuracy, kills) | Good | S | Shown on the victory and death screens. Pairs with achievements. |
| 7 | ✅ **Secret missions during a run** (e.g. 5 dash kills → medal) | Good | S | Show only after completing, so they don't clutter the screen. |
| 8 | **Orbiting drones** that block shots / hit on contact | Good | S | Upgrade the existing Orbiting Blade instead of a new system. |
| 9 | **Vortex ability** (pulls enemies and shots, then explodes) | Good | M | Could be a 4th ship's active, or a rare upgrade. |
| 10 | **Post-boss choice** (strong / safe / rare with a drawback) | Good | M | Merges well with "cursed upgrades" idea. |
| 11 | **Elite-style enemy hit effects by material** (metal sparks, energy light, boss shockwave) | Good | S | Pure visual; uses the 3D particle system. |
| 12 | **Shot trail changes with upgrades** | Good | S | Color/shape by damage, pierce and multishot. |
| 13 | **Evolving weapon** (normal → chain lightning ×3 → splitting beam) | Good, careful | M | Strong idea, but must not clash with the shop upgrades. Could be the Striker's identity. |
| 14 | **Elemental system** (fire + ice = shatter, oil + fire = burning zone) | Good, careful | L | Deep but adds rules; risk of the "too complicated" problem. Start with 2 elements (fire, frost) since Frost already exists. |
| 15 | **Destructible boss parts** (destroy the missile launcher first) | Good, careful | L | Works best with phases (#1). Do it for one boss first. |
| 16 | **Arena devices** (shoot to activate a laser, trap or turret; enemies can use them too) | Good | M | Great for specific maps (e.g. one new map built around them). |
| 17 | **Meta tech tree** (permanent currency: speed, magnet, crit) | Good, careful | M | Must stay small so it doesn't break the economy we just balanced. Unlock after the first story win. |
| 18 | ✅ **Enemy encyclopedia** | Nice | S | Helps new players learn enemies without cluttering the game. |
| 19 | **More ships / playstyles** | Partly done | M | We have 3 ships; a 4th (e.g. Vortex ship with a secondary weapon) fits here. |
| 20 | **Slow-mo at low HP** | Careful | S | Can feel unfair or annoying; make it short and optional (setting). |
| 21 | **Deeper 3D backgrounds** (background asteroids, moving nebulae, lights by player position) | Good | S–M | Natural next step for the WebGL renderer. |

**Suggested order:** ✅ v2.2 = #1–#7 and #18 (done) → v2.3 "New toys" = #8, #9, #10, #12 → later the bigger systems #13–#17.

## Open questions
- Is money now too tight on Normal? Needs real play feedback.
- Should Collapsing Arena and Warp Loop also appear in Story?
