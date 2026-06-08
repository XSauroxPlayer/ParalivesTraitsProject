**Creator:** xSauroXplayer | **Game:** Paralives

## Overview

The Traits Project is a BepInEx framework mod for Paralives that introduces a fully functional trait system. It adds a trait selection panel to character creation, loads trait definitions from JSON files, and persists trait data across save files. It also exposes a public API so that other mods can read which traits a character has and build gameplay effects on top of them.

## Setup Requirements

Install BepInEx 5 (x64) for Paralives and launch the game once to generate the necessary folders. Then place the `ParalivesTraitsProject` folder inside `BepInEx/plugins/`. The folder must contain the `ParalivesTraitsProject.dll` file along with the `Resources` folder holding the `json` and `images` subfolders. Launch the game — the trait panel will appear automatically in character creation.

## Key Features

- Trait selection panel integrated into the character creation screen
- Configurable maximum number of traits per character and per life stage
- Trait definitions loaded from a JSON file — no recompilation needed to add new traits
- Trait icons loaded from image files alongside the JSON
- Trait data saved and restored with each save file
- Public API for other mods to query which traits a character currently has

## For Mod Authors

Other mods can declare a dependency on this mod and use the public API to read character traits at runtime:

```csharp
[BepInDependency("com.xsauroxplayer.paratraits")]

using ParalivesTraitsProject.Managers;

var traits = TraitsManager.GetTraits(character.GUID.ToString());
bool hasTrait = traits.Any(t => t.Definition.id == "your_trait_id");
```

Trait IDs match the `id` field in the `traits.json` file. The API is safe to call every frame — trait lookups are dictionary-based.

## Usage Restrictions

Redistribution, inclusion in mod compilations, and derivative use require explicit permission and proper attribution to the original creator.
