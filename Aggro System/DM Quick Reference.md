# Aggro System — DM Quick Reference

This is a quick reference to the full canonical rules in [README.md](README.md). If any summary here appears to conflict with the full rules, the full rules are authoritative.

## Six tiers

| Tier | Name | Key rule |
|---:|---|---|
| 0 | Base Aggro | 100 for every player. |
| 1 | Player's Aggro | 100 - 2 × (Modified CHA - 10); final minimum 30. |
| 2 | Player's Aggro (Stealth) | Stealth skill modifier reduces Player's Aggro by 0–20% while unseen. |
| 3 | Player's Aggro in Combat | Add encounter-start modifiers and accumulated combat aggro. |
| 4 | Aggro Decay | -5 per turn without attacking/healing; floor 0. |
| 5 | End of Combat | Reset to normal Tier 1 Player's Aggro. |

## Combat aggro sources

| Source | Aggro |
|---|---:|
| Normal character damage | 1 damage = +1 |
| Tank damage | 1 damage = +2 |
| Effective healing | 1 HP restored = +1 to healer |
| Overhealing | 0 |
| HP loss | floor(HP lost in each separate damage event ÷ 5) |
| Poison, burning, other DoT | 0 |
| Taunt | DM guideline: Minor +5–10; Moderate +11–20; Strong +21–30; Exceptional +31–40 |
| Failed Intelligent Support Detection | Small DM-determined amount |

The healed player receives 0 aggro from the healing. Damage and healing aggro accumulate throughout the encounter.

## Encounter-start modifiers

**Low-INT enemy size adjustment only**

| Size | Modifier |
|---|---:|
| Tiny | -10 |
| Small | -5 |
| Medium | 0 |
| Large | +5 |
| Huge | +10 |
| Gargantuan | +15 |

**Enemy instinct:** DM-selected instinct targets receive +10% of their Player's Aggro once at combat start. It does not accumulate or force targeting.

**Intelligent Support Detection:** One CHA check at combat start. Success: no extra aggro. Failure: small DM-determined aggro.

## Stealth reduction

Use Stealth skill modifier, not DEX.

| Stealth modifier | Reduction |
|---:|---:|
| +0 to +1 | 0% |
| +2 to +3 | 2% |
| +4 to +5 | 4% |
| +6 to +7 | 6% |
| +8 to +9 | 8% |
| +10 to +11 | 10% |
| +12 to +13 | 12% |
| +14 to +15 | 14% |
| +16 to +17 | 16% |
| +18 to +19 | 18% |
| +20 | 20% |

Stealth ends on detection, revealing physical contact, attack, healing, or support action. Restore normal Player's Aggro before adding aggro from the revealing action.

## Target selection

Use a weighted spin wheel:

Player probability = (player's current aggro ÷ total party aggro) × 100%

Highest aggro means highest probability, not guaranteed selection. All enemies share one encounter aggro pool. Aggro changes do not automatically force a target switch.

## Aggro Decay

- No attack and no healing on the player's turn: -5.
- Attack or healing: prevents that turn's decay.
- Movement, defensive, and utility actions alone: do not prevent decay.
- Decay applies to all accumulated aggro and cannot reduce it below 0.
- Unconscious: retain aggro, cannot generate more, lose 5 per round unconscious.
- Whether unconscious decay stacks with normal inactive-turn decay, and how retained aggro resumes on revival, remain unresolved.

## DM-controlled

- Instinct governing mixed-species encounters.
- Intelligent Support Detection DC and failure amount.
- Whether a taunt works and its exact amount within the approved range.
- Target choice on equal aggro.
- Special enemy behaviour and when to make a new target selection.

## Rejected

- Proximity-based aggro adjustments.
- Separate aggro tables for every enemy.

See [the full Aggro System rules](README.md) for enemy-instinct examples, enemy intelligence categories, formulas, examples, and unresolved edge cases.
