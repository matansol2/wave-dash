# Wave Dash: fixes and ideas

All changes are local only in `index.html` (nothing pushed).

## Fixes made
1. **Translated everything to English**: title, menu, shop, upgrade names and descriptions, HUD, banners, pause and death screens. The page is now `lang="en" dir="ltr"`, so canvas text no longer renders right-to-left (e.g. "$50" no longer shows as "50$").
2. **Boss minions spawn at the boss**: only one of the two minions was moved to the boss; the other appeared at a random screen edge. Both now spawn beside the boss, and they count toward the wave progress bar.
3. **Health packs are no longer wasted at full HP**: they stay on the ground until you are hurt. The pop-up now shows the HP actually healed instead of always "+5".
4. **Health packs no longer get sucked to you at wave end**: the end-of-wave magnet now pulls only the pink drops, so packs stay where they are for later.
5. **No accidental restart from a focused button**: the Start / Play Again button is unfocused when a run begins, so Space or Enter can't trigger it during play.
6. **Firing can't get stuck on**: a cancelled pointer (touch interrupted, pen lifted off-screen) now stops firing.
7. **Works on older browsers**: added a fallback for canvas `roundRect`, which older Safari lacks and which crashed the HUD drawing.

Checked: script passes a syntax check, and a scripted run cleared waves 1 to 11 (including both bosses) with no console errors.

## Playability ideas
- **Touch controls**: virtual joystick plus dash button, so it works on phones.
- **Dash toward the mouse** when standing still (now it dashes in the last move direction).
- **Exploders pay out when they blow up on you**; only reward kills by the player.
- **Dash upgrade can make you nearly invincible** at max level (16 of every 25 frames); cap it or shorten the dash shield.
- **Sound effects and music**, with a mute key.
- **Settings**: volume, screen shake on/off, show aim line.
- **Shop shows your current stats** so you can judge upgrades.

## Content ideas
- **New enemies**: a splitter that breaks into small ones, a shielded enemy that only takes damage from behind, a healer that restores nearby enemies, a teleporter.
- **More bosses**: a different boss every 5 waves instead of the same one (e.g. a laser sweeper at wave 10, a summoner at wave 15).
- **New upgrades**: ricochet shots, homing shots, critical hits, lifesteal, a dash that damages enemies, slowing shots.
- **Synergies**: bonus effects when you own certain pairs (e.g. Piercing + Multishot).
- **Playable ships**: start choices with different stats (fast and fragile, slow tank).
- **Run modifiers / daily challenge**: e.g. "double enemies, double money".
- **Endless leaderboard stats**: best kills and best time, not only best wave.
