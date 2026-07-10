# 🎒 The Walking Seven — 60-Slot Backpack

A module of **[The Walking Seven](../README.md)**. Works on its own or alongside the other modules.

## What it does
Expands the player backpack from **45 → 60 slots** (a **5 × 12** grid), **all unlocked from the start** — no perk grind or pocket mods required. Five rows fit comfortably on screen at common resolutions.

## Values changed
*Files patched: `entityclasses.xml`, `XUi_InGame/windows.xml`*

| Setting | File | V3 | New | Change |
|---|---|:-:|:-:|:-:|
| `BagSize` (max slot count) | entityclasses | 45 | 60 | **×1.33** |
| `carryCapacityBase` (unlocked slots) | entityclasses | 27 | 60 | **×2.22** |
| Backpack grid `cols` | windows | 9 | 12 | — |
| Window `width` | windows | 606 | 807 | to fit columns |

Grid `rows` (5) and window `height` (349) stay vanilla — only the columns (and window width) change.

## A note on the Pack Mule perk
7 Days to Die only reliably unlocks backpack slots from the **base carry capacity**, not from the Pack Mule perk once the bag is enlarged — so this module unlocks all 60 up front. That makes Pack Mule's *"+backpack slots"* line redundant, but the perk's **other** effects still work: reduced crafting time in the backpack, and a chance to absorb damage. (This is why every large-backpack mod unlocks slots from the start.)

## Install
Copy the **`TWS-Backpack60`** folder into your `…/7 Days To Die/Mods/` folder and restart the game. EAC must be off.

> ⚠️ **Multiplayer:** the grid is drawn **client-side**, so install this on **every client** too — a client without it only sees the vanilla 45-cell grid. If the wider panel crowds other UI at your resolution, lower the window `width` in `Config/XUi_InGame/windows.xml`.

> Base ("V3") values captured from 7 Days to Die **version 3**. Full mod reference: [VALUES.md](../VALUES.md).
