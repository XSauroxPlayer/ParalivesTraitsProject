# Changelog

All notable changes to this project will be documented in this file.

## [1.2.0] - Latest

### Added

#### Commitment Issues Trait Effects
- Parafolk with the **Commitment Issues** trait gain **+1 Uncomfortable** when their romantic partner is in the same zone — proximity triggers the urge to flee.
- Parafolk with the **Commitment Issues** trait suffer **+1 Stressed** whenever they are in a romantic relationship (background anxiety at all times).
- Parafolk with the **Commitment Issues** trait receive a **+15% job bonus when single** (freedom is energizing) and a **−15% penalty when in a relationship** (commitment anxiety cripples focus).

#### Diva Trait Effects
- Every active emotion is amplified for **Diva** Parafolk: **+1 when positive, +1 when negative** — the spotlight magnifies both the highs and the lows.
- **Diva** Parafolk have their **job performance amplified ±20% in both directions** — mood swings hit harder at work.

#### Easy Going Trait Effects
- Parafolk with the **Easy Going** trait gain **+1 Happy** when not at work (thriving in leisure).
- Parafolk with the **Easy Going** trait have **−1 Stressed** while Stressed is active (nothing really gets to them).
- Parafolk with the **Easy Going** trait suffer **+1 Bored** when at work (resent being made to do things).
- Parafolk with the **Easy Going** trait always perform at **×0.80 job efficiency** — they do just enough.

#### Heavy Sleeper Trait Effects
- Parafolk with the **Heavy Sleeper** trait gain **+1 Happy** while sleeping (blissfully deep sleep).
- Parafolk with the **Heavy Sleeper** trait suffer **+1 Stressed** when their Sleep need is critical (cannot function without rest).
- Parafolk with the **Heavy Sleeper** trait have **+1 Bored** during morning hours (06:00–09:00) when not sleeping (groggy and grumpy after waking).
- **Heavy Sleepers** restore **Sleep ×2 faster** while sleeping (deep, efficient sleep).
- **Heavy Sleepers** have their Sleep need decay **×1.3 faster** when awake (they need more sleep than average).

#### Night Owl Trait Effects
- Parafolk with the **Night Owl** trait gain **+1 Inspired** at night (20:00–06:00) — nocturnal creativity peaks after dark.
- Parafolk with the **Night Owl** trait suffer **+1 Bored** in the afternoon (12:00–18:00) — the daytime slump is real.
- **Night Owls** have their Sleep need decay **×0.7 at night** (naturally awake) and **×1.4 during the day** (fighting daylight drowsiness).
- **Night Owls** gain **+25% skill XP** during nighttime hours — nocturnal focus sharpens learning.
- **Night Owls** receive a **×1.3 job performance bonus** when Inspired is their dominant emotion.

#### Rebellious Trait Effects
- Parafolk with the **Rebellious** trait gain **+1 Amused** when not at work (enjoying freedom from authority).
- Parafolk with the **Rebellious** trait suffer **+1 Uncomfortable** when at work (resents the system).
- **Rebellious** Parafolk always perform at **×0.75 job efficiency** (anti-establishment baseline), but receive an **additional ×1.6 multiplier when Angry is dominant** (spite as fuel — net ×1.2).

#### Seldom Sleepy Trait Effects
- Parafolk with the **Seldom Sleepy** trait always have **+1 Inspired**, even from zero — perpetual mental clarity from needing less sleep.
- Parafolk with the **Seldom Sleepy** trait suffer **+1 Bored** while sleeping (finds rest a wasteful chore).
- **Seldom Sleepy** Parafolk have their Sleep need decay at **×0.5** — they barely get tired.
- **Seldom Sleepy** Parafolk receive a **×1.2 job performance bonus** when Inspired is their dominant emotion.

### Added
- Clicking the **Randomize** button in the Personality section of the Paramaker now also randomizes the character's mod traits, respecting the per-life-stage trait limit from the mod config.

### Fixed
- **Diva + Commitment Issues** (and similar trait combos): Diva now correctly amplifies emotions that are raised from zero by another trait. The patch uses the same re-entrancy guard + fast/slow path pattern already in use for Grumpy and Easy Going.

### Changed

#### Cheerful Trait Rework
- Emotion patches now target `GetEmotionValueForUI` (amplifier model visible in the UI breakdown) instead of `GetEmotionValue`.
- Added **×1.15 job performance bonus** when Happy is the dominant emotion (money-driven peak performance from genuine happiness).

#### Gloomy Trait Rework
- Emotion patches now target `GetEmotionValueForUI`.
- Added the **Tortured Artist** effect: Parafolk with the **Gloomy** trait gain **+1 Inspired** whenever they are organically Sad — melancholy channels into creativity.
- Added **×1.3 job performance bonus** when Inspired is the dominant emotion (melancholy fuels creative output).

