---
title: "Masters of the Universe: Legends Unite – Solo He-Man Strategy Guide & Playthrough Transcripts"
author: "jtquisenberry"
date: "2026-09-30"
description: "A comprehensive strategy guide, reference tables, mechanic deep-dives, exact damage formulas, and deck-thinning transcripts for clearing Biome 6 (Anti-Eternia) in a solo He-Man run."
tags:
  - Masters of the Universe
  - Legends Unite
  - Deckbuilder
  - Strategy Guide
  - He-Man
category: "Game Guides"
version: "1.0"
---

# Overview & Character Setup

This guide documents solo playthroughs of *Masters of the Universe: Legends Unite* playing solo as **He-Man**. The strategy demonstrates optimal paths to beat the game solo, including clearing Biome 6 (Anti-Eternia) and defeating the true final boss, Anti-Eternia Ram Man. Victory can be achieved by leveraging mechanical synergies, strategic deck thinning, and high-burst damage loops.

*Note: This guide (v1.0) was updated on September 30, 2026, and covers the version of the game following the July 22, 2026 bonus content update.*

# Key Mechanics & Engine Interactions

Below are primary game mechanics, keywords, and synergies verified across playthroughs:

* **Solo Target Logic ("Ally" and "allies" Resolution):** In solo play, He-Man counts as his own eligible "ally." Cards with a target of "ally" or "allies" include the solo character as a valid target. For instance, He-Man can grant himself an extra turn using **YOUR TURN!**.
* **Turn-1 Status Immunity Window:** **IMMUNITY STONE** negates incoming status applications on Turn 1 of combat. Extending Turn 1 using **YOUR TURN!** allows for safe cycling and setup.
* **IMMUNITY Mechanics & Status Afflictions:** **IMMUNITY** prevents direct **DAMAGE** from attacks, but **it does not prevent POISON or BURN status applications**. For example, playing **VENOM FLASK** against an immune target still inflicts POISON stacks, which tick for full HP damage at the start of the target's next turn. Additionally, targets can suffer from both **POISON** and **BURN** simultaneously.
* **Absolute Shields & SHATTER Functionality:** Enemy SHIELDs are "absolute shields" that completely block incoming damage regardless of raw power or **EMPOWER** multipliers (e.g., a 128 DAMAGE hit against 1 stack of SHIELD reduces 0 HP). However, a single **SHATTER** card, such as **SHATTER STRIKE**, strips an entire stack of **SHIELD** at once, even if the target has a multi-instance stack of 3 SHIELDs.
* **Turn-1 Shield Conservation:** Using **ULTIMATE** shield cards on Turn 1 is wasteful when combining **SHIELD OF ETERNIA** with **IMMUNITY STONE**. While **SHIELD OF ETERNIA** prevents SHIELD expiration, enemy attacks still deplete active SHIELD stacks even while **IMMUNITY STONE** renders He-Man immune. Since ULTIMATE cards are single-use per battle, save them until after Turn 1 immunity expires.
* **Multi-Turn EMPOWER Stacking:** **EMPOWER** persists between turns as long as no Attack cards are played. By skipping attacks and playing defense/skills, **EMPOWER** can be stacked repeatedly (multiplying base damage for massive burst hits).
* **Card Status Terms ("Temporary"):** The **Temporary** status modifier means the card remains available for the **duration of the entire battle**, not just the single turn it is drawn or generated. If unplayed, Temporary cards return to the draw pool and can be drawn again in subsequent turns.
* **Merchant Inventory Re-Rolling:** Exiting to the main menu and reloading the game successfully re-rolls merchant inventories and trading post relic choices without losing gold or progress.
* **YOUR TURN! Cloning Mechanics:** **YOUR TURN!** cannot be naturally drawn again on subsequent turns during normal play. The only observed method to play **YOUR TURN!** multiple times in a single battle is by cloning it with **MAGIC MIRROR**.
* **Damage Engine Order of Operations:** Stat calculations follow a strict priority sequence:
  1. Base Damage + INSPIRATION bonus.
  2. Multiplied by EMPOWER.
  3. Scaled extra damage (e.g., POWER-scaling) multiplied by EMPOWER (*Note: INSPIRATION does not apply to extra scaling damage*).
  
  **Total Damage = ((Base Damage + INSPIRATION) * EMPOWER) + (Extra Damage * EMPOWER)**

# Advanced Boss Strategies & High-Burst Combos

Defeating endgame encounters like Hordak (Biome 5, 250 HP) and Anti-Eternia Ram Man (Biome 6, 300 HP) requires dedicated damage engines:

### Strategy 1: The (Base + INSPIRATION) * EMPOWER Engine (Peak Damage Output)
* **Core Setup:** Requires **MAGIC MIRROR**, **POWER UP!**, **CHAMPION'S ROAR** (+2 INSPIRATION), high **POWER** accumulation via **CHAIN OF CONFLICT**, and **BATTLE CAT, ATTACK!**.
* **Execution:**
  1. Play **MAGIC MIRROR** targeting **POWER UP!** to duplicate it.
  2. Play both copies of **POWER UP!** (reaching 4x EMPOWER).
  3. Play **CHAMPION'S ROAR** to grant +2 INSPIRATION.
  4. Play **BATTLE CAT, ATTACK!** (Base 12 DAMAGE, plus 8 extra DAMAGE per POWER) with a large amount of POWER stored.
  5. (Optional) Increase EMPOWER further using **BATTLE PLAN**, or increase INSPIRATION further using **BATTLE CAT'S ROAR**.
