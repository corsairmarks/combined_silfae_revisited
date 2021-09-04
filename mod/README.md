# Overview

Have you experienced the sleek, tentacled allure of Silfae's "Animated Octee-lan Portraits" mod?  Do you wish that the gameplay elements were up-to-date so that you can play the Kuri-octa-Xibi and rebel against the Beep-Boops?  Then this mod is for you!

There are other mods which contain the same portraits, so why should you choose this one?  This mod fixes the old code so that the special starting system (containing your former machine overlords) is playable and ensures all the assets are usable by players.  Please enjoy my adaptation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.0.*, the latest version when this was written.  Updates include:

* Remove duplication in room selector
* Remove alternate (blank) city graphics - mostly they were to try and get a static diplomacy backdrop but only worked for colonies with city size 4; set the `graphical_culture` to not define a cityset
* Add a static room that looks identical to the original room plus backdrop image - this room is used by the predefined empire by default
* Original room (with see-through viewport) also remains available for use with custom empires
* Update the namelist to account for all built-in army types, remove obsolete entries
* Fix definitions for Octee-lan custom greeting sound
* Robot species (Beep-Boop) now uses the default robot sounds instead of (non-robotic) mammalian sounds
* Code now sets any leader using the Octee-lan portrait to have `gender = female`
    * Species description and use of a female title for both male/female rulers indicates this is intended
    * All your Octee-lan-portrait leaders will show as Female in the UI and use female pronouns (she/her/hers)
    * Events (hidden) fire on game start, leaders spawning, when elections begin
* Add gestalt version of the Alien Zoo (both a building and technology) which is available to non-genocidal gestalt empires
* Override Isolated Valley (`d_alien_pets_deposit`) to support new zoo building
* Update prescripted empire for 3.0:
    * Octee-lan species: remove Communal to bring trait point total back to up 0 - this is because Charismatic is now 2 points now
    * Now has Origin: Syncretic Evolution (the Quoi-chi are the secondary species; requires Utopia)
    * Can randomly spawn
* Update custom starting initializer (Tsukimi Pool) for 3.0:
    * Now supports a variety of civics and origin starts (all the built-in ones)
    * Muubul species: add Quick Learners because they had an extra point
    * Yuibitt species: add Strong because they had an extra point
    * Xueench species: remove Solitary because this species had a point remaining but couldn't spend it
    * Your former overlords, the Beep Boops, will spawn if the Synthetic Dawn DLC is active
    * Beep-Boop species: removed High Maintenance, add Efficient Processors so that all points are spent
    * Beep-Boop empire: now has custom `country_type` so they can fight you, and you won't automatically gain control of their planet for owning the starbase
    * Beep-Boops will hate you for rejecting them
* You can use the Octee-lan portraits for your own empires without any DLC requirements
* You can use the Beep-Boop portrait (there is only one) for your own machine empires if you have Synthetic Dawn

## Compatibility

In order to add maske the Alien Zoo available to gestalts (needed for the Beep-Boops), it is necessary to override `d_alien_pets_deposit`.  That means this mod is incompatible with other mods that modify that planetary deposit - although I doubt many do.

Compatible with any other mod that does not add the same portraits, species class, or art assets.

The Launcher will tell you that some mods are outdated - that is because the dependency is out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mod.

Not compatible with achievements.

### Dependencies

In order for this mod to function, you **must** install the following mod and load it before this one:

[Animated Octee-lan Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=929140455) by Silfae

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits.

## Known Issues

This mod overrides the deposit `d_alien_pets_deposit` which generates a line in the error log like this:

```
[17:58:08][game_singleobjectdatabase.h:147]: Object with key: d_alien_pets_deposit already exists
```

## Changelog

* 1.0.0 Initial version
* 1.0.1 Tsukimi Pool special bonus species available for any empire using the initializer
* 1.0.2 Random names for Beep-Boops
* 1.0.3 Ensure correct `graphical_culture`

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/octeelan_portraits_revisited)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.