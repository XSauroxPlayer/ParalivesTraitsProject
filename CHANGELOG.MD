# Changelog

## 1.0.0

The first public release of The Traits Project. Everything here is new.

### New stuff

- Trait selection panel integrated directly into the character creation screen, positioned alongside the existing profile UI.
- Traits are loaded from a JSON file, making it easy to add or modify entries without touching any code.
- Each trait supports a custom icon loaded from an image file placed in the Resources folder.
- Hovering over a trait in the list shows a tooltip with its name and description.
- Configurable maximum number of traits a character can hold, with per-life-stage overrides available through a dedicated settings panel.
- Randomize button that picks a valid set of traits for the current character automatically.
- Trait data is saved alongside the game save and fully restored on load, including after deleting a save.
- Public API for other mods: any BepInEx plugin can declare a dependency on this mod and query character traits at runtime through `TraitsManager.GetTraits()`.
