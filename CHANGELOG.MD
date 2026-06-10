# Changelog

All notable changes to this project will be documented in this file.

## [1.1.2] - Latest

### Added

#### Good Trait Effects
- Parafolk with the **Good** trait gain **+2 Happy** while the emotion is active.
- Parafolk with the **Good** trait gain **+1 Happy** when nearby Parafolk have a positive dominant emotion.
- Parafolk with the **Good** trait do not suffer job performance penalties from negative emotions.

#### Evil Trait Effects
- Parafolk with the **Evil** trait gain **+2 Angry** while the emotion is active.
- Parafolk with the **Evil** trait gain **+1 Happy** when nearby Parafolk have a negative dominant emotion.
- Parafolk with the **Evil** trait convert the job performance penalty from **Angry** into a bonus while Angry is their dominant emotion.

---

## [1.1.1]

### Added
- Implemented the **Goofball** trait effect.

---

## [1.1.0]

### Breaking Changes
- Trait effects are now bundled directly into the main mod.
- The separate effects DLL is no longer required and must be removed.

### Added
- Search bar in the trait selection UI.
- Trait list is now sorted alphabetically by the localized trait name.

### Changed

#### UI
- The Traits section in the character profile is now displayed below the Personality section.
- Trait list ordering now uses the localized trait name instead of the raw English name.
- Trait search now matches against the localized trait name instead of the raw English name.

#### Localization
- Added name and description entries for all **534 traits** across all **8 supported languages**:
  - English (en)
  - Italian (it)
  - German (de)
  - Spanish (es)
  - French (fr)
  - Portuguese (pt)
  - Polish (pl)
  - Chinese (zh)
- Non-English languages currently use English as a placeholder for newly added entries pending translation.
- Trait descriptions now replace `(Parafolk name)` with the character's actual name.

#### Traits
- Disabled **470 traits** that currently have no implemented effect, preventing them from appearing in the trait selection UI.
- **51 traits** with active gameplay effects remain available.

---

## [1.0.0]

First public release.

### Added
- Trait selection panel integrated into the character creation screen next to the profile UI.
- Traits loaded from a JSON file, allowing customization without code changes.
- Support for custom trait icons loaded from the Resources folder.
- Tooltip displaying trait name and description when hovering over a trait.
- Configurable limit on the number of traits a character can have, including per-life-stage restrictions.
- Randomize button that generates a valid set of traits for the current character.
- Full save/load support for traits.
- Public API for other BepInEx mods to access character traits at runtime via `TraitsManager.GetTraits()`.
