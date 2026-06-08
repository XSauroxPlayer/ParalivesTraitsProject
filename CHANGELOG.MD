# Changelog

## 1.0.0

First public release. Everything here is new.

### What's in it

- A trait selection panel built into the character creation screen, next to the profile UI.
- Traits come from a JSON file, so you can add or change them without touching any code.
- Each trait can have its own icon, loaded from an image in the Resources folder.
- Hover a trait in the list to see its name and description in a tooltip.
- A cap on how many traits a character can have, with per-life-stage limits you can set in a small settings panel.
- A Randomize button that fills in a valid set of traits for the current character.
- Traits save with your game and come back on load, including after you delete a save.
- A public API: any BepInEx mod can depend on this one and read a character's traits at runtime with `TraitsManager.GetTraits()`.
