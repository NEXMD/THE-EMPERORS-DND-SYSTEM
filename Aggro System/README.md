# Aggro System

**Priority:** 1 on the Ideas & Development Priority List  
**Status:** Design record; incomplete  
**Current Weapon Mastery work remains separate.**

## Core concept

Every player has an aggro value that influences how likely enemies are to target them. The system is intended to make enemy targeting more dynamic than simply attacking whoever is closest.

The Aggro System and Weapon Mastery are separate systems. Do not assume they interact unless that interaction is approved.

## Recorded mechanics

### Base aggro

Every player starts with **100 base aggro**.

### Creature size modifier

Creature size modifies aggro only against enemies with low Intelligence.

| Creature size | Aggro modifier |
|---|---:|
| Tiny | -10 |
| Small | -5 |
| Medium | 0 |
| Large | +5 |
| Huge | +10 |
| Gargantuan | +15 |

### Charisma

- Use the actual Charisma ability score, not the Charisma modifier.
- Higher Charisma lowers aggro.
- A Charisma score of 10 is the neutral reference point.

**Formula discussed — proposal only, not a confirmed final rule:**

Aggro = 100 - 2 × (CHA - 10)

Do not treat this formula as finalized.

### Stealth

- Stealth can lower aggro.
- Its effect only applies while the player remains unseen.
- Physical contact cancels the stealth-based aggro reduction.
- Stealth and Charisma can stack.
- Stealth is automatically cancelled if an enemy notices the player.

### Healing and support

- Healing and support actions can attract enemy attention.
- A healer who heals or supports allies can become a target.
- The design intent is for healers to face the risk of attracting aggro.

## Target-selection design principles

- The system should be manageable for both players and the DM.
- Avoid mechanics that require excessive tracking.
- Small changes in aggro should not automatically change the enemy's target.

## Unfinished details

Do not invent these values or procedures:
- Final Charisma formula.
- Exact numerical Stealth reduction.
- Exact aggro changes from healing and support.
- Complete target-selection procedure.
- Other aggro modifiers and interactions.

Continue from the recorded mechanics and ask the user when a missing detail becomes necessary.

## Development boundary

This page records the current concept and mechanics from the project handover. It does not mean every part of the Aggro System is complete, and it does not move the current development focus away from Weapon Mastery.
