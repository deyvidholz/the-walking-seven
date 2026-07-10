# 📊 The Walking Seven — Complete Value Reference

Every value this mod changes, with the **original V3 value**, the **new value**, and **how many times** bigger or smaller it is. Use this to understand exactly what the mod does — or to re-balance it to your taste.

> ⚠️ **These numbers were read from 7 Days to Die version 3 (V3).**
> The mod forces the **New** value regardless of what the game ships, but if a future update changes a base value, the **“V3”** column below may no longer match the game. After a **major** game update, re-verify these against the vanilla files in `Data/Config/`. Nothing here breaks on a normal patch.

**Legend:** `×N` = N times the original. Cooking times marked *auto* had no fixed value in V3 — the game calculated them from the recipe's ingredients (roughly 1 second per ingredient), so they were already only a few seconds; the mod pins them to a fixed value.

---

## 1. 🪜 Zombies can't climb ladders
*File: `entityclasses.xml`*

| Setting | Entity | V3 | New |
|---|---|:-:|:-:|
| `CanClimbLadders` | `zombieTemplateMale` (all zombies inherit) | `true` | **`false`** |

Players, traders and survivor NPCs keep `true` — untouched.

---

## 2. 🥫 Food nutrition (fullness restored)
*File: `items.xml` — the `$foodAmountAdd` value*

| Item | V3 | New | Change |
|---|:-:|:-:|:-:|
| foodCanTuna | 5 | 25 | **×5** |
| foodCanStock | 5 | 20 | **×4** |
| foodCanMiso | 10 | 30 | **×3** |
| foodCanPeas | 10 | 30 | **×3** |
| foodCanPears | 10 | 30 | **×3** |
| foodCanSoup | 10 | 30 | **×3** |
| foodCharredMeat | 10 | 30 | **×3** |
| foodGrilledMeat | 10 | 30 | **×3** |
| foodBoiledMeat | 10 | 30 | **×3** |
| foodHoney | 8 | 20 | **×2.5** |
| foodCanCatfood | 10 | 25 | **×2.5** |
| foodCanDogfood | 10 | 25 | **×2.5** |
| foodCornOnTheCob | 10 | 25 | **×2.5** |
| foodCornBread | 10 | 25 | **×2.5** |
| foodBakedPotato | 10 | 25 | **×2.5** |
| foodEggBoiled | 10 | 25 | **×2.5** |
| foodCanBeef | 15 | 35 | **×2.33** |
| foodCanChicken | 15 | 35 | **×2.33** |
| foodCanLamb | 15 | 35 | **×2.33** |
| foodCanChili | 15 | 35 | **×2.33** |
| foodCanSham | 15 | 35 | **×2.33** |
| foodCanPasta | 15 | 35 | **×2.33** |
| foodCanSalmon | 15 | 35 | **×2.33** |
| foodPumpkinBread | 12 | 25 | **×2.08** |
| foodShamSandwich | 15 | 30 | **×2** |
| foodEgg | 5 | 10 | **×2** |

*Hearty cooked meals (stews, pies, brisket — already 30–141 fullness) and raw crops are intentionally left at vanilla.*

---

## 3. 💧 Water (hydration restored)
*File: `items.xml` — the `$waterAmountAdd` value*

| Item | V3 | New | Change |
|---|:-:|:-:|:-:|
| drinkJarBoiledWater | 20 | 35 | **×1.75** |

*Other drinks (mineral water, teas, coffee) were already generous and are left at vanilla.*

---

## 4. 🍳 Cooking / crafting time
*File: `recipes.xml` — the `craft_time` (seconds)*

**Food**

| Recipe | V3 time | New | Change |
|---|:-:|:-:|:-:|
| foodHoboStew | 65 | 5 | **13× faster** |
| foodCanSham | 15 | 3 | **5× faster** |
| foodBurntSmoothie | 25 | 5 | **5× faster** |
| foodOasisSmoothie | 25 | 5 | **5× faster** |
| foodFrostbiteSmoothie | 25 | 5 | **5× faster** |
| foodAtomicSmoothie | 25 | 5 | **5× faster** |
| foodMeatStew | *auto* | 5 | fixed |
| foodVegetableStew | *auto* | 5 | fixed |
| foodGumboStew | *auto* | 5 | fixed |
| foodShamChowder | *auto* | 5 | fixed |
| foodHoneyGlazedSham | *auto* | 5 | fixed |
| foodHoneyBrisket | *auto* | 5 | fixed |
| foodShepardsPie | *auto* | 5 | fixed |
| foodSpaghetti | *auto* | 5 | fixed |
| foodTunaFishGravyToast | *auto* | 5 | fixed |
| foodBlueberryPie | *auto* | 4 | fixed |
| foodPumpkinPie | *auto* | 4 | fixed |
| foodPumpkinCheesecake | *auto* | 4 | fixed |
| foodSteakAndPotato | *auto* | 4 | fixed |
| foodChiliDog | *auto* | 3 | fixed |
| foodFishTacos | *auto* | 3 | fixed |
| foodBaconAndEggs | *auto* | 3 | fixed |
| foodPumpkinBread | *auto* | 3 | fixed |
| foodCharredMeat | *auto* | 2 | fixed |
| foodGrilledMeat | *auto* | 2 | fixed |
| foodBoiledMeat | *auto* | 2 | fixed |
| foodCornOnTheCob | *auto* | 2 | fixed |
| foodCornBread | *auto* | 2 | fixed |
| foodCornMeal | *auto* | 2 | fixed |
| foodBakedPotato | *auto* | 2 | fixed |
| foodEggBoiled | *auto* | 2 | fixed |