* **Damage Calculation Example:**
  * **Example POWER:** Suppose that you have collected 54 POWER.
  * **Base Damage Component:** (12 Base + 2 INSPIRATION) * 4 EMPOWER = 56 DAMAGE
  * **Extra Power Component:** (8 Base Extra * 54 POWER) * 4 EMPOWER = 432 * 4 = 1728 DAMAGE
  * **Total Output:** 56 + 1728 = 1784 DAMAGE
* **Key Takeaway:** Addition of INSPIRATION takes precedence over multiplication by EMPOWER, while INSPIRATION does not add to extra POWER-scaling damage.

### Strategy 2: Accelerated BATTLEMARK Doubling Engine
* **Core Setup:** Requires **MIGHTY BATTLE AXE**, **SWIFT STRIKE**, and **CHAIN OF CONFLICT**.
* **Execution:**
  1. Accumulate POWER in battles leading up to the boss.
  2. Play **MIGHTY BATTLE AXE** to inflict 4 BATTLEMARK per POWER (e.g., 25 POWER yields 100 BATTLEMARK).
  3. Play **SWIFT STRIKE** immediately after to double the BATTLEMARK stacks on the target (e.g., 100 BATTLEMARK $\rightarrow$ 200 BATTLEMARK).
  4. Play a low-cost Attack card in the same turn when BATTLEMARK was inflicted, or BATTLEMARK will expire.
* **Efficiency Advantage:** Incorporating **SWIFT STRIKE** cuts the required POWER accumulation in half to achieve equivalent damage thresholds.

### Strategy 3: The Infinite POWER Stacking Rules (ZOAR & Relic Constraints)
* **Core Setup:** Built around storing unspent POWER across battles using **CHAIN OF CONFLICT**.
* **Prohibited Card:** **ZOAR** must not be present in the deck. **ZOAR** automatically plays any Attack card drawn from its 3-card draw. Eventually, this forces an automated play of an Unleash Power card, such as **I HAVE THE POWER**, which completely drains accumulated POWER.
* **Prohibited Relic:** **BATTLE HARNESS** must not be equipped, as it caps maximum stored POWER at 6.

### Strategy 4: The Magic Mirror Double-EMPOWER Burst (256+ Multi-target Damage)
* **Core Setup:** Requires **MAGIC MIRROR**, **POWER UP!**, **BATTLE PLAN**, and a heavy area-of-effect finisher like **I HAVE THE POWER**.
* **Execution:**
  1. Play down your hand until **MAGIC MIRROR** and **POWER UP!** are the remaining options.
  2. Play **MAGIC MIRROR** to target and duplicate **POWER UP!** (creating a Temporary, Ultimate copy).
  3. Play both the original **POWER UP!** (+2 EMPOWER) and the duplicate **POWER UP!** (+2 EMPOWER).
  4. Cycle **BATTLE PLAN** twice across rounds without playing Attack cards to add +4 more EMPOWER, building up to **8x EMPOWER**.
  5. Play **I HAVE THE POWER** (32 Base DAMAGE). The 8x multiplier elevates the attack to **256 DAMAGE** across all enemies without requiring pre-battle POWER farming. Additionally, **I HAVE THE POWER** carries the SHATTER effect, which destroys enemy SHIELD stacks. 
* **Optimization & Anti-Bloat Warning:** Avoid mixing engines. Running **MIGHTY BATTLE AXE** (a BATTLEMARK-dependent Unleash Power card) or slow utility like **CRYSTAL BALL** inside a pure EMPOWER engine dilutes card draws, significantly delaying how quickly you reach 8x EMPOWER or higher.

# Cards

These are the cards observed while playing the game; it is not an exhaustive list. 

