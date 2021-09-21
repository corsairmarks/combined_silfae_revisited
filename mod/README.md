# Overview

Have you seen the fantastic, animated portraits from Silfae's "Animated Hyena Portraits" mod?  Do you wish that the gameplay elements were up-to-date so that you can play the Viverran Rising Throne as originally designed?  Then this mod is for you!

There are lots of other mods which contain these portraits, so why should you choose this one?  None of the others update the custom solar system initializer, but this one does!  Please enjoy my translation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.0.*, the latest version when this was written.  Updates include:

* Fix the broken portrait clothing selector for male rulers
* Update the namelist to account for all built-in army types, remove obsolete entries
* Update the custom starting system initializer for 3.0
* Custom starting initializer now supports a variety of civics and origin starts (all the built-in ones)
* Add an extra species trait (Communal) to the prescripted empire, because Repugnant is now -2 points
* Update portrait and clothing selection for Pops - your Pops will wear clothing based on their jobs

## Compatibility

Compatible with any mod that does not add the same portraits, species class, or art assets.

The Launcher will tell you that some mods are outdated - that is because the dependencies are both out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mods.

Built for Stellaris version 3.1.* "Lem."  Not compatible with achievements.

### Dependencies

In order for this mod to function, you **must** install these two mods and load them before this one:

* [Animated Hyena Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=1126014321) by Silfae
* [Silfae's city sets updated](https://steamcommunity.com/sharedfiles/filedetails/?id=2247427791) by Nozeminer

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits or city graphics.

## Known Issues

This mod overwrites the corresponding species class added by "Silfae's city sets updated" so that it will not be available for use.  Instead, the original species class from Silfae (with localisation) is used.  Expect to see one line in error.log like this:

```
[05:11:30][game_singleobjectdatabase.h:147]: Object with key: Silfae-Hyena already exists
```

## Changelog

* 1.0.0 Initial version
* 1.0.1 Fix Machine World origin to have correct districts
* 1.0.2 Adjust system initializer description
* 1.0.3 Fix a different clothing selector that I broke, allow portrait randomization
* 1.0.4 Ensure correct `graphical_culture`
* 1.1.0 Mark as compatible with Stellaris version 3.1.* "Lem"
    * Add new localisation keys introduced in 3.1

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/hyenafolk_portraits_revisited).

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.