# THE EMPEROR'S DND SYSTEM — AGGRO SYSTEM

**Canonical rules record · Version 1.0 · Updated 20 November 2026**

**Status:** The six-tier structure and the listed core mechanics are recorded below. DM-controlled decisions and genuinely unresolved edge cases are kept separate.  
**Priority:** Priority 1 on the Ideas & Development List. Weapon Mastery remains the current development focus.  
**Source of truth:** This document is the full written Aggro System record. The website page is intended to reproduce it. Historical drafts are preserved separately and must not override later approved decisions.

## System purpose

The Aggro System determines how much attention each player attracts and how likely that player is to be selected as an enemy's target. Aggro is cumulative during an encounter. Damage, healing, HP loss, enemy instincts, size, Stealth, taunts, and certain intelligent-enemy interactions can affect a player's aggro.

The system uses one shared aggro pool for the encounter. It is designed to create tactical choices without requiring the DM to maintain a separate aggro table for every enemy.

## The six tiers

| Tier | Name | What it records |
|---:|---|---|
| 0 | Base Aggro | The universal starting value: 100. |
| 1 | Player's Aggro | The character's starting value after Charisma and applicable item effects. |
| 2 | Player's Aggro (Stealth) | The conditional reduction while the character remains unseen and undetected. |
| 3 | Player's Aggro in Combat | The encounter value after applicable starting modifiers and accumulated combat aggro. |
| 4 | Aggro Decay | The reduction when a player does not attack or heal, including the separate unconscious-player rule. |
| 5 | End of Combat | Combat aggro is cleared and the player returns to normal Player's Aggro. |

---

# TIER 0 — BASE AGGRO

Every player begins with **100 Base Aggro**.

A_Base = 100

This is the common reference value before character-specific calculations and encounter modifiers.

---

# TIER 1 — PLAYER'S AGGRO

Player's Aggro is the character's individual starting aggro value. Calculate it when the character enters combat.

## 1. Charisma calculation

Use the character's **actual Charisma ability score**, not the Charisma modifier.

A_CHA = 100 - 2 × (Modified CHA - 10)

- CHA 10 is neutral and produces 100 CHA-adjusted aggro.
- Every point of CHA above 10 reduces aggro by 2.
- Every point of CHA below 10 increases aggro by 2.
- Higher CHA lowers Player's Aggro; lower CHA raises it.

### CHA reference table

| Modified CHA score | CHA-adjusted aggro |
|---:|---:|
| 1 | 118 |
| 2 | 116 |
| 3 | 114 |
| 4 | 112 |
| 5 | 110 |
| 6 | 108 |
| 7 | 106 |
| 8 | 104 |
| 9 | 102 |
| 10 | 100 |
| 11 | 98 |
| 12 | 96 |
| 13 | 94 |
| 14 | 92 |
| 15 | 90 |
| 16 | 88 |
| 17 | 86 |
| 18 | 84 |
| 19 | 82 |
| 20 | 80 |

### Equipment and items

- Equipment that changes the character's CHA changes the CHA score used in the formula.
- An item may also have a direct aggro effect. Apply the effect written for that item.
- The final Player's Aggro cannot be lower than **30**.
- No maximum Player's Aggro has been specified.

The general stacking order for multiple direct item modifiers has not been separately specified; follow the item's own wording and the DM's ruling rather than inventing a universal stacking rule.

### Example

A character has CHA 14. An item raises their CHA by 2.

1. Modified CHA = 14 + 2 = 16.
2. CHA-adjusted aggro = 100 - 2 × (16 - 10).
3. Player's Aggro before any direct item effect = **88**.

If an item also directly modifies aggro, apply that item's stated effect, while respecting the minimum of 30.

---

# TIER 2 — PLAYER'S AGGRO (STEALTH)

Stealth reduces Player's Aggro while the player remains unseen and undetected.

Use the character's **Stealth skill modifier**, not their DEX score.

## 1. Stealth reduction table

| Stealth skill modifier | Aggro reduction | Aggro remaining |
|---:|---:|---:|
| +0 to +1 | 0% | 100% |
| +2 to +3 | 2% | 98% |
| +4 to +5 | 4% | 96% |
| +6 to +7 | 6% | 94% |
| +8 to +9 | 8% | 92% |
| +10 to +11 | 10% | 90% |
| +12 to +13 | 12% | 88% |
| +14 to +15 | 14% | 86% |
| +16 to +17 | 16% | 84% |
| +18 to +19 | 18% | 82% |
| +20 | 20% | 80% |

Every increase of 2 Stealth modifier points increases the aggro reduction by 2 percentage points, up to the listed +20 / 20% entry.

A_Stealth = Player's Aggro × (1 - Stealth reduction)

## 2. Conditions for the Stealth reduction

