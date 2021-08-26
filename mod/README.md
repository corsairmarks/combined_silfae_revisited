# Overview

Have you seen the insidious, sleek portraits from Silfae's "Animated Portraits - The Hidden Eye" mod?  Do you long to steer the unwitting masses with up-to-date gameplay elements and play the Global Earth Order as originally designed?  Then this mod is for you!

There are other mods which contain these portraits, so why should you choose this one?  None of the others update the special Grand Illusion gameplay, but this one does!  Please enjoy my translation of Silfae's custom empire into modern Stellaris.

## Important Performance Notes

This mod can have a performance impact on your games, because it iterates all the Pops in empires with the special origin on a monthly basis.  It is off-limits for the AI to randomly pick for this reason.  There is a reason Paradox moved away from this mechanic for Rogue Servitors.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.0.*, the latest version when this was written.  Updates include:

* Remove duplication in room selector, allow it to always be chosen
* Allow portraits to be randomly selected
* **Rebuild special Rogue Servitor-like gameplay for balancing your ruler Pops versus the unwitting slaves**
    * Rebuild special Pop happiness mechanics to have clearer if/else code, reduce usage of `every_owned_pop` for some performance gains
    * Update game events for setting up custom origin, including using `set_update_modifiers_batch` for some performance gains
    * Convert "Parasitic Evolution" into an origin instead of a civic (including graphics for the selection screen and icon)
    * As with the original civic, Origin: Parasitic Evolution is not available for the AI
* Update all custom negative traits to work with Stellaris 3.0
    * Traits use up-to-date-modifiers
    * Most of the `BIOLOGICAL` traits are now available to use on `LITHOID`s too
* Update prescripted empire for 3.0:
    * Now uses the new Origin: Parasitic Evolution (requires Utopia)
    * Now has Civic: Shadow Council to replace the civic which became the origin
    * Can randomly spawn
* You can use Silfae's custom Reptilian portraits (mixed, just Reptilians, or just "Humans") for your own empires without any DLC requirements

# * Fix the broken portrait clothing selector for male rulers
* Update portrait selection for Pops - higher-strata Pops (rulers, complex drones, bio-trophies, and precursors) may use laurel wreaths
* Update clothing selection for Pops - your Pops will wear clothing based on their jobs

## Compatibility

Compatible with any mod that does not add the same portraits, species class, or art assets.

The Launcher will tell you that some mods are outdated - that is because the dependencies are both out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mods.

Not compatible with achievements.

### Dependencies

In order for this mod to function, you **must** install these two mods and load them before this one:

* [Animated Portraits - The Hidden Eye](https://steamcommunity.com/sharedfiles/filedetails/?id=1168459329) by Silfae
* [Silfae's city sets updated](https://steamcommunity.com/sharedfiles/filedetails/?id=2247427791) by Nozeminer

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits or city graphics.

## Known Issues

This mod overwrites the corresponding species class added by "Silfae's city sets updated" so that it will not be available for use.  Instead, the original species class from Silfae (with localisation) is used.  Expect to see one line in error.log like this:

```
[15:41:32][game_singleobjectdatabase.h:147]: Object with key: Silfae-ThirdEye already exists
```

## Changelog

* 1.0.0 Initial version

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/slreptilian_portraits_revisited).

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.

TODO: original start seemed to be 1 rept, 7 human