# Overview

Have you seen the insidious, sleek portraits from Silfae's "Holosphere Rising" mod?  Do you long to steer the unwitting masses with up-to-date gameplay elements and play the Global Earth Order as originally designed?  Then this mod is for you!

There are other mods which contain these portraits, so why should you choose this one?  None of the others update special holofrixit gameplay or the holofrixigam crisis, but thi one does!  Please enjoy my adaptation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.0.*, the latest version when this was written.  Updates include:

* Enhance Holofrixit portrait usage:
    * Allow portraits to be randomly selected
    * Fix portrait selector and mesh errors (lead to error logs)
    * Set all the main Holofrixit portraits to have a version with and without the Unbidden sparkles
    * Adjust portrait grouping so that all Holofrixit portraits can be selected by the player when creating a custom empire
    * TODO Add Pop-job-based selectors for empires that are not using the custom origin
* Attach special Holofrixit features to an origin, which allows players to opt out of it
* **Rebuild Holofrixit "caste"-based playstyle to work with the Pop job system and new way of assembling robot Pops
    * Remove old-style "buildable Pops"
    * Reduce amount modifiers attached to the shared Holofrixit trait
    * Adjust special "caste" traits (Hologanglion, Holowarrior/Hologenotype, Holofrixigram/Advanced Holofrixigram/Hyperfrixigram) for up-to-date modifiers
    * Add Holodrone trait for basic drones
    * Add Xechiro trait for highest caste (also the only species that can generate leaders)
    * Start with Pops from each of the four Pop-based castes, but overall fewer than normal empires
    * Holofrixit government is now divided into the Xechiros Protocol government and Hive-network authority, available only with the Holofrixit origin
    * Add random names for the Holofrixit government
* Remove unnecessary old army overrides
* Adjust Holowarrior and Hologenotype armies
* Update Polarizing Nexus energy storage building



* Update prescripted empire for 3.0:
    * Can randomly spawn

* Add a namelist for `XXX` (necessary for randomized species to get names)
* You can use Silfae's Holofrixit portraits for your own empires without any DLC requirements

## Compatibility

Compatible with any mod that does not add the same portraits, species class, or art assets.

The Launcher will tell you that some mods are outdated - that is because the dependencies are both out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mods.

Not compatible with achievements.

### Dependencies

In order for this mod to function, you **must** install these two mods and load them before this one:

* [Holosphere Rising](https://steamcommunity.com/sharedfiles/filedetails/?id=868965217) by Silfae
* [Silfae's city sets updated](https://steamcommunity.com/sharedfiles/filedetails/?id=2247427791) by Nozeminer

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits or city graphics.

## Known Issues

This mod overwrites the corresponding species class added by "Silfae's city sets updated" so that it will not be available for use.  Instead, the original species class from Silfae (with localisation) is used.  Expect to see one line in error.log like this:

```
[20:21:43][game_singleobjectdatabase.h:147]: Object with key: Silfae-Holofrixit already exists
```

## Changelog

* 1.0.0 Initial version

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/holosphere_rising_revisited).

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.

# TODO add notes about incompatibility with Silicoids
# Also add note to Silicoids

# TODO consider weak/strong/very strong to help with weighting (intelligent, ingenious, etc)
# or overwrite pop_jobs (blah)

# event on_tech_increased that upgrades them all to the new trait? leave old ones able to be modded (apply template) but special trait(s) can't be removed
# on_tech_increased to upgrade trait levels automagically (and convert all references - yay ezmode)

# when creating initial ganglions, warriors - use the base species but swap the holodrone to hologanglion/holowarrior/holofrixigram
# when editing holofrixigrams, consider them as similar robot/droid/synth

# TODO: could add country modifier during a war with +happiness for warriors, -happniess for ganglions

# TODO: need a holo-drone trait image

# look into the gun locators for the unbidden ships
# C&P for all unbidden ship colors

# TODO: Holofrixit consume energy, probably need to edit pop_categories (no food)

# TODO: Xechiros will only take ruler jobs
# TODO: require corresponding traits for each leader role
# => override 

# Battle Thrall military leaders for ?