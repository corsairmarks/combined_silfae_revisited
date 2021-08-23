# Overview

Are you a fanatic xenophile when it comes to blue aliens? Do you wish Silfae's "Animated Quarian Portraits" mod was up-to-date?  This mod is for you! Now you can play the Migrant Fleet as designed and use all the gameplay elements for your own empires.

There are lots of other mods which contain the same or similar portraits portraits, so why should you choose this one? Silfae's art style meshes well with Stellaris, or maybe you want to play her version of the Migrant Fleet - content which this mod again makes playable.  Please enjoy my translation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.0.*, the latest version when this was written.  Updates include:

* Fix invalid texture reference in `quarian_female_01_portrait.mesh` (caused lots of error logs)
* Improve Quarian clothing selectors to be influenced by Pop job
* Update the namelist to account for all built-in army types, remove obsolete entries; Army names more lore-friendly
* Update custom starting initializer for 3.0:
    * Original version with a habitable planet
    * New version that works with the Void Dwellers origin
* Add custom trait "Wanderers" that is a higher-powered verion of Nomadic: +30% growth from immigration, -50% resettlement cost, +50% pop automatic resettlement chance
* Replace original "Quarian" trait with "Immunocompromised" that gives +5% engineering research, -5% habitability (0 points) - available for any species
* Update prescripted empire for 3.0
    * Now has oligarchic authority to reflect Quarian government style
    * Now has Origin: Void Dwellers (requires Federations)
    * Species traits altered: Void Dwellers, Wanderers, Intelligent, Immunocompromised, Nonadaptive, Deviants (selected based on the effects of Silfae's original design)
    * Starting leader begins with three traits: Home in the Sky, Space Miner, and Fleet Organizer
    * Can randomly spawn
* You can use the Quarian portraits for your own empire without any DLC requirements

## Compatibility

Compatible with any mod that does not add the same portraits, species class, or art assets.

The Launcher will tell you that some mods are outdated - that is because the dependency is out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mod.

Not compatible with achievements.

### Dependencies

In order for this mod to function, you **must** install the following mod and load it before this one:

[Animated Quarian Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=708669421) by Silfae

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits.

## Known Issues

Silfae's original mod does not include graphics for ecumenopoleis, so they will fall back to the Mmammalian graphical culture. If anyone knows of a mod that provides said stage-6 city picture, I would be happy to investigate getting permission to reuse the graphics, or add it as a dependency to this one.

## Changelog

* 1.0.0 Initial version

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/quarian_portraits_revisited)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.