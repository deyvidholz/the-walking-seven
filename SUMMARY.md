# 🧟 The Walking Seven

**A quality-of-life overhaul for 7 Days to Die (V3) — fully modular**

**Version** 1.0.0 · **Game** 7 Days to Die V3 · **Type** XML modlet (no DLLs) · **EAC** must be OFF

---

## What is this?

The Walking Seven smooths out seven of the most tedious corners of 7 Days to Die — so you spend less time babysitting hunger bars and cook timers, and more time fighting the horde. It doesn't add items or wildly rebalance the game; it just makes the survival grind *fair*.

It ships as **five independent modules** — install only the ones you want. Because they're modlets, they live in your `Mods/` folder and **survive game updates**.

## The modules

| Module | What it does |
|---|---|
| 🪜 **TWS-NoZombieLadders** | Zombies can't climb ladders (players / traders / NPCs still can). |
| 🍳 **TWS-Food** | Heartier canned & cooked food (~2–5×), better boiled water, near-instant cooking (2–8s). |
| 💣 **TWS-Explosives** | Grenades & rockets do ~3× damage to enemies (block damage unchanged). |
| 🎒 **TWS-Backpack60** | 60-slot backpack (5 × 12), all unlocked from the start. |
| ⛽ **TWS-Vehicles** | Gas lasts 12× longer + no food/water drain while driving. |

Every module is standalone — mix and match freely.

## Installation

Each `TWS-*` folder is a complete, standalone modlet. Copy the folders you want **directly into** your game's `Mods/` folder:

```
…/steamapps/common/7 Days To Die/Mods/
```

To install everything, copy all five. Each module must be a **direct** child of `Mods/` (not nested inside another folder), or the game won't load it. Launch the game — the **Mods** entry on the main menu lists what loaded.

**⚠️ EAC (anti-cheat) must be OFF** — this mod changes game values. Singleplayer and EAC-disabled servers work fine.

## Multiplayer

Install the modules on the server **and** on each client, same versions, EAC off. The **TWS-Backpack60** grid is drawn client-side — without it, a player only sees 45 slots even if the server allows 60.

## Surviving game updates

A normal game update does **not** remove your `Mods/` folder, so the modules keep working — you do nothing. Editing the game's config files directly, by contrast, gets overwritten on every update. A modlet doesn't.

## Uninstall

Delete any `TWS-*` folder from `Mods/` and restart — that feature is gone. The mod never edits your real game files; it only patches them in memory at load.

---

**Full docs, per-module guides & the complete value reference (every old → new value):**
👉 https://github.com/deyvidholz/the-walking-seven

*Made by deyvidholz. Free to use, modify and share. Not affiliated with The Fun Pimps.*