**Drinks / water**

| Recipe | V3 time | New | Change |
|---|:-:|:-:|:-:|
| drinkYuccaJuiceSmoothie | 25 | 4 | **6.25× faster** |
| drinkJarGrandpasAwesomeSauce | *auto* | 8 | fixed |
| drinkJarBeer | *auto* | 4 | fixed |
| drinkJarGrandpasMoonshine | *auto* | 5 | fixed |
| drinkJarGrandpasLearningElixir | *auto* | 5 | fixed |
| drinkJarBlackStrapCoffee | *auto* | 3 | fixed |
| drinkJarBoiledWater | *auto* | 2 | fixed |
| drinkJarPureMineralWater | *auto* | 2 | fixed |
| drinkJarYuccaJuice | *auto* | 2 | fixed |
| drinkJarGoldenRodTea | *auto* | 2 | fixed |
| drinkJarHoneyTea | *auto* | 2 | fixed |
| drinkJarRedTea | *auto* | 2 | fixed |
| drinkJarCoffee | *auto* | 2 | fixed |

*Note: `drinkJarRiverWater` has no cook recipe in V3 (river water is collected, not brewed), so there is nothing to speed up there.*

---

## 5. 💣 Grenades & thrown explosives — entity damage
*File: `items.xml` — `Explosion` → `EntityDamage` (block damage left at vanilla)*

| Item | Block dmg (unchanged) | V3 entity | New entity | Change |
|---|:-:|:-:|:-:|:-:|
| thrownAmmoPipeBomb | 5 | 253 | 800 | **×3.16** |
| thrownGrenade | 10 | 341 | 1050 | **×3.08** |
| thrownGrenadeContact | 10 | 341 | 1050 | **×3.08** |
| thrownDynamite | 3000 | 550 | 1600 | **×2.91** |
| thrownTimedCharge | 110 | 800 | 2000 | **×2.5** |

---

## 6. 🚀 Rocket launcher ammo — entity damage
*File: `items.xml` — block damage left at vanilla*

| Ammo | Damage type | V3 | New | Change |
|---|---|:-:|:-:|:-:|
| ammoRocketHE | Explosion (AoE) entity | 420 | 1300 | **×3.10** |
| ammoRocketHE | Direct-hit entity | 20 | 200 | **×10** |
| ammoRocketFrag | Explosion (AoE) entity | 730 | 2200 | **×3.01** |
| ammoRocketFrag | Direct-hit entity | 30 | 300 | **×10** |

---

## 7. 🎒 Inventory / backpack — 96 slots
*Files: `entityclasses.xml` (playerMale) + `XUi_InGame/windows.xml`*

| Setting | File | V3 | New | Change |
|---|---|:-:|:-:|:-:|
| `BagSize` (real slot count) | entityclasses | 45 | 96 | **×2.13** |
| `carryCapacityBase` (slots unlocked at start) | entityclasses | 27 | 96 | **×3.56** |
| Backpack grid `rows` | windows | 5 | 8 | — |
| Backpack grid `cols` | windows | 9 | 12 | — |
| Window `width` | windows | 606 | 807 | to fit cells |
| Window `height` | windows | 349 | 550 | to fit cells |

Result: **8 × 12 = 96 slots**, all unlocked from the start (no armor pocket mods needed).

---

## 8. ⛽ Vehicles — fuel & driving drain
*File: `vehicles.xml`*

**Fuel efficiency (`fuelKmPerL`) — higher = burns gas slower. All ×12 → gas lasts 12× longer.**

| Vehicle | V3 | New | Change |
|---|:-:|:-:|:-:|
| vehicleMinibike | .4 | 4.8 | **×12** |
| vehicleMotorcycle | .2 | 2.4 | **×12** |
| vehicleTruck4x4 | .1 | 1.2 | **×12** |
| vehicleGyrocopter | .15 | 1.8 | **×12** |
| vehicleJokeblimp | .05 | .6 | **×12** |

**Food/water drain while driving (`foodDrain`) — set to zero.**

| Vehicle | V3 (drive,turbo) | New |
|---|:-:|:-:|
| vehicleMinibike | .002,.0122 | **0,0** |
| vehicleMotorcycle | .002,.0101 | **0,0** |
| vehicleTruck4x4 | .002,.00811 | **0,0** |
| vehicleGyrocopter | .002,.00811 | **0,0** |

*`vehicleJokeblimp` has no `foodDrain` in V3, and `vehicleBicycle` uses no fuel — both need no change. Fuel-tank capacities are left at vanilla.*

---

<div align="center">
<sub>The Walking Seven · v1.0.0 · values captured from 7 Days to Die V3</sub>
</div>