The reduction applies only while the player remains unseen and undetected.

The Stealth reduction is cancelled when:
- The enemy notices or detects the player.
- The player physically interacts with or touches an enemy in a way that reveals their presence.
- The player attacks.
- The player heals.
- The player performs a supporting action.

CHA-based reduction and Stealth-based reduction can stack.

## 3. Losing Stealth during combat

When Stealth is cancelled, return to the player's normal **Tier 1 Player's Aggro** first. Then add the aggro generated by the action that revealed the player.

Do not continue using the reduced Stealth value after the player has revealed themselves.

### Example

A player has normal Player's Aggro of 88 and is benefiting from Stealth. The player attacks and deals 20 damage.

1. Remove the Stealth reduction.
2. Restore the normal Player's Aggro of 88.
3. Add the damage-generated aggro of 20.
4. The player's combat aggro becomes **108** before any other applicable modifier.

The recovered documents do not specify a decimal-rounding convention for Stealth calculations.

---

# TIER 3 — PLAYER'S AGGRO IN COMBAT

Player's Aggro in Combat is the player's accumulated aggro for the current encounter. It starts from the applicable Player's Aggro value and is adjusted by encounter-start modifiers and aggro generated during combat.

**Damage and healing aggro accumulate throughout the entire fight.** They are not limited to the current turn.

## 1. Encounter-start adjustments

Apply the relevant encounter-start rules when combat begins.

### A. Creature-size modifier — Low-INT enemies only

Creature size modifies aggro **only against Low-INT enemies**. The size modifier is added to the player's aggro at the beginning of combat.

| Player character's size | Aggro modifier |
|---|---:|
| Tiny | -10 |
| Small | -5 |
| Medium | 0 |
| Large | +5 |
| Huge | +10 |
| Gargantuan | +15 |

- Medium is neutral.
- Each size category changes aggro by 5.
- Average-INT and High-INT enemies ignore size-based aggro adjustments.
- The modifier is an encounter-start adjustment, not a new modifier every time the player moves.

### B. Enemy instinct bonus — +10%

Different enemy species may have instincts, personalities, and combat priorities that influence which players attract their attention.

At the beginning of combat:
1. The DM identifies the player or players who match the relevant enemy instinct.
2. Each DM-selected player receives an additional **10% of their Player's Aggro**.
3. This bonus is applied once. It does not accumulate or repeat every round.
4. The bonus makes that player more likely to be selected; it does not force the enemy to attack them.
5. A different player with higher total aggro can still be more likely to be selected.

When multiple enemy species are present, the DM decides which species' instinct governs the encounter. The DM retains control over this decision.

### C. Intelligent Support Detection

Intelligent enemies may recognise a player operating in a rear-guard support role.

This check happens **once at the beginning of combat only**. It is not repeated every round.

1. An intelligent enemy identifies a player operating in a rear-guard support role.
2. The identified player makes a CHA check.
3. On success, the player receives no additional aggro from this check.
4. On failure, the player gains a small amount of additional aggro.

The DM determines:
- The CHA check DC.
- The additional aggro gained on failure.
- Whether the enemy can identify the support player in that situation.

Examples of enemies that may use this behaviour include intelligent humanoids, demons, hunters, elves, humanoid tacticians, and other enemies capable of tactical reasoning.

## 2. Damage-generated aggro

Damage dealt generates aggro.

| Character type | Conversion | Formula |
|---|---:|---|
| Normal character | 1 damage = 1 aggro | Damage dealt × 1 |
| Tank | 1 damage = 2 aggro | Damage dealt × 2 |

- Normal characters generate 1 aggro per 1 damage dealt.
- Tanks generate 2 aggro per 1 damage dealt.
- The Tank multiplier compensates for typically lower damage output and helps Tanks maintain enemy attention.
- The Tank multiplier applies to damage-generated aggro. It does not multiply healing aggro or HP-loss aggro.

## 3. Healing-generated aggro

Healing generates aggro for the **healer**, not the player receiving the healing.

A_Healing = Effective HP Restored × 1

- Every 1 effective HP restored generates 1 aggro.
- Only effective HP actually restored counts.
- Overhealing generates no aggro.
- The healed player receives 0 aggro from that healing.
- A healer can become the highest-aggro player if their accumulated healing aggro exceeds the other players' accumulated aggro.

## 4. HP-loss aggro

Losing HP also generates aggro.

Calculate each separate damage event individually and round down:

A_HP_Loss = floor(HP lost in that event ÷ 5)

Every 5 HP lost generates 1 aggro.