| Card Name | Energy Cost | Power Gain | Description / Editor's Note | Observed with Character |
| :--- | :---: | :---: | :--- | :---: |
| **ANTIDOTE** | 0 | 0 | Consumable. Remove all your POISON. Gain RESISTANCE. | He-Man |
| **BATTLE CAT, ATTACK!** | 2 | 0 | Unleash Power. SHATTER. Deal 12 DAMAGE. Deal extra 8 DAMAGE for each POWER. | He-Man |
| **BATTLE CAT'S ROAR** | 1 | 1 | All allies gain 4 INSPIRATION. | He-Man |
| **BATTLE PLAN** | 1 | 0 | Draw 1 card. If you draw an Attack, gain 2 EMPOWER. | He-Man |
| **CALL TO ARMS** | 1 | 0 | Ultimate. Taunt. Gain 3 SHIELD. | He-Man |
| **CASTLE GRAYSKULL** | 1 | 1 | Gain RESISTANCE. | He-Man |
| **CHAMPION'S ROAR** | 0 | 1 | All allies gain 2 INSPIRATION. | He-Man |
| **CRYSTAL BALL** | 0 | 0 | Utility spell. Can bloat fast EMPOWER combo decks if unneeded. | He-Man |
| **FLAME VIAL** | 0 | 0 | **Description:** Consumable. Inflict BURN on target.<br>**Editor's Note:** Bypasses target IMMUNITY status. | He-Man |
| **FRENZY STRIKE** | 3 | 0 | Deal 36 DAMAGE. Costs 1 less ENERGY if you have BATTLEMARK. | He-Man |
| **GIANT MARSHMALLOW** | 0 | 0 | Campfire. Rest heals an extra 30% of Max HP. | He-Man |
| **GRACE OF GRAYSKULL** | 3 | 0 | Consumable. Super Defense Mode. Heal HP all allies! | He-Man |
| **GREATER POTION** | 0 | 0 | Consumable. Heal 30 HP. | He-Man |
| **GUARDIAN'S TONIC** | 2 | 0 | Heal targeted ally 12 HP. If target's HP is below 50%, apply 2 SHIELD. | He-Man |
| **HERO'S FIST** | 2 | 1 | SHATTER. Deal 18 DAMAGE. | He-Man |
| **I HAVE THE POWER** | 6 | 0 | **Description:** Unleash Power. SHATTER. Deal 32 DAMAGE to all enemies. This card costs 1 less ENERGY for each POWER.<br>**Editor's Note:** Since this card has the Unleash Power disposition, it consumes all of the player's POWER. Having 12 POWER does not enable consecutive plays of the card. | He-Man |
| **MAGIC MIRROR** | 0 | 0 | **Description:** Ultimate. Copy 1 random card from your hand. Gain ENERGY equal to its ENERGY cost.<br>**Editor's Note:** High-value target for duplication is POWER UP! or YOUR TURN!. The Ultimate disposition prevents using a pair of **MAGIC MIRROR** cards to make unlimited duplicate **MAGIC MIRROR**. | He-Man |
| **MARSHMALLOW** | 0 | 0 | Campfire. Rest heals an extra 15% of Max HP. | He-Man |
| **MIGHTY BATTLE AXE** | 1 | 0 | Unleash Power. Deal 8 DAMAGE. Apply 4 BATTLEMARK for each POWER. | He-Man |
| **POWER BREW** | 0 | 0 | Consumable. Apply IMMUNITY to all allies. | He-Man |
| **POWER SWORD** | 1 | 1 | Deal 14 DAMAGE. Suffer 2 BATTLEMARK. | He-Man |
| **POWER UP!** | 1 | 0 | Ultimate. Gain 2 EMPOWER. | He-Man |
| **PURIFYING SHIELD** | 0 | 0 | Ultimate. Refresh yourself. Gain 1 SHIELD. Heal 6 HP for each of your SHIELD. | He-Man |
| **RADIANT DEFENSE** | 0 | 0 | Ultimate. All allies whose HP is below 50% gain IMMUNITY and RESISTANCE. | He-Man |
| **ROYAL CHARGE** | 3 | 0 | Ultimate. Deal 32 DAMAGE. If blocked, deal 8 DAMAGE to a random enemy 3 times. | He-Man |
| **SHATTER STRIKE** | 1 | 1 | **Description:** SHATTER. Deal 8 DAMAGE.<br>**Editor's Note:** SHATTER is required to strip enemy "absolute shields". Strips all instances of a multi-stack SHIELD in a single play. | He-Man |
| **SHIELD** | 1 | 0 | Gain 1 SHIELD. | He-Man |
| **SHIELD SLAM** | 1 | 0 | Ultimate. SHATTER. Deal 6 DAMAGE. Deal extra 12 DAMAGE for each SHIELD shattered. | He-Man |
| **SMELLY POTION** | 0 | 0 | Consumable. Heal 10 HP. Gain 10 RESTORATION. | He-Man |
| **SNACK BREAK** | 1 | 0 | Heal 5 HP. | He-Man |
| **SOOTHING SHIELD** | 1 | 0 | Ultimate. Gain 2 SHIELD. Convert stacks of POISON, BURN, and BLEED into 2 HP each. | He-Man |
| **SORCERESS'S ELIXIR** | 0 | 0 | **Description:** Add 2 random potion cards into your hand.<br>**Editor's Note:** The draw pool for potion cards includes SMELLY POTION, POWER BREW, FLAME VIAL, ANTIDOTE, GREATER POTION, SWEET POTION, and VENOM FLASK. | He-Man |
| **SORCERESS'S GIFT** | 1 | 0 | Add 3 Hand Axe into your hand. | He-Man |
| **STRIKE** | 1 | 0 | Deal 5 DAMAGE. | He-Man |
| **SWEET POTION** | 0 | 0 | Consumable. Heal 10 HP. Gain 2 Energy. | He-Man |
| **SWIFT STRIKE** | 1 | 0 | Deal 4 DAMAGE. Double target's BATTLEMARK. | He-Man |
| **SWORD SLAM** | 1 | 1 | Deal 6 DAMAGE. Apply 2 BATTLEMARK. | He-Man |
| **THUNDER PUNCH** | 1 | 0 | Deal 12 DAMAGE. If target has BATTLEMARK, gain 2 ENERGY. | He-Man |
| **UNSTOPPABLE FORCE** | 3 | 0 | Deal 32 DAMAGE. This card costs 1 less ENERGY if you have SHIELD. | He-Man |
| **VENOM FLASK** | 0 | 0 | Consumable. Apply 5 POISON to all enemies. | He-Man |
| **WRATH OF GRAYSKULL** | 3 | 0 | Consumable. Super Attack Mode. Deal DAMAGE to all enemies! | He-Man |
| **YOUR TURN!** | 1 | 0 | Ultimate. Give an extra turn to an ally. | He-Man |
| **ZOAR** | 1 | 0 | Ultimate. Draw 3 cards. For each Attack drawn, play it immediately at no ENERGY cost. | He-Man |

# Relics

These are the relics observed during runs; it is not believed to be an exhaustive list.

