# Changelog

## 1.0.2 - 2026-10-27

Maintenance release. No behaviour change.

- Brand spelling: the plugin is now "HoneyBadger DPS Meter" and the studio is HoneyBadger Software, one word, in the
  `[Info]` line, the console load line, the README and the licence files. Config keys, lang keys, permissions and the
  chat command are unchanged, so an in-place update keeps every setting.

## 1.0.1 - 2026-10-27

- Author line in `[Info]` is now `Honeybadgermods`, the uMod account name, as uMod's submission guidelines require.
  The studio is still HoneyBadger Software; nothing else in the plugin changed.
- Licence files split: `LICENSE` is the plain MIT text for the code; the band artwork terms moved to `ART-LICENSE.md`.
- README: the band is four PNG files, not five.

## 1.0.0 - 2026-10-26 - first public release

- Settings menu on `/dps`: METER on/off, STYLE art/text, HIT POP on/off, RESET SESSION, with a live preview of the band.
- Every choice is remembered per player and survives relogs and plugin reloads.
- JSON config: default on/off, optional permission gate, DPS window, refresh rate, which targets count (NPCs, animals,
  buildings, vehicles), art base URL and cache tag for self-hosting, band position and scale, hit pop on/off.
- All player-facing text goes through the Lang API (`lang/en/HoneyBadgerDps.json`).
- Permissions `honeybadgerdps.use` (only enforced when the config asks for it) and `honeybadgerdps.admin`.
- The damage hooks are only subscribed while at least one meter is on screen; nothing runs per hit otherwise.
- Hits on corpses never count; buildings and deployables are off by default.
- TARGET names: players keep their name; Rust's NPC players (named by bot id, e.g. "511") show Scientist, Heavy
  Scientist, Tunnel Dweller, Dweller or Bandit from their prefab; animals and structures show a tidied prefab name
  ("Stag", "Wall External High Stone"). All of it is in the lang file (`Target.*`).
- Console commands renamed to `hbdps.menu`, `hbdps.toggle`, `hbdps.set`, `hbdps.reset`, `hbdps.probe`.
  (The old `hb.menu` / `hb.give` loadout commands moved to a separate admin-only test plugin and are not part of this release.)

## 0.2.x - 2026-10-13 to 2026-10-14 - private builds on the HoneyBadger server

- Painted band art, hit pop moved out of the crosshair, per-player on/off memory, `/dps text` fallback.

## 0.1.0 - 2026-10-10

- First text meter: DPS, last hit, total, measured from the health drop one tick after each hit.
