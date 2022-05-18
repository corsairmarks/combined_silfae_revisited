# Overview

Have you seen the insidious, sleek portraits from Silfae's "Animated Portraits - The Hidden Eye" mod?  Do you long to steer the unwitting masses with up-to-date gameplay elements and play the Global Earth Order as originally designed?  Then this mod is for you!

There are other mods which contain these portraits, so why should you choose this one?  None of the others update the special Grand Illusion gameplay, but this one does!  Please enjoy my translation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.4 "Cepheus," the latest version when this was written.  Updates include:

* Renamed species class to "Sleek Reptilian" so there isn't confusion with the built-in Reptilian species class
* Remove duplication in room selector, allow it to always be chosen
* Allow portraits to be randomly selected
* Add a namelist for `SLRPTLN` (necessary for randomized species to get names)
* Fix mesh definitions to use the correctly-named animations (`slreptilian` uses `reptilian_04`)
* Fix portrait selectors so male/female reptilians aren't considered different phenotypes
* Update clothing selection for Pops - your Pops will wear clothing based on their jobs
* Update hair selection for Pops - reduce duplication
* **Rebuild special Rogue Servitor-like gameplay for balancing your ruler Pops versus the unwitting slaves**
    * Rebuild special Pop happiness mechanics to have clearer if/else code, use the country modifier for all bonuses (as opposed to iterating all the Pops)
    * Update game events for setting up custom origin, including using `set_update_modifiers_batch` for some performance gains
    * Convert "Parasitic Evolution" into an origin instead of a civic (including graphics for the selection screen and icon)
    * As with the original civic, Origin: Parasitic Evolution is not available for the AI
* Update all custom negative traits to work with modern Stellaris
    * Traits use up-to-date-modifiers
    * Most of the `BIOLOGICAL` traits are now available to use on `LITHOID`s too
    * These traits were originally designed as advanced traits, which means you must have Evolutionary Mastery to use them
* Update pre-scripted empire
    * Now uses the new Origin: Parasitic Evolution (requires Utopia)
    * Now has Civic: Shadow Council to replace the civic which became the origin
    * Can randomly spawn
* You can use Silfae's custom Sleek Reptilian portraits (mixed, just Reptilians, or just "Humans") for your own empires without any DLC requirements
* Support being able to choose a single-gender species (new in Stellaris 3.2)

## Compatibility

Compatible with any mod that does not add the same portraits, species class, or art assets.

The Launcher will tell you that some mods are outdated - that is because the dependencies are both out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mods.

Built for Stellaris version 3.4 "Cepheus."  Not compatible with achievements.

### Dependencies

In order for this mod to function, you **must** install these two mods and load them before this one:

* [Animated Portraits - The Hidden Eye](https://steamcommunity.com/sharedfiles/filedetails/?id=1168459329) by Silfae
* [Silfae's city sets updated](https://steamcommunity.com/sharedfiles/filedetails/?id=2247427791) by Nozeminer

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits or city graphics.

## Known Issues

This mod overwrites the corresponding species class added by "Silfae's city sets updated" so that it will not be available for use.  Instead, the original species class from Silfae (with localisation) is used.  Expect to see one line in error.log like this:

```
[23:27:00][game_singleobjectdatabase.h:147]: Object with key: Silfae-ThirdEye already exists, using the one at  file: common/species_classes/zz_silfae_cities_slreptilian_exclude.txt line: 2
```

## Changelog

* 1.0.0 Initial version
* 1.1.0 Add missing fleet names, add government random names, fix missing localisation
* 1.2.0 Update for compatibility with Stellaris version 3.1 "Lem"
    * Add new localisation keys introduced in 3.1
* 2.0.0 Update for compatibility with Stellaris version 3.2 "Herbert"
    * Apply new mono-gender portrait rules
    * More Pop clothing selector refinements
    * New "Mineral Deficient" negative trait for lithoids
* 2.0.1 Fix improper species-level portrait selector syntax for non-male "human" portraits
* 2.0.2 Don't break the base game diplomacy rooms - fix is to name the new file to load _before_ the built-in file
* 2.0.3 Minor tweaks
    * Portrait selectors based on job category, not pop category - my goal is for the Pop portraits to be based on the job, not the Pop's stratum
    * No longer ignore portrait duplication for the pre-scripted empire
    * Don't randomize the all-Reptilian or all-"Human" portrait groups
* 2.0.4 Allow players to pick the all-Reptilian or all-"Human" portrait groups - it is intended only that the AI cannot randomly choose those two groups
* 3.0.0 Update for compatibility with Stellaris version 3.3 "Libra"
    * Integrate base game script changes
    * Use a shared set of triggers for job-based clothing
* 4.0.0 Update for Stellaris version 3.4 "Cepheus"
    * Add a useful description to Civic: Geneticists
    * Update shared triggers
    * Minor localisation enhancements (spelling, grammar, use dynamic loc commands)
    * All static text moved to localisation (random empire names, name lists, species names, prescripted empire)

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/slreptilian_portraits_revisited).

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.