| Relic Name | Description |
| :--- | :--- |
| **ALCHEMIST FLASK** | 33% chance to keep a Consumable card when it is played. |
| **BATTLE HARNESS** | Begin battle with at least 2 POWER (power is capped at 6). |
| **CHAIN OF CONFLICT** | Unspent POWER carries over to the next battle. |
| **CHEST OF TREASURES** | No Gold is lost when knocked out. |
| **FIRE JEWEL** | At the start of every round, apply 3 BURN to a random ally or enemy. |
| **IMMUNITY STONE** | At the start of each battle, a random ally & enemy each gain IMMUNITY. |
| **MERCHANT SIGIL** | 40% discount at Trading Post and Marketplace. |
| **PRIMEVAL POTION** | All potion healing effects are increased by 100%. |
| **REBIRTH AMULET** | When knocked out, recover to full HP at the start of the next battle. |
| **SHIELD OF ETERNIA** | Your and enemies' SHIELD no longer expire after each round. |
| **SKELETOR'S SPOILS** | Dealing a fatal blow awards 15 Gold. |
| **SNACK PACK** | Heals 8 HP after battle. |
| **SPARE WRENCH** | Campfire and Battle Scar cards cost nothing to Burn. |
| **THE HOURGLASS** | Refresh yourself every time you skip a turn. |
| **VICTORY FEAST** | In trials, Gold reward increases 50%. |
| **VIPER IDOL** | At the start of every round, apply 3 POISON to a random ally or enemy. |

# Status Effects

| Effect / Term | Category | Description / Details |
| :--- | :--- | :--- |
| **ATTACK** | Card Type | Cards with a red frame deal direct DAMAGE to targets. |
| **BATTLEMARK** | Debuff | Takes extra damage equal to BATTLEMARK for one round. |
| **BLEED** | Debuff | When attacking with BLEED, take DAMAGE equal to BLEED. BLEED is not reduced over turns. |
| **BURN** | Debuff | At turn start, takes DAMAGE equal to BURN, then reduces BURN by 1. |
| **CAMPFIRE** | Card Disposition | This card is not drawn during battle. Burning this card at the campfire activates its effects. |
| **DAMAGE** | Battle Effect | Reduces the target's HP. |
| **DEFENSE** | Card Type | Cards with a blue frame apply SHIELD or heals. |
| **EMPOWER** | Buff | Next Attack deals DAMAGE multiplied by EMPOWER. EMPOWER is triggered and removed after the attack.<br><br>*Editor's Note:* The character retains the EMPOWER buff until performing an attack. By not playing an attack, EMPOWER persists between rounds and can be stacked up to 8x. |
| **ENERGY** | Resource | Resource used to play cards. |
| **HP** | Resource | Health points. At 0 health points, you get knocked out, lose 20% Score and Gold, and add 2 Battle Scar cards into your deck. |
| **IMMUNITY** | Buff | Takes no direct attack DAMAGE for one round. **Does not block POISON or BURN status application.** |
| **INSPIRATION** | Buff | Deals additional DAMAGE equal to INSPIRATION for next Attack. INSPIRATION is then triggered and removed after the attack. |
| **POISON** | Debuff | Inflicts damage at the start of turn equal to stack count. Can be applied during IMMUNITY. |
| **POWER** | Resource | A shared resource that builds up when players use cards with POWER. Unleash Power cards can spend all POWER for stronger effects. |
| **RESISTANCE** | Buff | Prevents gaining negative effects for one round. |
| **SHATTER** | Battle Effect | Removes all SHIELD instances from the target. |
| **SHIELD** | Buff | Blocks the next ATTACK. Unused SHIELD expires after one round. |
| **SKILL** | Card Type | Cards with a green frame perform special actions other than damage, shielding or healing. |
| **SUPER ATTACK MODE** | Action | For a short time, everyone swipes as many cards as possible to create SUPER ATTACK MODE. The more SUPER ATTACK MODE made, the bigger the total damage split evenly among the enemies. |
| **SUPER DEFENSE MODE** | Action | For a short time, everyone swipes as many cards as possible to create SUPER DEFENSE MODE. The more SUPER DEFENSE MODE, the bigger the total healing, split evenly among the allies. |
| **TAUNT** | Debuff | All enemies with single-target Attack must target you. |
| **TEMPORARY** | Status Modifier | **Editor's Note:** Card remains active and present in the draw pool for the entire duration of the battle, rather than single-turn expiry. |
| **UNLEASH POWER** | Card Disposition | Consumes all POWER to power up this card's effects. |
| **ULTIMATE** | Card Disposition | This card can only be played once per battle, then removed from your deck until end of the battle. |

# Biomes & Realms

Regions in the game are referred to alternatively as "realms" or "biomes". The official listing on the Amazon Luna store page states, "...battle your way through a variety of diverse biomes and obstacles with every playthrough...". In-game text refers to the regions as "realms". This guide prefers "biomes" to align with external source references.

| Biome Name | Miniboss / Elite Leader | Boss | Boss HP |
| :--- | :--- | :--- | :---: |
| **1. EVERGREEN** | Moaty | Anti-Eternia Teela | 60 HP |
| **2. SNAKE MOUNTAIN** | Kobra Khan | King Hiss | 80 HP |
| **3. VINE JUNGLE** | Mosquitor | Anti-Eternia Man-at-Arms | 140 HP |
| **4. ICE MOUNTAINS** | Shokoti | Anti-Eternia He-Man | 165 HP |
| **5. FRIGHT ZONE** | Scare Glow | Hordak | 250 HP |
| **6. ANTI-ETERNIA** | Faker | Anti-Eternia Ram Man | 300 HP |

