# Overview

Have you seen the razor-sharp good looks of Silfae's "Animated Raptor Portraits" mod?  Do you wish that the gameplay elements were up-to-date so that you can play the Glorious Crescent as originally designed?  Then this mod is for you!

There are lots of other mods which contain these portraits, so why should you choose this one?  None of the others update the custom solar system initializer, special primitives, and guaranteed neighbor systems, but this one does!  Please enjoy my translation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.7 "Canis Minor," the latest version when this was written.  Updates include:

* Enhance portrait selectors to specialize some Pops with appropriate clothing (because the clothing is built in to each portrait file, I can't change to clothing selectors instead of phenotypes)
* Update the namelist to account for all built-in army types, remove obsolete entries
* Update the custom starting system initializer, including the primitive civilization and its extra armies to make conquering them more difficult
* All seven custom neighboring systems updated, and eliminated chance for one of them to double-spawn
* Custom starting initializer now supports a variety of civics and origin starts (all the built-in ones)
* Update the AI personality to account for new game features
* Support being able to choose a single-gender species (new in Stellaris 3.2)

## Compatibility

Compatible with any mod that does not add the same portraits, species class, or art assets.

The Launcher will tell you that some mods are outdated - that is because the dependencies are both out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mods.

Built for Stellaris version 3.7 "Canis Minor."  Not compatible with achievements.

### Dependencies

In order for this mod to function, you **must** install these two mods and load them before this one:

* [Animated Raptor Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=872596925) by Silfae
* [Silfae's city sets updated](https://steamcommunity.com/sharedfiles/filedetails/?id=2247427791) by Nozeminer

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits or city graphics.

## Known Issues

This mod overwrites the corresponding species class added by "Silfae's city sets updated" so that it will not be available for use.  Instead, the original species class from Silfae (with localisation) is used.  Expect to see one line in error.log like this:

```
[23:27:00][game_singleobjectdatabase.h:165]: Object with key: Silfae-Saur already exists, using the one at  file: common/species_classes/zz_silfae_cities_saurischian_exclude.txt line: 2
```

## Changelog

* 1.0.0 Initial version
* 1.0.1 Allow portrait randomization, slight tweaks to portrait selectors
* 1.0.2 Ensure correct `graphical_culture`
* 1.1.0 Mark as compatible with Stellaris version 3.1 "Lem"
    * Add new localisation keys introduced in 3.1
    * Volatile motes had to be moved to different planets to avoid mining stations improperly collecting them at game start (reported by Kaiser Nikolaus I)
* 2.0.0 Update for compatibility with Stellaris version 3.2 "Herbert"
    * Apply new mono-gender portrait rules
    * More portrait selector refinements (these portraits don't have a separate clothing layer - it is built-in the the portrait)
* 2.0.1 Use kelp blockers for ocean planets in the custom system initializer
* 2.0.2 Portrait selectors based on job category, not pop category - my goal is for the Pop portraits to be based on the job, not the Pop's stratum
* 2.0.3 No longer ignore portrait duplication for the pre-scripted empire
* 3.0.0 Update for compatibility with Stellaris version 3.3 "Libra"
    * Integrate base game script changes
    * Use a shared set of triggers for job-based portraits
    * Add pre-sapient saurischian species class
* 4.0.0 Update for Stellaris version 3.4 "Cepheus"
    * Update shared triggers
    * All static text moved to localisation (name lists, species random names, prescripted empire, custom starting system)
* 4.0.1 Fix incorrect localisation key for sequentially-named fleets in the Saurischian name list
* 5.0.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax")
    * Minor namelist updates
    * Update `hair` to `attachment`
* 6.0.0 Update for Stellaris version 3.7 "Canis Minor"
    * Update Pretentious Conquerors personality with new features
    * Update shared triggers for Pop portraits
    * Update custom starting system with underlying changes to pre-FTL civilizations
    * Remove global flag
    * Add compatibility trigger `has_saurischian_portraits_revisited_active`
* 6.0.1 Fix pre-FTL setup event for the Twin Quarks system

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/saurischian_portraits_revisited).

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.