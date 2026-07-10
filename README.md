<div align="center">

<img src="logo.svg" alt="The Walking Seven" width="160" />

# 🧟 The Walking Seven

### A quality-of-life overhaul for **7 Days to Die (V3)** — now fully modular

![Version](https://img.shields.io/badge/version-1.0.0-brightgreen)
![Game](https://img.shields.io/badge/7_Days_to_Die-V3-red)
![Type](https://img.shields.io/badge/type-XML_modlet-blue)
![Modular](https://img.shields.io/badge/modular-pick_%26_choose-9cf)
![EAC](https://img.shields.io/badge/anti--cheat-must_be_OFF-orange)

*Survive smarter, not harder. No DLLs, no Harmony patches — just clean XML.*

</div>

---

## 📖 What is this?

**The Walking Seven** smooths out seven of the most tedious corners of 7 Days to Die — so you spend less time babysitting hunger bars and cook timers, and more time fighting the horde. It doesn't add items or wildly rebalance the game; it just makes the survival grind *fair*.

It's shipped as **five independent modules** — install only the ones you want. Because they're modlets, they live in your `Mods/` folder and **survive game updates** (the game re-applies them automatically every launch).

> 📋 Every value the mod changes — old value, new value, and how many times bigger/smaller — is in **[VALUES.md](VALUES.md)**. All values were read from **game version V3** (see the note there). Each module folder also has its own README.

---

## 🧩 The modules

| Module folder | What it does | Details |
|---|---|---|
| 🪜 **[TWS-NoZombieLadders](TWS-NoZombieLadders/)** | Zombies can't climb ladders (players/traders/NPCs still can). | [readme](TWS-NoZombieLadders/README.md) |
| 🍳 **[TWS-Food](TWS-Food/)** | Heartier canned/cooked food (~2–5×), better boiled water, near-instant cooking (2–8s). | [readme](TWS-Food/README.md) |
| 💣 **[TWS-Explosives](TWS-Explosives/)** | Grenades & rockets do ~3× damage to enemies (block damage unchanged). | [readme](TWS-Explosives/README.md) |
| 🎒 **[TWS-Backpack60](TWS-Backpack60/)** | 60-slot backpack (5×12), all unlocked from the start. | [readme](TWS-Backpack60/README.md) |
| ⛽ **[TWS-Vehicles](TWS-Vehicles/)** | Gas lasts 12× longer + no food/water drain while driving. | [readme](TWS-Vehicles/README.md) |

Every module is standalone — mix and match freely.

---

## 📦 Installation

Each `TWS-*` folder is a **complete, standalone modlet**. Install by copying the folders you want **directly into** your game's `Mods/` directory (at the game root, next to `Data/`):

```
…/steamapps/common/7 Days To Die/Mods/
```

### Get the files
```bash
git clone https://github.com/deyvidholz/the-walking-seven.git
```
…or **Code ▸ Download ZIP** and extract.

### Then copy the module folder(s) you want into `Mods/`
Pick any combination. To install everything, copy all five. The result should look like this — each module a **direct** child of `Mods/` (not nested inside another folder, or the game won't load it):

```
7 Days To Die/
└── Mods/
    ├── TWS-NoZombieLadders/     ← each is its own modlet
    ├── TWS-Food/                   (ModInfo.xml + Config/ + README.md)
    ├── TWS-Explosives/
    ├── TWS-Backpack60/
    └── TWS-Vehicles/
```

Launch the game — the **Mods** entry on the main menu lists the modules that loaded.

> ⚠️ **Anti-cheat (EAC):** because this changes game values, **EAC must be OFF** (toggled on the launcher / main menu). Singleplayer and EAC-disabled servers work fine.

### 📁 What's in this repo
```
the-walking-seven/            ← this repository (a collection, not a modlet itself)
├── logo.svg
├── README.md                 ← you are here (whole-mod overview)
├── VALUES.md                 ← full change reference for every module
├── TWS-NoZombieLadders/      ┐
├── TWS-Food/                 │  each: ModInfo.xml · README.md · Config/*.xml
├── TWS-Explosives/           │  (the actual XPath patches)
├── TWS-Backpack60/           │
└── TWS-Vehicles/             ┘
```

---

## 🔄 Surviving game updates

- ✅ **A normal game update does *not* remove your `Mods/` folder.** The modules keep working — you do nothing.
- ♻️ **If Steam "Verify integrity" or a reinstall wipes them**, just copy the folders back (or `git pull` and re-copy). No editing.
- 🔧 **If a *major* version reshapes the config files**, a patch may stop matching — the game logs a warning naming the file, and you'd tweak that one line. That's why the base values live in [VALUES.md](VALUES.md): easy to re-verify. Editing `Data/Config` directly, by contrast, gets **overwritten every update** — a modlet doesn't.

---

## 🤝 Multiplayer

Install the modules on the **server**, and on **each client** too (any change touching items/UI). Keep versions identical, EAC off. Note: the **TWS-Backpack60** grid is drawn client-side — without it on a client, that player only sees 45 slots even if the server allows 60.

---

## 🧹 Uninstall

Delete any `TWS-*` folder from `Mods/` and restart — that feature is gone. The mod never edits your actual game files; it only patches them in memory at load, so removing a folder fully reverts it.

---

## 🛠️ How it works (for the curious)

Each module's `Config/` files contain small **XPath patch instructions** that change single values at load time, instead of copying and editing the game's big config files. Example — the ladder change is one line:

```xml
<set xpath="//entity_class[@name='zombieTemplateMale']//property[@name='CanClimbLadders']/@value">false</set>
```

The vanilla files are never altered on disk — that's what makes it update-proof and trivially removable.

---

## 📜 License & credits

Made by **deyvidholz**. Free to use, modify, and share — a credit back to this repo is appreciated. Not affiliated with The Fun Pimps.

**Full change reference → [VALUES.md](VALUES.md)**

<div align="center">
<sub>🧟 Stay sharp. Keep your ladders clear. 🧟</sub>
</div>