*Editor's Note on Biome 6:* Some sources state that the final boss of the game is Faker. Faker serves as the leader for the Elite Battle nodes in Biome 6. However, he is not the biome's final boss; Faker appears alongside Anti-Eternia Ram Man in the final encounter, where Anti-Eternia Ram Man serves as the true final boss with the highest HP pool (300 HP).

# Playthrough Session Overviews

### Playthrough 1: Fast-Cycling 13-Card Deck Engine
Focuses on extreme deck pruning, dual-Zoar turn-1 cycling, and save-scumming shop inventories for maximum gold efficiency. (See full step-by-step transcript below).

### Playthrough 2: Status Exploits & Endgame Build Variations
Highlights from the second solo He-Man clear:
* **Hordak Defeated With:**
  * **Relics:** IMMUNITY STONE, MERCHANT SIGIL, CHAIN OF CONFLICT, SHIELD OF ETERNIA, REBIRTH AMULET.
  * **Deck Engine:** SHATTER STRIKE (x2), UNSTOPPABLE FORCE, I HAVE THE POWER, PURIFYING SHIELD, CALL TO ARMS, CASTLE GRAYSKULL, SOOTHING SHIELD, MAGIC MIRROR, SORCERESS'S ELIXIR, POWER UP!, YOUR TURN!, ZOAR.
* **Anti-Eternia Ram Man Defeated With:**
  * **Relics:** IMMUNITY STONE, MERCHANT SIGIL, CHAIN OF CONFLICT, SHIELD OF ETERNIA, SNACK PACK.
  * **Non-Campfire Cards:** MIGHTY BATTLE AXE, SHATTER STRIKE (x2), UNSTOPPABLE FORCE, I HAVE THE POWER, PURIFYING SHIELD, CALL TO ARMS, CASTLE GRAYSKULL, SOOTHING SHIELD, CRYSTAL BALL, MAGIC MIRROR (x2), SORCERESS'S ELIXIR, BATTLE PLAN, POWER UP!, YOUR TURN!
  * **Campfire Cards:** GIANT MARSHMALLOW, MARSHMALLOW (x3).

### Playthrough 3: Record High Burst Peak (1,784 Damage OTK)
High-burst setup against Anti-Eternia Ram Man in Biome 6:
* **Relics Owned:** IMMUNITY STONE, SHIELD OF ETERNIA, CHAIN OF CONFLICT, MERCHANT SIGIL, SNACK PACK.
* **Deck Contents:** SHATTER STRIKE, SHIELD SLAM, SWIFT STRIKE, THUNDER PUNCH, BATTLE CAT, ATTACK!, UNSTOPPABLE FORCE, I HAVE THE POWER, CALL TO ARMS, CASTLE GRAYSKULL, SOOTHING SHIELD, CHAMPION'S ROAR, MAGIC MIRROR, SORCERESS'S ELIXIR (x2), BATTLE PLAN, POWER UP!, YOUR TURN!.
* **Sequence Executed:**
  1. **MAGIC MIRROR** (Targeted and duplicated **POWER UP!**).
  2. Played **POWER UP!** (Original) + **POWER UP!** (Duplicate) $\rightarrow$ 4x EMPOWER.
  3. Played **CHAMPION'S ROAR** $\rightarrow$ Granted +2 INSPIRATION.
  4. Played **BATTLE CAT, ATTACK!** with 54 stored POWER.
* **Damage Delivered:** **1,784 DAMAGE**, establishing the definitive formula for INSPIRATION precedence and EMPOWER scaling.

---

# Gameplay Transcript (Playthrough 1)

This is a structured transcript of the primary documented gameplay session in Masters of the Universe: Legends Unite, organized chronologically by decisions, game states, and overarching strategies. 

As used in this transcript, "regular card" refers to all cards that can be played in battle. It excludes CAMPFIRE cards.

CHOOSE A PATH: Biome 1 Pathing

Choices Available

* Top Path: Battle
* Middle Path: Battle
* Bottom Path: Battle

Choice Made

* Top Path

Game State

*   **Gold:** 50
*   **Relics:** None

* * *

Undocumented actions omitted.

* * *

CHOOSE A PATH: Biome 1 Pathing

Choices Available

* Campfire

Choice Made

* Campfire

* * *

CHOOSE A PATH: Biome 2 Pathing

Choices Available

*   Top Path: Trials of Eternia, Campfire
*   Middle Path: Battle, Battle, Elite Battle, Campfire
*   Bottom Path: Campfire, Battle, Trials of Eternia, Campfire

Choice Made

*   Middle Path

Reason

To aggressively target the Elite battle for high-value card rewards, using your gold reserves to bypass gold-generating paths like the Trials of Eternia.

Game State

*   **Gold:** 352+
*   **Deck Size:** 16 regular cards
*   **Relics:** Shield of Eternia, Spare Wrench, Immunity Stone, Chain of Conflict, Battle Harness

* * *

CHOOSE A CARD: Biome 2, Battle 1 Reward

Choices Available

*   Power Sword
*   Unstoppable Force
*   Champion's Roar

Choice Made

*   Skip

Reason

Power Sword's negative self-debuff ("Suffer 2 BATTLEMARK") was deemed too dangerous for a solo run, and the other choices did not provide enough value compared to keeping the deck lean.

Game State

*   **Gold:** ~360+
*   **Health:** 90 / 90 Max HP

