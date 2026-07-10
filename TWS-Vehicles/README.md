# ⛽ The Walking Seven — Fuel-Efficient Vehicles

A module of **[The Walking Seven](../README.md)**. Works on its own or alongside the other modules.

## What it does
- **Gas lasts 12× longer** — every fueled vehicle's efficiency (`fuelKmPerL`) is multiplied by 12, keeping their relative balance intact.
- **Driving no longer drains your food/water** — the per-vehicle `foodDrain` is set to zero.

The bicycle uses no fuel and is untouched. Fuel-tank capacities are left at vanilla.

## Values changed
*File patched: `vehicles.xml`*

### Fuel efficiency (`fuelKmPerL` — higher = burns gas slower)
| Vehicle | V3 | New | Change |
|---|:-:|:-:|:-:|
| vehicleMinibike | .4 | 4.8 | **×12** |
| vehicleMotorcycle | .2 | 2.4 | **×12** |
| vehicleTruck4x4 | .1 | 1.2 | **×12** |
| vehicleGyrocopter | .15 | 1.8 | **×12** |
| vehicleJokeblimp | .05 | .6 | **×12** |

### Food/water drain while driving (`foodDrain`, drive/turbo)
| Vehicle | V3 | New |
|---|:-:|:-:|
| vehicleMinibike | .002,.0122 | **0,0** |
| vehicleMotorcycle | .002,.0101 | **0,0** |
| vehicleTruck4x4 | .002,.00811 | **0,0** |
| vehicleGyrocopter | .002,.00811 | **0,0** |

*(`vehicleJokeblimp` has no `foodDrain` in V3, so only its fuel changes.)*

## Install
Copy the **`TWS-Vehicles`** folder into your `…/7 Days To Die/Mods/` folder and restart the game. EAC must be off. These values are enforced server-side.

> Base ("V3") values captured from 7 Days to Die **version 3**. Full mod reference: [VALUES.md](../VALUES.md).
