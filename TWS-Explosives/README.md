# 💣 The Walking Seven — Explosives

A module of **[The Walking Seven](../README.md)**. Works on its own or alongside the other modules.

## What it does
Grenades and rocket ammo hit **much harder against enemies** — roughly **3× entity damage**. **Block damage is left completely unchanged**, so this doesn't turn your explosives into base-wrecking tools; it just makes them lethal to the horde.

## Values changed
*File patched: `items.xml` — the `Explosion` → `EntityDamage` (and matching tooltip)*

### Grenades & thrown explosives
| Item | Block dmg (unchanged) | V3 entity | New entity | Change |
|---|:-:|:-:|:-:|:-:|
| thrownAmmoPipeBomb | 5 | 253 | 800 | **×3.16** |
| thrownGrenade | 10 | 341 | 1050 | **×3.08** |
| thrownGrenadeContact | 10 | 341 | 1050 | **×3.08** |
| thrownDynamite | 3000 | 550 | 1600 | **×2.91** |
| thrownTimedCharge | 110 | 800 | 2000 | **×2.5** |

### Rocket launcher ammo
| Ammo | Damage type | V3 | New | Change |
|---|---|:-:|:-:|:-:|
| ammoRocketHE | Explosion (AoE) entity | 420 | 1300 | **×3.10** |
| ammoRocketHE | Direct-hit entity | 20 | 200 | **×10** |
| ammoRocketFrag | Explosion (AoE) entity | 730 | 2200 | **×3.01** |
| ammoRocketFrag | Direct-hit entity | 30 | 300 | **×10** |

*(Molotov does no direct entity damage — it's a fire buff — so it's not part of this module. Rocket **block** damage, e.g. HE's 2500, is untouched.)*

## Install
Copy the **`TWS-Explosives`** folder into your `…/7 Days To Die/Mods/` folder and restart the game. EAC must be off. Damage is computed server-side; install on clients too so tooltips show the new numbers.

> Base ("V3") values captured from 7 Days to Die **version 3**. Full mod reference: [VALUES.md](../VALUES.md).