* * *

CHOOSE A CARD: Biome 2, Battle 2 Reward

Choices Available

*   Swift Strike
*   Thunder Punch
*   Shield Up

Choice Made

*   Thunder Punch (Second copy)

Reason

To improve on your energy-refund loop; hitting a BATTLEMARK-ed enemy with Thunder Punch provides a net-positive ENERGY gain.

Game State

*   **Deck Size:** 17 regular cards

* * *

CHOOSE A CARD: Biome 2 Elite Reward

Choices Available

*   King's Fury
*   Purifying Shield
*   Wrath of Grayskull

Choice Made

*   Purifying Shield

Reason

Provides healing for each instance of SHIELD.

Game State

*   **Gold:** ~400+
*   **Health:** 90 / 90 Max HP
*   **Deck Size:** 18 regular cards

* * *

CAMPFIRE DECISION: Biome 2 Node Tuning

Choices Available

*   Burn Card (Paid deck thinning)

Choice Made

*   Burn 1 Shield, 1 Strike, and 1 Snack Break (across consecutive campfires). It is possible to Rest at any campfire, whether or not any cards are burned. Resting heals 20% of max HP but can be improved by burning Campfire cards.

Reason

Basic starter defense and weak 5 HP heals became obsolete after acquiring the Shield of Eternia plus Purifying Shield.

Game State

*   **Gold:** 592
*   **Deck Size:** 15 regular cards (Completely starter-free)

* * *

CHOOSE A CARD: Biome 2 Boss (King Hiss) Reward

Choices Available

*   Inspire Hope
*   Power Up!
*   Your Turn!

Choice Made

*   Power Up!

Reason

EMPOWER acts as a massive damage multiplier that primes He-Man to one-shot heavy targets with finishers.

Game State

*   **Health:** 90 / 90 Max HP
*   **Deck Size:** 16 regular cards

* * *

CHOOSE A RELIC: Biome 2 Boss cleared

Choices Available

*   Primeval Potion
*   Rebirth Amulet
*   Chain of Conflict

Choice Made

*   Chain of Conflict

Reason

Allows you to safely stall and stack massive Power buffs at the end of minor battles, entering Boss and Elite rooms with high stored POWER on turn 1.

* * *

STRATEGIC DECISION: The Save-Scumming Merchant Strategy

Summary

Throughout the run, you established that exiting to the main menu and reloading the game successfully re-rolls merchant inventories. You chose to aggressively hold onto your gold hoards to save-scum shops exclusively for top-tier items.

* * *

MARKETPLACE BUNDLE: Biome 3 Shop

Choices Available

*   Royal Onslaught & Box of Traps bundle (117 gold)
*   Reroll via Reload Exploits

Choice Made

*   Reroll, Purchased **Zoar & Purifying Shield** bundle

Reason

The first bundle offered bad synergies. The re-rolled bundle offered a second copy of Zoar (doubling turn-one draw frequency) and a second Purifying Shield.

Gold

*   **Gold:** 642, decreased to 525 after buying the bundle.

* * *

STRATEGIC DECISION: Unrecorded Biome 2/3 Transition Burn

Summary

Note: An unrecorded card burn occurred at the last Campfire of Biome 2 or first Campfire of Biome 3. The burn reduced the deck from 16 cards to 15 cards, removing a remaining basic or weak card. This achieved the target 15-card starter-free composition before entering Biome 3 encounters.

* * *

STRATEGIC DECISION: The "Absolute Shield" Keep Policy

Summary

You originally intended to prune _Shatter Strike_ to lean out the deck. However, you realized that in this game, enemy "Absolute Shields" block all incoming damage regardless of how hard an attack hits unless a _Shatter_ effect is used. You pivot to permanently keeping _Shatter Strike_ to act as an essential key to unlock your big finishers.

* * *

CHOOSE A CARD: Biome 3, Battle 1 Reward

Choices Available

*   Hero's Fist
*   Crater Kick
*   Power Sword

Choice Made

*   Skip

Reason

To preserve the 15-card starter-free balance so your dual-Zoar engine draws combo elements quickly. Rejection of Power Sword re-confirmed due to self-debuff risk.

Game State

*   **Deck Size:** 15 regular cards

* * *

CHOOSE A CARD: Biome 3, Battle 2 Reward

Choices Available

*   Rapid Strike
*   Frenzy Strike
*   Bring It On

Choice Made

*   Frenzy Strike

Reason

Frenzy Strike is an elite high-roll finisher when used against enemies who inflict BATTLEMARK to you. 

Game State

*   **Deck Size:** 16 regular cards

* * *

TRADING POST RELICS: Biome 3 Shop

Choices Available

*   Roll 1: Berserker's Oath, Fire Jewel, Snack Pack
*   Roll 2: Skeletor's Spoils, Meditation Stone, The Hourglass
*   Roll 3: Battle Harness and Cosmic Gem

Choice Made

*   Purchased **Battle Harness**

Reason

Starting with 2 POWER feeds into your _Chain of Conflict_ engine. However, it is risky to take Battle Harness because it limits maximum POWER to 6.

Game State

*   **Gold:** 525

* * *

CHOOSE A CARD: Biome 3 Boss (Anti-Man-At-Arms) Reward

Choices Available

*   Grayskull's Hero
*   Your Turn!
*   Wrath of Grayskull

Choice Made

*   Your Turn!

Reason