| HP lost in one damage event | Calculation | Aggro gained |
|---:|---:|---:|
| 5 | floor(5 ÷ 5) | +1 |
| 10 | floor(10 ÷ 5) | +2 |
| 20 | floor(20 ÷ 5) | +4 |
| 37 | floor(37 ÷ 5) | +7 |
| 50 | floor(50 ÷ 5) | +10 |
| 100 | floor(100 ÷ 5) | +20 |

**Important:** Calculate every separate damage event separately. Round down each event before adding its aggro to the accumulated total. Do not combine multiple separate hits into one calculation.

Intentionally taking damage to generate aggro is allowed under the current design. The DM considers this an acceptable tactical trade-off because deliberately taking damage endangers the player.

## 5. Damage-over-time effects

Poison damage, burning damage, and other ongoing damage-over-time effects generate **no aggro**.

This exclusion applies even though HP-loss aggro exists for applicable damage events.

## 6. Taunts and aggro manipulation

Taunts and special aggro manipulation may generate additional aggro.

The approved DM reference ranges are:

| Taunt strength | Additional aggro |
|---|---:|
| Minor | +5 to +10 |
| Moderate | +11 to +20 |
| Strong | +21 to +30 |
| Exceptional | +31 to +40 |

The DM decides:
- Whether the enemy responds to the taunt.
- Which strength category applies.
- The exact additional aggro within that category.
- Whether the enemy's intelligence, species, personality, or design makes the taunt effective.

A taunt adds aggro. It does **not** automatically force an enemy to target the taunter.

## 7. Shared aggro pool

All enemies in an encounter use one shared aggro pool.

- Do not maintain a separate aggro table for every enemy.
- Damage, healing, HP-loss aggro, decay, and applicable modifiers change the player's current encounter aggro.
- Enemy instincts and intelligence may influence target selection, while the DM retains control over special behaviour.

## 8. Target selection — weighted spin wheel

Enemy target selection uses a weighted spin-wheel website. Each party member's share is proportional to their current aggro.

P_i = (A_i ÷ Total Party Aggro) × 100%

Where:
- P_i is the player's percentage chance on the wheel.
- A_i is that player's current aggro.
- Total Party Aggro is the combined current aggro of the party.

Procedure:
1. Determine every party member's current aggro.
2. Add the party members' values to get total party aggro.
3. Calculate each player's percentage using their aggro divided by total party aggro.
4. Set the spin-wheel weights using those percentages.
5. Spin to select the target.

The player with the highest aggro has the highest probability, but is **not guaranteed** to be selected. A healer can become the most likely target if their accumulated healing aggro becomes higher than another player's accumulated damage aggro.

Aggro changes alter the wheel weights. They do not automatically force an enemy to switch targets.

The exact mandatory frequency for re-spinning or reselecting a target has not been specified; the DM determines when a new target selection is required.

## 9. Aggro ties

When multiple players have equal aggro, the DM decides which player the enemy targets.

---

# TIER 4 — AGGRO DECAY

Aggro Decay reduces a player's accumulated aggro when they complete a turn without attacking or healing.

A_after_decay = max(0, A_before_decay - 5)

## 1. Normal decay

Every player turn without attacking or healing reduces accumulated aggro by **5**.

| Player action | Prevents the -5 decay? |
|---|---|
| Attacking | Yes |
| Healing | Yes |
| Movement | No |
| Defensive action | No |
| Utility action | No |
| Doing nothing | No |

A defensive or utility action only prevents decay if it also involves attacking or healing.

## 2. What decay affects

Decay applies to **all accumulated aggro**, not only Base Aggro.

This includes:
- Base aggro.
- Damage-generated aggro.
- Healing-generated aggro.
- HP-loss aggro.
- Taunt-generated aggro.
- Other accumulated aggro factors.

Aggro cannot fall below **0**.

Small attacks can reset decay. This is an intentional tactical trade-off because attacking can endanger teammates.

## 3. Unconscious players

- A player at 0 HP retains their accumulated aggro.
- An unconscious player cannot generate additional aggro.
- An unconscious player loses **5 aggro per round** while unconscious.
- Aggro cannot fall below 0.

The exact procedure for whether retained aggro becomes active again immediately upon revival has not been explicitly finalized. Do not invent an additional revival rule.

The recovered decisions also do not explicitly state whether the unconscious-player -5 per round is applied in addition to the ordinary inactive-turn -5 for the same interval. This interaction remains DM-dependent; do not double-count it without a ruling.

---

# TIER 5 — END OF COMBAT

When combat ends, each player's accumulated combat aggro resets to their normal **Tier 1 Player's Aggro**.

A_Combat → A_Player

- Combat-generated aggro does not carry into the next encounter.
- The next encounter begins from the player's normal Player's Aggro, recalculated using their current CHA and applicable equipment.
- The Stealth reduction is conditional and applies only if its conditions are met in the next encounter.

---

