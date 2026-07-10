# 🍳 The Walking Seven — Food & Cooking

A module of **[The Walking Seven](../README.md)**. Works on its own or alongside the other modules.

## What it does
- **Canned & basic cooked food** restore **~2–5× more** fullness, so you don't eat a whole shelf to survive.
- **Boiled water** gives more hydration.
- **Cooking is near-instant** — every meal and drink finishes in **2–8 seconds** (stews went from 65s → 5s).

Hearty meals (stews, pies, brisket — already 30–141 fullness) and raw crops are intentionally left at vanilla.

## Values changed
*Files patched: `items.xml` (food/water), `recipes.xml` (cook times)*

### Food nutrition (fullness restored — `$foodAmountAdd`)
| Item | V3 | New | Change |
|---|:-:|:-:|:-:|
| foodCanTuna | 5 | 25 | **×5** |
| foodCanStock | 5 | 20 | **×4** |
| foodCanMiso / Peas / Pears / Soup | 10 | 30 | **×3** |
| foodCharredMeat / GrilledMeat / BoiledMeat | 10 | 30 | **×3** |
| foodHoney | 8 | 20 | **×2.5** |
| foodCanCatfood / Dogfood | 10 | 25 | **×2.5** |
| foodCornOnTheCob / CornBread / BakedPotato / EggBoiled | 10 | 25 | **×2.5** |
| foodCanBeef / Chicken / Lamb / Chili / Sham / Pasta / Salmon | 15 | 35 | **×2.33** |
| foodPumpkinBread | 12 | 25 | **×2.08** |
| foodShamSandwich | 15 | 30 | **×2** |
| foodEgg | 5 | 10 | **×2** |

### Water (hydration — `$waterAmountAdd`)
| Item | V3 | New | Change |
|---|:-:|:-:|:-:|
| drinkJarBoiledWater | 20 | 35 | **×1.75** |

### Cooking time (`craft_time`, seconds)
Recipes that had **no** fixed time in V3 were auto-calculated from ingredients (~1s each); this module pins them to a fixed value.

| Recipe(s) | V3 | New |
|---|:-:|:-:|
| foodHoboStew | 65 | **5** (13× faster) |
| smoothies (Burnt/Oasis/Frostbite/Atomic), foodCanSham | 15–25 | **3–5** (5× faster) |
| drinkYuccaJuiceSmoothie | 25 | **4** (6.25× faster) |
| stews, big meals (MeatStew, Gumbo, Spaghetti, Brisket…) | *auto* | **5** |
| pies, steak & potato | *auto* | **4** |
| chili dog, tacos, bacon & eggs, pumpkin bread | *auto* | **3** |
| grilled/charred/boiled meat, corn, bread, potato, eggs | *auto* | **2** |
| grandpa's awesome sauce | *auto* | **8** |
| beer, moonshine, learning elixir | *auto* | **4–5** |
| boiled/mineral water, teas, coffee, yucca juice | *auto* | **2–3** |

*(`drinkJarRiverWater` has no cook recipe in V3 — river water is collected, not brewed — so nothing to change there.)*

## Install
Copy the **`TWS-Food`** folder into your `…/7 Days To Die/Mods/` folder and restart the game. EAC must be off. On a server, food amounts and cook times are enforced server-side; install on clients too so tooltips match.

> Base ("V3") values captured from 7 Days to Die **version 3**. Full mod reference: [VALUES.md](../VALUES.md).
