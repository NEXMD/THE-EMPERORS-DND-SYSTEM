# Light Hammer

**Record:** Weapon 001  
**Passive:** Quick Impact  
**Active skill:** Rapid Impact  
**Status:** Core concept documented; numerical weapon values remain TBD.

## Weapon identity

The Light Hammer's established identity centres on an accurate opening attack followed by a rapid second strike.

## Passive — Quick Impact

> Gain an accuracy bonus on the first attack against an enemy each turn.

The size and exact numerical implementation of the accuracy bonus have not yet been specified.

## Active — Rapid Impact

**Action cost:** Action  
**Target:** One enemy  
**Attacks:** Two separate D20 attack rolls  
**Damage:** Each strike's damage is resolved independently.

### Resolution

1. Select one enemy.
2. Make the first D20 attack roll. The first strike receives the Quick Impact accuracy bonus.
3. Resolve the first strike's damage.
4. Make the second D20 attack roll. The second strike does not receive the Quick Impact accuracy bonus.
5. Resolve the second strike's damage independently.

### Established constraints

- The second strike proceeds even if the first strike misses.
- Both strikes are committed to the same target.
- If the first strike defeats the target, the second strike is wasted.
- The second strike cannot be redirected to another enemy.
- Players do not see exact enemy health, so they cannot reliably know whether the first strike was lethal before the second strike resolves.

### Possible outcomes

| First strike | Second strike | Result |
|---|---|---|
| Hit | Hit | Both strikes connect |
| Hit | Miss | Only the first connects |
| Miss | Hit | Only the second connects |
| Miss | Miss | Neither connects |

## Values not yet established

| Attribute | Status |
|---|---|
| Accuracy bonus amount | TBD |
| Base damage | TBD |
| Range | TBD |
| Other weapon statistics | TBD |

Do not assign numerical values until they are decided and approved.

## Design decisions

- **Rapid Impact** was selected as the active skill.
- The two-strike implementation follows Option A: two consecutive attacks against one target, with separate D20 rolls and independently resolved damage.
- The first strike benefits from Quick Impact; the second does not.
- The target cannot be changed between strikes.