You deduced that since the Immunity Stone targets a random "ally" and successfully hits He-Man in solo play, the word "ally" includes yourself. Taking _Your Turn_ was a calculated gamble to secure an extra turn mechanic, with the fallback plan of burning it if it failed.

Game State

*   **Deck Size:** 17 regular cards

* * *

CHOOSE A RELIC / ARTIFACT: Biome 3 Boss cleared

Choices Available

*   Merchant Sigil
*   Alchemist Flask
*   Fire Jewel

Choice Made

*   Merchant Sigil (Discarded **Spare Wrench**)

Reason

Because you hit a strict 5-relic capacity limit, you sacrificed the Spare Wrench. The Merchant Sigil combined with your 903 gold gave you massive purchasing power.

Game State

*   **Gold:** 903
*   **Relic Inventory:** Shield of Eternia, Immunity Stone, Chain of Conflict, Battle Harness, Merchant Sigil.

* * *

STRATEGIC DECISION: The Solo "Your Turn" Breakthrough

Summary

Upon entering Biome 4 (Ice Mountains), you tested _Your Turn_ in combat and confirmed it successfully grants He-Man an entire extra turn in solo play. This elevated your deck by providing a 1-cost time-walk mechanism. Put another way, it provides a net-gain of 2 ENERGY.

* * *

CHOOSE A PATH: Biome 4 Pathing

Choices Available

*   Path 1: Battle path leading to an Elite Battle node.
*   Path 2: Campfire path leading to a mystery node, two Trials of Eternia, and a Marketplace.

Choice Made

*   Path 2 (The Campfire/Event route)

Reason

Low risk and high utility. Because your deck was already winning, you focused on non-combat nodes to let your _Merchant Sigil_ multiply your buying opportunities safely. 

* * *

STRATEGIC DECISION: Unrecorded Biome 4 Event/Shop Acquisition

Summary

Note: An unrecorded card acquisition occurred during Biome 4 Path 2 (via the Mystery Event Node or Marketplace), bringing the deck size from 17 to 18 cards prior to the Biome 4 Boss encounter.

* * *

CHOOSE A CARD: Biome 4 Boss (Anti-He-Man) Reward

Choices Available

*   Shatter Strike
*   Grayskull's Hero
*   Inspire Hope

Choice Made

*   Skip

Reason

To keep your rotation completely un-diluted so you draw into _Your Turn_ or your dual _Zoar_ loops immediately on turn one.

Game State

*   **Health:** 90 / 90 Max HP
*   **Deck Size:** 18 regular cards
*   **Relics:** Skipped reward relic to preserve your 5 flawless active relics.

* * *

CHOOSE A CARD: Biome 5 (Fright Zone) Standard Battle Reward

Choices Available

*   Royal Charge (Second Copy)
*   Miscellaneous pool cards

Choice Made

*   Royal Charge (Second Copy)

Reason

Having two copies of Royal Charge (32 damage) combined with two copies of Zoar maximized the math that you would pull a free 32+ damage attack on turn one.

Game State

*   **Deck Size:** 19 regular cards

* * *

CAMPFIRE DECISION: Fright Zone Node

Choices Available

*   Burn Radiant Defense (Recently acquired co-op card)
*   Keep

Choice Made

*   Burn Radiant Defense

Reason

It required your health to drop below 50% to trigger its defensive traits. Because you are playing solo with an elite shield baseline, conditional co-op blocks are dead weight.

Game State

*   **Gold:** ~900+ (Easily absorbed the scaling card-burn gold penalty)

* * *

CHOOSE A CARD: Biome 5 Elite Reward

Choices Available

*   Soothing Shield
*   Miscellaneous pool cards

Choice Made

*   Skip

* * *

STRATEGIC DECISION: The Anti-Hordak Tactical Shift

Summary

Facing **Hordak**, you encountered a severe wall due to his BLEED and BURN mechanics punishing high-speed card play. After a battle reload, you formulated a strict structural pivot:

1.  Maximize card plays **exclusively on Turn 1** while your _Immunity Stone_ completely protects you from direct DAMAGE during Turn 1 of combat.
2.  Use _Your Turn!_ on Turn 1 to pile on maximum damage while completely safe.
3.  Once Turn 1 ends and you are afflicted, freeze your deck speed. Stop cycling minor attack cards and only play 1-2 heavy finishing attacks per round to minimize BLEED damage.
4.  Prepare to prune the deck layout down to a 10–12 card hyper-focused format in Biome 6 to pull shields reliably.

* * *

STRATEGIC DECISION: Mid-Run Transition Acquisitions & 5-Card Prune Sequence (Pre-Anti-Ram Man Setup)

Choices Available

