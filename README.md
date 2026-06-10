# Traits

A BepInEx mod for Paralives that adds a personality-traits system to the game.

**Creator:** XSauroxPlayer

**Available in [6ix's Plugin Hub](https://github.com/6xvl/paralives-plugins-index).** Install it from inside the game with one click, and it stays up to date on its own.

## What it does

Adds a trait selection panel to character creation. You pick traits for your Parafolk, and they save with your game. Other mods can read a character's traits through a small public API and build gameplay on top of them.

## Install

1. Install BepInEx 5 (x64) for Paralives and run the game once so it creates the BepInEx folders.
2. Put `ParalivesTraitsProject.dll` in `BepInEx/plugins/`.
3. Start the game. The trait section shows up in character profile on its own.

That is the whole install: one file. The traits and all icons are built into the DLL.

## Customizing traits

The first time you run the mod it creates a `BepInEx/plugins/ParalivesTraitsProject/Resources/` folder with `traits.json`, an `images/` folder, and a short README that explains the format. Edit those files to add traits, remove them, or change icons, then restart the game. If you delete a file by accident, the mod falls back to its built-in copy, so nothing breaks. To reset everything, delete the folder and restart.

## Features

- Trait selection panel in the character creation screen
- A cap on traits per character and per life stage
- Traits defined in a JSON file, so you can add your own without rebuilding the mod
- Custom trait icons from image files
- Traits saved and restored with each save file
- Trait data kept in its own file, so it never touches your game saves
- A public API other mods can use to read a character's traits

## For mod authors

Declare a dependency and read a character's traits at runtime:

```csharp
[BepInDependency("com.xsauroxplayer.paratraits")]

using ParalivesTraitsProject.Managers;

var traits = TraitsManager.GetTraits(character.GUID.ToString());
bool hasTrait = traits.Any(t => t.Definition.id == "your_trait_id");
```

Trait IDs match the `id` field in `traits.json`. Lookups are dictionary-based, so the API is cheap to call often.

## License

MIT. See [LICENSE](LICENSE).
