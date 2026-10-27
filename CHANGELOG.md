# Changelog

## 1.0.0 - 2026-10-26 - first public release

- Settings menu on `/dps`: METER on/off, STYLE art/text, HIT POP on/off, RESET SESSION, with a live preview of the band.
- Every choice is remembered per player and survives relogs and plugin reloads.
- JSON config: default on/off, optional permission gate, DPS window, refresh rate, which targets count (NPCs, animals,
  buildings, vehicles), art base URL and cache tag for self-hosting, band position and scale, hit pop on/off.
- All player-facing text goes through the Lang API (`lang/en/HoneyBadgerDps.json`).
- Permissions `honeybadgerdps.use` (only enforced when the config asks for it) and `honeybadgerdps.admin`.
- The damage hooks are only subscribed while at least one meter is on screen; nothing runs per hit otherwise.
- Hits on corpses never count; buildings and deployables are off by default.
- Console commands renamed to `hbdps.menu`, `hbdps.toggle`, `hbdps.set`, `hbdps.reset`, `hbdps.probe`.
  (The old `hb.menu` / `hb.give` loadout commands moved to a separate admin-only test plugin and are not part of this release.)

## 0.2.x - 2026-10-13 to 2026-10-14 - private builds on the Honey Badger server

- Painted band art, hit pop moved out of the crosshair, per-player on/off memory, `/dps text` fallback.

## 0.1.0 - 2026-10-10

- First text meter: DPS, last hit, total, measured from the health drop one tick after each hit.
