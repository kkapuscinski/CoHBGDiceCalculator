# CoHBGDiceCalculator
Static calculator for damage and defence dice in Company of Heroes Board Game 2E.

## Importing rulebook graphics

1. Add individual SVGs or transparent PNGs cleared for redistribution to `assets/icons/`. Use lowercase, hyphenated filenames, such as `anti-infantry.svg`.
2. Set `icon: './assets/icons/anti-infantry.svg'` on the matching entry in `DAMAGE`, `TARGETS`, or `COVER` in [index.html](./index.html). Keep the path relative so it works on GitHub Pages. The image is decorative; the text label stays visible and works without an icon.
3. Record the source, rulebook edition, redistribution permission, and any required attribution for each asset below.

The [GitHub Pages workflow](./.github/workflows/deploy-pages.yml) copies the `assets` directory into the published site when it exists. No build step is needed to preview the page locally.

### Artwork credits

No rulebook artwork is bundled yet.