#### Grumpy Trait Rework
- Emotion patches now target `GetEmotionValueForUI`.
- **Grumpy** Parafolk now always have **+1 Angry**, even from zero — perpetually irritable baseline.
- Added **×1.2 job performance bonus** when Angry is the dominant emotion (bitter determination).

---

## [1.1.8]

### Changed
- Disabled duplicated entry for great kisser trait.
- Fixed various issues with the UI, now building correctly also in the Paramaker

---

## [1.1.7] - Latest

### Changed
- All three UI panels (Traits, Config, Randomize) now have a resize handle in the bottom-right corner — drag it to scale the panel up or down, enlarging icons and text proportionally. The scale is preserved while the game session is active and resets to default on game restart.

### Added

#### Greedy Trait Effects
- Parafolk with the **Greedy** trait gain **+1 Happy** when household money is ≥ 10 000 — wealth brings genuine satisfaction.
- Parafolk with the **Greedy** trait suffer **+1 Stressed** when household money drops below 1 000 — financial panic sets in.
- Parafolk with the **Greedy** trait get a **+25% job bonus** when Happy is their dominant emotion (money-driven peak performance).
- Parafolk with the **Greedy** trait suffer a **+30% amplified job penalty** when Stressed is dominant (financial anxiety cripples focus).

#### Paranoid Trait Effects
- Parafolk with the **Paranoid** trait always have **+1 Stressed**, even from zero — chronic baseline anxiety.
- Parafolk with the **Paranoid** trait gain **+1 Stressed** during night hours (22:00–06:00) — things lurk in the dark.
- Parafolk with the **Paranoid** trait have **−1 Stressed** when completely alone during daytime — their own space is the one safe place (net stress from trait = 0 when alone in daylight).
- Parafolk with the **Paranoid** trait suffer a **+35% amplified job penalty** when Stressed is dominant.

#### Perfectionist Trait Effects
- Parafolk with the **Perfectionist** trait gain **+1 Inspired** whenever they are actively leveling any skill (constant drive for improvement).
- Parafolk with the **Perfectionist** trait suffer **−1 Happy** while leveling a skill below level 5 — early incompetence is genuinely frustrating.
- Parafolk with the **Perfectionist** trait gain **+25% skill XP** when the skill being practiced is already at level ≥ 8 — mastery accelerates mastery.
- Parafolk with the **Perfectionist** trait get a **+20% job bonus** when Inspired is their dominant emotion.

#### Couch Potato Trait Effects
- Parafolk with the **Couch Potato** trait always have **+1 Bored**, even from zero — they're easily bored by default.
- Parafolk with the **Couch Potato** trait gain **+1 Happy** while watching TV or napping (true couch bliss).
- Parafolk with the **Couch Potato** trait have their **Fun need decay 30% slower** — passive entertainment satisfies them completely.
- Parafolk with the **Couch Potato** trait suffer a **+30% amplified job performance penalty** when Bored is their dominant emotion — they genuinely cannot focus.

#### Slob Trait Effects
- Parafolk with the **Slob** trait gain **+1 Amused** when near dirty or messy fixtures (right at home in filth).
- Parafolk with the **Slob** trait have **-1 Uncomfortable** when near dirty fixtures (immune to the discomfort others feel).
- Parafolk with the **Slob** trait suffer **-1 Happy** while doing household chores (genuinely resent being made to clean).

#### Hyperactive Trait Effects
- Parafolk with the **Hyperactive** trait always have **+1 Amused**, even from zero — perpetually buzzing with energy.
- Parafolk with the **Hyperactive** trait gain **+1 Stressed** when their Fun need is at warning level — they can't handle inactivity.
- Parafolk with the **Hyperactive** trait have their **Fun need decay 35% faster** — they burn through entertainment and constantly crave new stimulation.
- Parafolk with the **Hyperactive** trait have their **Sleep need decay 30% slower** — naturally energetic, they need less rest to function.



#### Over-Emotional Trait Effects
- Parafolk with the **Over-Emotional** trait gain **+1 to every active emotion** — all moods are felt more intensely, positive and negative alike.
- Parafolk with the **Over-Emotional** trait have their **job performance amplified by 25% in both directions** — strong moods push harder at work.

#### Coward Trait Effects
- Parafolk with the **Coward** trait always have **+1 Embarrassed** (timid by nature, even from zero).
- Parafolk with the **Coward** trait gain **+2 Stressed** when a visibly angry Parafolk (organic Angry > 0, or Hot-Headed) is in the same zone.
- Parafolk with the **Coward** trait suffer a **50% amplified job performance penalty** when Stressed is their dominant emotion.

#### Dramatic Trait Effects
- Parafolk with the **Dramatic** trait gain **+1 to their dominant emotion**, whatever it currently is — they always double down on their prevailing mood.
- Parafolk with the **Dramatic** trait have their **job performance amplified by 30% in both directions** — mood-driven swings at work are more extreme.

