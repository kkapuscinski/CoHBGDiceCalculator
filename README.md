# CoHBGDiceCalculator
Static calculator for damage and defence dice in Company of Heroes Board Game 2E.

## Importing rulebook graphics

1. Add individual SVGs or transparent PNGs cleared for redistribution to `assets/icons/`. Use lowercase, hyphenated filenames, such as `anti-infantry.svg`.
2. Set `icon: './assets/icons/anti-infantry.svg'` on the matching entry in `DAMAGE`, `TARGETS`, or `COVER` in [index.html](./index.html). Keep the path relative so it works on GitHub Pages. The image is decorative; the text label stays visible and works without an icon.
3. Record the source, rulebook edition, redistribution permission, and any required attribution for each asset below.

The [GitHub Pages workflow](./.github/workflows/deploy-pages.yml) copies the `assets` directory into the published site when it exists. No build step is needed to preview the page locally.

### Artwork credits

The damage-dice badges, target icons (colored hearts and a black house), and blue shield shared by Unit bonus and the Battlefield defence options that grant dice in [`assets/icons/`](./assets/icons/) are original placeholders, not rulebook artwork. To use cleared artwork later, replace each PNG in place or update its image path in [index.html](./index.html) if the filename or format changes. Record the new artwork's credits here.
