# Aggro System

**Priority:** 1 on the Ideas & Development Priority List  
**Status:** Core mechanics established; selected implementation details remain open.  
**Current project focus:** Weapon Mastery. Aggro System remains separately documented.

## Core concept

Every player has an aggro value. Enemies use those values to determine each player's probability of being selected as a target. The player with the highest aggro is more likely to be selected, but is not guaranteed to be selected.

## 1. Aggro calculation

The approved calculation is:

`Aggro = 100 - 2 × (CHA - 10) + S + D + H`

Where:

| Symbol | Meaning |
|---|---|
| 100 | Every player’s starting base aggro |
| CHA | Actual Charisma ability score, not the Charisma modifier |
| S | Applicable creature-size modifier |
| D | Total damage dealt by that player during the current fight |
| H | Total HP restored by that player through healing during the current fight |

### Charisma

- CHA 10 is neutral: it does not change the starting base aggro.
- Every point of CHA above 10 reduces starting aggro by 2.
- Every point of CHA below 10 increases starting aggro by 2.
- Use the actual ability score, not the ability modifier.

The Charisma formula was approved in the earlier project discussion. It is not an unresolved proposal.

## 2. Accumulated damage and healing

Aggro from damage and healing accumulates throughout the entire fight.

| Action | Aggro gained |
|---|---:|
| Deal 1 damage | +1 aggro to the attacker |
| Restore 1 HP through healing | +1 aggro to the healer |
| Receive healing | 0 aggro from that healing |

**Healing aggro belongs entirely to the healer.** The player receiving the healing does not gain aggro from the restored HP.

Damage and healing are cumulative during the fight; they are not limited to the current turn.

## 3. Creature-size modifier

Creature size modifies a player's aggro only when the enemy making the target decision has low Intelligence.

| Player character's size | Modifier |
|---|---:|
| Tiny | -10 |
| Small | -5 |
| Medium | 0 |
| Large | +5 |
| Huge | +10 |
| Gargantuan | +15 |

Against enemies that do not have low Intelligence, this size modifier does not apply.

## 4. Stealth

- Stealth reduces a player's aggro while that player remains unseen.
- The Stealth reduction can stack with the Charisma effect.
- Physical contact cancels the Stealth-based aggro reduction.
- If an enemy notices the player, the Stealth-based reduction is cancelled.

The exact numerical amount of the Stealth reduction has not been established in the recovered decisions.

## 5. Enemy target selection — weighted spin wheel

Target selection uses a spin-wheel website with each party member weighted according to their current aggro.

`Player's selection probability = (Player's aggro ÷ Total party aggro) × 100%`

In other words:

1. Determine each party member's current aggro.
2. Add the party members' aggro values to obtain the total party aggro.
3. Give each player a share of the wheel proportional to their aggro divided by the total.
4. Use the weighted spin to select the enemy's target.

### What this means in combat

- More aggro means a higher probability of being selected.
- The highest-aggro player is not automatically selected every time.
- A player who deals the most damage will generally build substantial aggro.
- A healer can overtake that player if the healer's accumulated healing aggro is greater.
- A change in aggro changes the selection probability; it does not automatically force the enemy to change targets.

## 6. Remaining implementation details

These are the details not established in the recovered discussion. They should not be filled in without the project owner's decision:

- The exact numerical amount by which Stealth reduces aggro.
- Exactly when or how often the weighted spin wheel is used to select or reselect a target.
- Whether non-healing support actions generate aggro, and if so, how much.
- Any additional modifiers or special-case interactions.
- How accumulated values are handled between separate fights.

The core damage, healing, Charisma, size-modifier, and weighted target-selection rules above are established and should not be marked as undecided.

## Development boundary

Aggro System is priority 1 on the ideas list, but Weapon Mastery remains the current development focus. These are separate systems; no interaction between them is assumed unless the project owner approves it.