#### Brave Trait Effects
- Parafolk with the **Brave** trait have **-1 Stressed** while Stressed is active (stress does not take hold).
- Parafolk with the **Brave** trait gain **+1 Happy** when a visibly angry or Hot-Headed Parafolk is in the same zone (energized by conflict).
- Parafolk with the **Brave** trait have their **job performance penalty converted to a bonus** when Stressed is their dominant emotion — they thrive under pressure.

#### Mean Spirited Trait Effects
- Parafolk with the **Mean Spirited** trait always have **+1 Angry**, even from zero (hostile baseline).
- Parafolk with the **Mean Spirited** trait gain **+1 Happy** when any nearby Parafolk has a negative dominant emotion (broad schadenfreude).
- Parafolk with the **Mean Spirited** trait have all **mood-based job performance penalties halved** — negativity barely slows them down.

#### Absent-Minded Trait Effects
- Parafolk with the **Absent-Minded** trait have **-1 Inspired** while Inspired is active (thoughts scatter before inspiration can be channelled).
- Parafolk with the **Absent-Minded** trait always have **+1 Amused**, even from zero (mildly entertained by their own wandering mind).
- Parafolk with the **Absent-Minded** trait suffer a **-15% job performance penalty** when Inspired is their dominant emotion — the spark leads to daydreaming, not productivity.

---

## [1.1.6]

### Added

#### Outgoing Trait Effects
- Parafolk with the **Outgoing** trait gain **+1 Happy** while at least one other Parafolk is in the same zone.
- Parafolk with the **Outgoing** trait gain **+1 Stressed** when completely alone.

#### Dastardly Trait Effects
- Parafolk with the **Dastardly** trait always have **+1 Amused** (perpetually mischievous).
- Parafolk with the **Dastardly** trait gain **+1 Happy** when organically angry (thrive on being mean).
- Parafolk with the **Dastardly** trait gain a **+20% job performance bonus** when Angry is their dominant emotion.

#### Clumsy Trait Effects
- Parafolk with the **Clumsy** trait gain **+1 Amused** when Embarrassed is active (laugh at their own failures).
- Parafolk with the **Clumsy** trait have **-1 Embarrassed** while Embarrassed is active (not bothered by failure).
- Parafolk with the **Clumsy** trait suffer a **-15% job performance penalty** when their mood is positive (mishaps even in good times).

---

## [1.1.5]

### Added

#### Hot-Headed Trait Effects
- Parafolk with the **Hot-Headed** trait always have **+2 Angry**, even from zero.
- Parafolk in the same zone as a **Hot-Headed** Parafolk gain **+1 Angry** (rage contagion).
- Parafolk with the **Hot-Headed** trait suffer **double job performance penalty** when Angry is their dominant emotion.

#### Self-Assured Trait Effects
- Parafolk with the **Self-Assured** trait have **-1 Stressed** while Stressed is active.
- Parafolk with the **Self-Assured** trait have **-1 Embarrassed** while Embarrassed is active.
- Parafolk with the **Self-Assured** trait suffer **half the job performance penalty** when their mood is negative.

#### Loyal Trait Effects
- Parafolk with the **Loyal** trait gain **+1 Happy** while their romantic partner is in the same zone.
- Parafolk with the **Loyal** trait in a romantic relationship gain a **+30% job performance bonus** when their mood is positive.

---

## [1.1.4]

### Added

- disabled duplicate entries for enabled traits

#### Ambitious Trait Effects
- Parafolk with the **Ambitious** trait gain **+2 Inspired** while actively at work.
- Parafolk with the **Ambitious** trait suffer **+1 Stressed** when away from work with low job performance (< 50).
- Parafolk with the **Ambitious** trait receive a **50% job performance boost** when Inspired is their dominant emotion at work.


---

## [1.1.3]

### Added

#### Custom Traits Support
- Entries in `custom_traits.json` with the same ID as a built-in trait now take full priority, replacing the base definition.
- Base traits can be disabled from `custom_traits.json` by redeclaring the same ID with `"enabled": false`.

#### Crybaby Trait Effects
- Parafolk with the **Crybaby** trait gain **+2 Sad** while the emotion is active.
- Parafolk with the **Crybaby** trait gain **+1 Sad** when nearby Parafolk have a negative dominant emotion.

#### Easily Bored Trait Effects
- Parafolk with the **Easily Bored** trait gain **+2 Bored** while the emotion is active.
- Parafolk with the **Easily Bored** trait suffer increased **Bored** buildup over time.

#### Hates Computers Trait Effects
- Parafolk with the **Hates Computers** trait gain **+2 Angry** when using computer-related interactions.
- Parafolk with the **Hates Computers** trait gain **+1 Uncomfortable** while near a computer.

#### Hates Reading Trait Effects
- Parafolk with the **Hates Reading** trait gain **+2 Bored** when performing reading interactions.
- Parafolk with the **Hates Reading** trait gain **+1 Uncomfortable** while near books or bookshelves.

---

## [1.1.2]

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
