# Project: Company of Heroes Board Game 2E – dice counter

Single-file web app (`index.html`, plain HTML/CSS/JS, mobile-friendly, state in `localStorage`). It counts damage dice and calculates defence dice for a chosen target. Dice types and targets are data lists (`DAMAGE`, `TARGETS`, `COVER`) at the top of the script. A later goal is rolling dice and calculating combat results.

## Damage dice
Anti-Infantry, Armor Piercing, High Explosive (HE), Flame (special).

## Targets
Infantry (green), Light armour (yellow), Heavy armour (red), Emplacement (purple), Building (black house).

## Defence matrix
Columns: Anti-Infantry / Armor Piercing / HE / Flame.

| Target       | AI | AP | HE | Flame |
|--------------|----|----|----|-------|
| Infantry     | -  | R  | -  | -     |
| Light armour | R  | -  | R  | -     |
| Heavy armour | X  | S  | R  | X     |
| Emplacement  | R  | R  | -  | -     |
| Building     | X  | X  | -  | -     |

Key: `-` = no defence, R = resistance (1 resistance die per damage die), S = 2 frontal static defence dice regardless of how many damage dice, X = invulnerable.

## Rules implemented
1. **Resistance:** one die per damage die of that type, where the matrix says R.
2. **Battlefield defence (Infantry only, one at a time):** None 0, Yellow 1, Green 2, Grey (standard building) 3, Purple (destroyed building) 1 static dice.
3. **Bonus static dice:** a unit can have one or more, set with a counter.
4. **Flame:** bypasses all defence (resistance and static) unless the target is invulnerable. Static dice (battlefield and bonus) only count when at least one non-flame damage die is present that the target isn't invulnerable to.
5. **HE can miss:** only hits and crits give resistance dice and count as exposure for static dice. Separate Hit and Crit counters; hits plus crits never exceed the HE dice count.
6. **Total damage done:** 1 per die. HE hit = 1, HE crit = 2, HE miss = 0. Damage types the target is invulnerable to are excluded. Flame damage is shown in parentheses, e.g. `4 (2)`, and is included in the total.
7. **Statistics:** total damage done, and resistance plus static defence dice (shown as `–` with no target).

## Open points
- The grey shield in the matrix image has a small star that was not interpreted. Check that cell against the rulebook.
- Dice names and the matrix were taken from the user's images; verify against the 2E rulebook.
