<div align="center">

# 🧟 The Walking Seven

### A quality-of-life overhaul modlet for **7 Days to Die (V3)**

![Version](https://img.shields.io/badge/version-1.0.0-brightgreen)
![Game](https://img.shields.io/badge/7_Days_to_Die-V3-red)
![Type](https://img.shields.io/badge/type-XML_modlet-blue)
![EAC](https://img.shields.io/badge/anti--cheat-must_be_OFF-orange)

*Survive smarter, not harder. No DLLs, no Harmony patches — just clean XML.*

</div>

---

## 📖 What is this?

**The Walking Seven** is a lightweight, pure-XML **modlet** that smooths out seven of the most tedious corners of 7 Days to Die — so you spend less time babysitting hunger bars and cook timers, and more time fighting the horde.

It doesn't touch the game's balance wildly or add new items. It just makes the survival grind *fair*: food that fills you up, cooking that doesn't take forever, a backpack big enough to actually loot, and vehicles that don't drink a gas can every block.

Because it's a modlet, **it lives in your `Mods/` folder and survives game updates** — the game re-applies it automatically every launch. See [Surviving game updates](#-surviving-game-updates).

> 📋 **Every single value this mod changes** — old value, new value, and how many times bigger/smaller — is documented in **[VALUES.md](VALUES.md)**. All values were read from **game version V3**; a future game update could change the base numbers (see that doc's note).

---

## ✨ What it does

| # | Feature | In short |
|:-:|---------|----------|
| 1 | 🪜 **No zombie ladder-climbing** | Ladders are yours again. Zombies can't use them — but players, traders and survivor NPCs still can. |
| 2 | 🥫 **Hearty food** | Canned & basic cooked food restore **~2–5× more** fullness. No more eating a whole shelf to survive. |
| 3 | 💧 **Better boiled water** | Boiled water gives more hydration. |
| 4 | 🍳 **Near-instant cooking** | Every meal & drink cooks in **2–8 seconds**. Stews went from **65s → 5s**. |
| 5 | 💣 **Deadlier grenades** | Pipe bombs, grenades, dynamite & charges do **~3× entity damage** — block damage untouched. |
| 6 | 🚀 **Deadlier rockets** | HE & Frag rockets hit far harder against enemies, same block damage. |
| 7 | 🎒 **96-slot backpack** | Inventory expanded from 45 → **96 slots**, all unlocked from the start. |
| 8 | ⛽ **Fuel-efficient vehicles** | Gas lasts **12× longer**, and driving **no longer drains** your food/water. |

---

## 📦 Installation

The mod installs into the game's **`Mods/`** folder (next to `Data/`, at the game root).

**Typical path:**
```
…/steamapps/common/7 Days To Die/Mods/
```

### Option A — Download / clone (recommended)
```bash
cd "…/steamapps/common/7 Days To Die/Mods"
git clone https://github.com/deyvidholz/the-walking-seven.git
```

### Option B — Manual
1. Download this repository as a ZIP (**Code ▸ Download ZIP**).
2. Extract it.
3. Copy the folder into `…/7 Days To Die/Mods/` so the layout is:

```
7 Days To Die/
└── Mods/
    └── the-walking-seven/
        ├── ModInfo.xml
        ├── README.md
        ├── VALUES.md
        └── Config/
            ├── entityclasses.xml
            ├── items.xml
            ├── recipes.xml
            ├── vehicles.xml
            └── XUi_InGame/
                └── windows.xml
```

4. Launch the game. On the main menu you can open **Mods** to confirm *The Walking Seven* is loaded.

> ⚠️ **Anti-cheat (EAC):** because this changes game values, **EAC must be OFF** (it is toggled on the launcher / main menu). Singleplayer and Nitrado/dedicated servers with EAC disabled work fine.

---

## 🔄 Surviving game updates

This is the whole point of shipping it as a modlet:

- ✅ **A normal game update does *not* remove your `Mods/` folder.** The mod keeps working — you do **nothing**. The game re-applies it on the next launch.
- ♻️ **If Steam "Verify integrity of game files" or a full reinstall wipes it**, just copy the `the-walking-seven` folder back into `Mods/` (or `git pull`). No re-editing.
- 🔧 **If a *major* game version reshapes the config files**, one or two patches may stop matching — the game logs a warning naming the file, and you'd tweak just that line. This is why the base values live in [VALUES.md](VALUES.md): easy to re-verify against a new version.

Compare that to editing the vanilla files in `Data/Config` directly — **those get overwritten on every update.** A modlet doesn't.

---

## 🤝 Multiplayer

On a server, the mod must be installed **on the server**, and typically on **each client** too (any change to items/UI). Keep versions identical on both sides. EAC off.

---

## 🧹 Uninstall

Delete the `the-walking-seven` folder from `Mods/` and restart the game. Nothing else is touched — the mod never modifies your actual game files, it only patches them in memory at load.

---

## 🛠️ How it works (for the curious)

Instead of copying and editing the game's big config files, each file under `Config/` contains a handful of **XPath patch instructions** that surgically change single values at load time. Example — the ladder change is literally one line:

```xml
<set xpath="//entity_class[@name='zombieTemplateMale']//property[@name='CanClimbLadders']/@value">false</set>
```

The vanilla files are never altered on disk. That's what makes it update-proof and easy to uninstall.

---

## 📜 License & credits

Made by **deyvidholz**. Released free to use, modify, and share — a credit back to this repo is appreciated. Not affiliated with The Fun Pimps.

**Full change reference → [VALUES.md](VALUES.md)**

<div align="center">
<sub>🧟 Stay sharp. Keep your ladders clear. 🧟</sub>
</div>
