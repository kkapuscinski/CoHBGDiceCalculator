# CoHBGDiceCalculator
Static calculator for damage and defence dice in Company of Heroes Board Game 2E.

## Importing rulebook graphics

1. Add individual SVGs or transparent PNGs cleared for redistribution to `assets/icons/`. Use lowercase, hyphenated filenames, such as `anti-infantry.svg`.
2. Set `icon: './assets/icons/anti-infantry.svg'` on the matching entry in `DAMAGE`, `TARGETS`, or `COVER` in [index.html](./index.html). Keep the path relative so it works on GitHub Pages. The image is decorative; the text label stays visible and works without an icon.
3. Record the source, rulebook edition, redistribution permission, and any required attribution for each asset below.

The [GitHub Pages workflow](./.github/workflows/deploy-pages.yml) copies the `assets` directory into the published site when it exists. No build step is needed to preview the page locally.

Keep Damage Dice icons transparent: the calculator draws the white rounded die face behind each symbol.

### Artwork credits

- **Damage dice:** Anti-Infantry, Armor Piercing, High Explosive, and Flame are from the *Company of Heroes Board Game 2nd Edition Rulebook*, section 5.2, “Damage Types” (printed page 17). The icons were cropped and given transparent backgrounds, and are included with permission.
- **Target types:** The G, Y, R, and P hearts and the Building symbol are from the same rulebook, section 5.5, “Resistance Defense Matrix” (printed page 19). The icons were cropped and given transparent backgrounds, and are included with permission.
- **Defense Die:** The shield shared by Unit bonus and Battlefield defence comes from section 5.6, “Static Defenses” (printed page 20), and is included with permission.
- **HE Splash Damage Die:** [`he-splash-damage.png`](./assets/icons/he-splash-damage.png) comes from section 5.3.1, “Damage – HE Splash Damage – Full Game Rules” (printed page 18). It is included with permission as an asset for future use and is not shown in the calculator.