# ENEMY BEHAVIOUR & DM GUIDANCE

## 1. Enemy instincts

Different species and creatures may have different instincts, personalities, and combat priorities.

| Creature or enemy type | Example instinct / target preference |
|---|---|
| Wolves | Wounded targets; isolated targets |
| Goblins | Vulnerable-looking targets |
| Spiders | Restrained targets; trapped targets |
| Dragons | Greatest perceived threat |
| Assassins and Hunters | Rear-guard support; strategically important targets |
| Undead | Closest living target |
| Predatory Beasts | Weakest-looking targets |
| Demons | Magical threats; strategically important targets |

These are behavioural tendencies, not mandatory rules. Different species should not necessarily target the same way. The DM retains control over enemy behaviour and chooses which instinct governs a mixed-species encounter.

The +10% instinct bonus is the numerical encounter-start rule. The examples above describe the kind of instinct that may guide the DM's selection.

## 2. Enemy intelligence categories

| Category | Behaviour | Size modifier |
|---|---|---|
| Low-INT | More influenced by physical presence and instinctive targeting. | Applies |
| Average-INT | Uses the general aggro system without size-based adjustments. | Ignored |
| High-INT | Can reason, identify rear-guard support, evaluate threats, and use tactical targeting behaviour. | Ignored |

- Numerical INT thresholds for Low-INT, Average-INT, and High-INT have not been established.
- The DM classifies enemies according to their ability to reason and use tactical behaviour.
- The DM may design intelligent enemies with special targeting behaviour.

## 3. DM-controlled decisions

The DM retains control over:
- Which instinct governs an encounter, particularly when multiple species are present.
- Which players match an enemy's instinct.
- Whether an intelligent enemy can identify a rear-guard support player.
- The DC and failure aggro for Intelligent Support Detection.
- Whether an enemy responds to a taunt, the taunt category, and the exact amount within its range.
- Which player is targeted when multiple players have equal aggro.
- When a new target selection is required.
- Special enemy behaviour based on intelligence, species, personality, and encounter design.

## 4. Rejected mechanics

| Mechanic | Status | Reason |
|---|---|---|
| Proximity-based aggro | **Rejected** | Tracking aggro adjustments every time a player moves would waste DM time. |
| Separate aggro tables for every enemy | **Rejected** | Maintaining separate tables for every enemy would be unnecessarily complicated. |

---

# UNRESOLVED EDGE CASES — DO NOT INVENT RULES

The following points are not fully specified in the recovered decisions. They are listed so that a future edit does not silently turn an assumption into a rule.

1. **AoE damage:** Whether aggro is calculated separately for each enemy hit or once using the total damage dealt.
2. **Mixed-INT encounters:** How the Low-INT size adjustment is applied when Low-, Average-, and High-INT enemies are present together while the encounter uses one shared aggro pool.
3. **Unconscious-player revival:** Whether retained aggro becomes active again immediately upon revival.
4. **Unconscious decay interaction:** Whether the unconscious -5 per round replaces or stacks with normal inactive-turn decay for the same interval.
5. **INT thresholds:** Numerical boundaries for Low-INT, Average-INT, and High-INT enemies.
6. **Stealth decimals:** The rounding convention for percentage reductions that produce fractional aggro.
7. **Target-selection timing:** The mandatory frequency, if any, for spinning the wheel again or selecting a new target.
8. **Direct item modifiers:** A universal stacking order for multiple direct aggro-modifying items.
9. **Combined starting modifiers:** A universal mathematical order for every possible combination of Stealth, size, and enemy-instinct adjustments.

These are unresolved procedures, not permission to change established mechanics.

---

# DESIGN PRINCIPLES & CHANGE CONTROL

1. Keep the system manageable for the DM and players.
2. Avoid unnecessary complexity and excessive bookkeeping.
3. Do not create separate aggro tables for every enemy.
4. Preserve tactical decision-making and meaningful risk.
5. Small changes in aggro do not automatically force a target switch.
6. Treat established rules as existing decisions.
7. Keep DM-dependent rulings and unresolved edge cases clearly labelled.
8. Never silently change a formula, number, condition, or approved mechanic.
9. Do not assume Aggro System and Weapon Mastery interact unless the project owner approves that interaction.
10. The DM has decided not to add more mechanics until further testing.

## Project priority

Aggro System is priority 1 on the Ideas & Development List. Weapon Mastery remains the current development focus. The two systems remain separate unless an interaction is explicitly approved.


## Historical source archive

The original structured draft is preserved unchanged at [Archive/Original Aggro System Draft 1.0-draft.json](Archive/Original%20Aggro%20System%20Draft%201.0-draft.json). It is a historical snapshot; this canonical document records the later approved decisions and supersedes earlier unresolved labels where the user made subsequent decisions.