*   Option 1: Retain setup velocity and redundant attacks (including both copies of Zoar, Thunder Punch, Royal Charge, and Frenzy Strike) to maximize draw speed.
*   Option 2: Integrate late-biome defensive/utility pickups (Castle Grayskull, Guardian's Tonic, Magic Mirror) and execute an aggressive 5-card prune sequence across mid-run Campfire nodes to purge non-damaging velocity cards and redundant attacks before entering Biome 6.

Choice Made

*   Option 2 (Late Acquisitions + Aggressive 5-Card Prune Sequence)

Reason

Non-damaging velocity cards like Zoar diluted the draw engine against BLEED and BURN bosses, while secondary attack cards stole draws from critical defense and heavy burst combinations. An alternative perspective on Zoar is that it is useful to increase the number of cards drawn and useful to play cards a no cost. Since Zoar has the Ultimate attribute, its risk of diluting the draw engine is minimized.

Cards Acquired (Late Biome 5 / Pre-Biome 6)

1.  **Castle Grayskull**
2.  **Guardian's Tonic**
3.  **Magic Mirror**

Cards Pruned Across Sequence

1.  **Zoar (First copy)**
2.  **Thunder Punch**
3.  **Royal Charge**
4.  **Frenzy Strike**
5.  **Zoar (Second copy)**

Game State

*   **Pre-Prune Deck Size:** 22 Cards, including late acquisitions: Castle Grayskull, Guardian's Tonic, Magic Mirror
*   **Post-Prune Deck Size:** 17 Cards
*   **Remaining Deck (17 Cards):** Mighty Battle Axe, Shatter Strike, Sword Slam, Thunder Punch, Royal Charge, Unstoppable Force, I Have the Power, Purifying Shield (x2), Castle Grayskull, Guardian's Tonic, Radiant Defense, Crystal Ball, Magic Mirror, Battle Plan, Power Up!, Your Turn!.

* * *

STRATEGIC DECISION: Biome 6 Deck Optimization & Pathing

Choices Available

*   Route Option A: High-risk elite paths with potential high-value utility drops.
*   Route Option B: Safe non-combat path consisting of Campfire -> Trials of Eternia -> Campfire to execute maximum deck pruning.

Choice Made

*   Route Option B (Safe Non-Combat Path)

Reason

Eliminating RNG combat risks while purging redundant cards compresses the draw engine down to 13 cards, ensuring probable turn 1 or turn 2 draws of essential defense cards (Castle Grayskull, Radiant Defense).

Game State

*   **Character:** He-Man
*   **Location:** Biome 6 (Anti-Eternia)
*   **Pre-Pruning Deck Size:** 17 Cards
*   **Deck Contents:** Mighty Battle Axe, Shatter Strike, Sword Slam, Thunder Punch, Royal Charge, Unstoppable Force, I Have the Power, Purifying Shield (x2), Castle Grayskull, Guardian's Tonic, Radiant Defense, Crystal Ball, Magic Mirror, Battle Plan, Power Up!, Your Turn!.

* * *

CHOOSE A CARD TO PRUNE: Campfire #1

Choices Available

*   Sword Slam
*   Shatter Strike
*   Crystal Ball
*   Magic Mirror
*   Other remaining deck cards

Choice Made

*   Sword Slam, Shatter Strike

Reason

Secondary mid-tier attack cards that dilute the attack pool and steals draws from high-priority defense setups. Recall that I Have the Power includes the SHATTER effect, reducing the usefulness of Shatter Strike.

Game State

*   **Deck Size:** 15 Cards

* * *

CHOOSE A PATH: Trials of Eternia Node

Choices Available

*   Earn gold

Choice Made

*   Earn gold

Game State

*   **Deck Size:** 15 Cards

* * *

CHOOSE A CARD TO PRUNE: Campfire #2

Choices Available

*   Crystal Ball
*   Magic Mirror
*   Other remaining deck cards

Choice Made

*   Crystal Ball

Reason

Slow utility setup that consumes actions without dealing damage or providing immediate block, exposing the character to heavy early-turn boss damage.

Game State

*   **Deck Size:** 14 Cards

* * *

CHOOSE A CARD TO PRUNE: Final Campfire / Prune Node

Choices Available

*   Magic Mirror
*   Your Turn!
*   Other remaining deck cards

Choice Made

*   Magic Mirror

Reason

Pruning Magic Mirror achieves the target 13-card deck threshold, guaranteeing rapid cycling via Battle Plan and Unstoppable Force. However, another perspective is that keeping Magic Mirror would have allowed for the possibility of duplicating Battle Plan or Power Up!, making it possible to reach high damage output earlier in the battle.

Game State

*   **Final Deck Size:** 13 Cards
*   **Final Deck List:** Mighty Battle Axe, Thunder Punch, Royal Charge, I Have the Power, Power Up!, Battle Plan, Castle Grayskull, Radiant Defense, Purifying Shield (x2), Guardian's Tonic, Unstoppable Force, Your Turn!.

* * *

STRATEGIC DECISION: Retaining "Your Turn!"

Summary

Evaluated whether to prune "Your Turn!" to drop total deck size to 12 versus retaining it at 13 cards. Chose to retain "Your Turn!" because at a 13-card deck size, it provides +2 net ENERGY gain, giving the resources needed to set up Castle Grayskull and execute attacks on the same turn.

Game State

*   **Target Boss Ahead:** Biome 6 Guardian / Final Encounter

* * *

STRATEGIC DECISION: Combat Execution & Turn-by-Turn Engine vs. Anti-Eternia Ram Man

Summary

Faced Anti-Eternia Ram Man (the true final boss of Biome 6) after discovering Faker was not the end-boss. Evaluated direct aggression versus defensive stacking. Chose to hold direct attacks to accumulate multi-turn non-attack multipliers, maintaining defense/immunity coverage, and striking with a single massive burst. Skipping attacks allowed the EMPOWER multiplier to stack up to 6x across turns while 0-cost/low-cost shields absorbed incoming damage.

Game State

*   **Location:** Biome 6 Final Encounter
*   **Enemy:** Anti-Eternia Ram Man
*   **Combat Calculation:** Base Heavy Attack (32 damage) x Stacked Multiplier (6x) = 192 total damage in a single turn.
*   **Outcome:** Victory; Anti-Eternia Ram Man defeated; Biome 6 cleared; Credits rolled.
