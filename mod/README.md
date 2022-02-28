# Overview

Do you like space-elves? Perhaps even from a certain grimdark IP? Silfae's "Animated Eldar Portraits" mod fits the bill, but unfortunately the custom empire and starting system are no longer functional due to changes in Stellaris.  With this mod, now you can play as Ulthwé Craftworld using the special Eye of Terror system initializer as Silfae designed it (portraits and starting system available for use with custom empires).

There are lots of other mods which contain these portraits, so why should you choose this one?  None of the others update the custom solar system initializer or address the "Eldar leaders die quickly" issue, but this one does!  Please enjoy my translation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.3 "Libra," the latest version when this was written.  Updates include:

* Enhance clothing selectors to be influenced by Pop job
* Update the namelist to account for all built-in army types, remove obsolete entries
* Add custom trait "Ældari Longevity" to the Eldar species class
    * This trait makes their leaders begin at an older age (previously this effect was from species class itself)
    * Add bonus lifespan to compensate for their older starting age
    * Automatically given to any species designed with the Eldar portraits
* Update pre-scripted empire
    * Now has Origin: Remnants (requires Ancient Relics)
    * Can randomly spawn
    * Gains Psionic Theory for free
    * Ulthwé names and colors are a somewhat more lore-friendly
* Rebuilt challenge-start custom solar system initializer
    * Setup to work correctly for all origins/civics in unmodded Stellaris that do not restrict the starting system initializers (i.e. Origin: Shattered Ring or Origin: Void Dwellers)
    * Rebuild district and building creation and Pop generation
    * Any empire using this initializer gains Hydroponics Farming (`tech_hydroponics`) and Weather Control Systems (`tech_housing_1`) for free
    * Add modified Origin: Remnants starting capital deposits for use with this initializer
    * The Eye of Terror is its own graphics entity with a Stellaris-flavored description and adds the negative effects of _both_ black holes and pulsars
    * Expect Shroud entities to become progressively more successful in their attempts to manifest in the system
* You can use the Eldar portraits and/or custom initializer for your own empire without any DLC requirements
* Fix the file type on the incuded event image - it was a `.png` with the `.dds` extension - it is now distributed in the correct `.dds` format for Stellaris
* Support being able to choose a single-gender species (new in Stellaris 3.2)

## Compatibility

Compatible with any mod that does not add the same portraits, species class, or art assets.

May conflict with other mods that need to alter how relic worlds are upgraded or make changes to Armageddon Bombardment.

The Launcher will tell you that some mods are outdated - that is because the dependency is out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mod.

Built for Stellaris version 3.3 "Libra."  Not compatible with achievements.

### Partial Overrides

This mod also allows the Creatures of the Shroud country to bombard your homeworld if you start in the Eye of Terror system initializer.  And they will use the Armageddon bombardment stance to do so.  To make this work, this mod overrides one game rule (`can_orbital_bombard`) and one bombardment stance (`armageddon`).

### Required Dependency Mods

In order for this mod to function, you **must** install both of the following mods and load them before this one:

* [Animated Eldar Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=707415339) by Silfae
* [Building: Aquaponics Farms](https://steamcommunity.com/sharedfiles/filedetails/?id=2768297949) by me

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits.

## Known Issues

This mod preempts one event from the base game related to restoring relic worlds to ecumenopoleis (`mega.200`) and a bombardment stance (`armageddon`).  Expect to see two lines in error.log like these:

```
[23:27:00][game_singleobjectdatabase.h:147]: Object with key: armageddon already exists, using the one at  file: common/bombardment_stances/01_eldar_revisited_bombardment_stance_overrides.txt line: 1
[23:27:10][eventmanager.cpp:361]: an event with id [mega.201] already exists!  file: events/megacorp_events.txt line: 211
```

## Changelog

* 1.0.0 Initial version
* 1.0.1 More clothing selector improvement, don't allow other species to pick the free Eldar trait
* 1.0.2 Namelist tweaks
* 2.0.0 Update for compatibility with Stellaris version 3.1 "Lem"
    * Add new localisation keys introduced in 3.1
    * Update Eye of Terror planet class with new icon syntax
    * Fix changed field name in custom deposits
    * Update homeworld setup to account for new changes in 3.1 (e.g. Reanimators, Clone Army, Pleasure Seekers, etc.)
    * The creatures of the Shroud want to devour your homeworld if you start with the initializer `eldar_system`
* 2.0.1 Fix Eye of Terror description highlighting
* 3.0.0 Update for compatibility with Stellaris version 3.2 "Herbert"
    * Apply new mono-gender portrait rules
    * More Pop clothing selector refinements
    * Update custom starting system to handle the changes in the base game (mostly for Anglers)
    * Add new tech for special Aquaponics Farms - needed more food for Anglers starting in the Eye of Terror
* 3.0.1 Small adjustments
    * Restrict the Aquaponics tech to Angler empires, unless a mod is detected that allows normal empires to work Angler jobs
    * No longer ignore portrait duplication for the pre-scripted empire
* 4.0.0 Update for compatibility with Stellaris version 3.3 "Libra"
    * Eldar traits use the new properties that replaced `modification`
    * Special Craftworld setup supports unity building changes
    * Special Craftworld setup supports Posthumous Employment
    * Aquaponics is now its own mod and is a dependency for this mod
    * Use a shared set of triggers for job-based clothing
* 4.0.1 Update dependency name

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/eldar_portraits_revisited)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.