# 🪜 The Walking Seven — No Zombie Ladders

A module of **[The Walking Seven](../README.md)**. Works on its own or alongside the other modules.

## What it does
Zombies can **no longer climb ladders** — they path around them instead. Players, traders and survivor NPCs are unaffected and climb normally. All 31 zombie types inherit this from one base template, so a single change covers every zombie.

## Values changed
*File patched: `entityclasses.xml`*

| Setting | Entity (all zombies inherit) | V3 | New |
|---|---|:-:|:-:|
| `CanClimbLadders` | `zombieTemplateMale` | `true` | **`false`** |

## Install
Copy the **`TWS-NoZombieLadders`** folder into your `…/7 Days To Die/Mods/` folder and restart the game. EAC must be off.
*Server note:* this change is enforced server-side, so a client doesn't strictly need it — but matching versions on server + clients is recommended.

> Base ("V3") value captured from 7 Days to Die **version 3**. Full mod reference: [VALUES.md](../VALUES.md).
