# Overview

Are you a creature of the void?  Does your never-ending hunger compel you to seek out an update of Silfae's "Animated Hollow Portraits" mod?  Do the eldritch powers demand up-to-date gameplay elements so that you can play the Hollow Rift as originally designed?  Then this mod is for you!

There are other mods which contain these portraits, so why should you choose this one?  None of the others update the custom solar system initializer, AI personality, modified Prethoryn-based shipset, custom ship type, or custom species trait, but this one does!  Please enjoy my translation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.0.*, the latest version when this was written.  Updates include:

* Fix the included Prethoryn-swap shipset `horrorworm_01`
    * Ensure the ship entities are blank for ship sections and instead use the ship hull as the attachment point for the modified Prethoryn graphics
    * Add missing entities and weapon locators
    * Remove duplication
    * Fallback for titans, juggernauts, and colossi is molluscoid
* Fix the included custom ship type (Dimensional Horrorworm with an XL slot) - note that Leviathans is required for the ship model
    * Fix the ship class, section, and default design to work in 3.0
    * Fix portrait selectors to offer fewer phenotypes with the correct multiple color options - the graphics have been there the whole time, just needed some tweaking for presentation
    * Add components for the Dimensional Horrorworm ship type (reactors, computers, and thrusters) of all types included in regular Stellaris
* Adjust Eltryrad portraits based on Pop type - lore-wise they have a caste system
* Add a custom deposit for the Hollow starting world ancient ruins - the previous deposit type was removed from the base game
* Update the namelist to account for all built-in army types, remove obsolete entries
* Update the custom starting system initializer for 3.0
    * Starting planet intentionally tiny and filled with ancient ruins blockers
    * Can have guaranteed habitable worlds nearby (based on game settings)
    * Less complex that some of Silfae's other starting systems, so it already works with newer civics and origins
* Update the AI personality to account for new game features
* Update the custom empire the Hollow Rift
    * Now uses Origin: Survivor (requires DLC: Apocalypse) to represent the Hollow's explosive arrival in this dimension
    * Update the custom trait Astral Horror to use modifiers available in Stellaris 3.0
    * Add Repugnant trait to the Hollow - the effects of the old Repugnant trait were built-in to Astral Horror, but the new effects require the Repugnant trait to be active
* You can use the Hollow portraits and/or custom initializer for your own empire without any DLC requirements

## Compatibility

Compatible with any mod that does not add the same portraits, species class, ship, ship components, or art assets.

The Launcher will tell you that some mods are outdated - that is because the dependencies are both out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mods.

Not compatible with achievements.  The shipset does not have NSC classes.

### Dependencies

In order for this mod to function, you **must** install these two mods and load them before this one:

* [Animated Hollow Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=902526212) by Silfae
* [Silfae's city sets updated](https://steamcommunity.com/sharedfiles/filedetails/?id=2247427791) by Nozeminer

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits or city graphics.

## Known Issues

The solar system initializer for Hollow Rift fills the planet with ancient ruins and adds enough Pops to work all open jobs.  The logic does not work if there are open jobs that the main species cannot fill.  In base Stellaris, this only applies to Rogue Servitors and this mod handles that case.  However, other mods that can lead to this situation may break the bonus Pop mechanic.

### Error Logs

This mod overwrites the corresponding species class added by "Silfae's city sets updated" so that it will not be available for use.  Instead, the original species class from Silfae (with localisation) is used.  Expect to see one line in error.log like this:

```
[18:56:44][game_singleobjectdatabase.h:147]: Object with key: Silfae-Horror already exists
```

### Stellaris Bugs

When selecting the Eltryrad portraits and later editing a species using the "Main Hive" portrait as the Ruler, (the large one, phenotype 13) the game will appear to prevent you from accessing the other colors of the other phenotypes.  Change to a different phenotype, move to another empire creation tab, and then come back to the Ruler tab.  The color selection arrows will again be active.

This appears to be a bug with Stellaris where the various portrait selector arrows do not dynamically update while you are at the screen and a species offers phenotypes with differing amounts of colors (e.g. phenotype A has 3 colors but phenotype B has 5 colors).  This is most noticeable when a species has a phenotype with only one color - the arrows are disabled until leaving the tab and coming back.

### Graphics Issues

The graphics file `horrorworm_warrior_d_body_03.dds` is the wrong color - it does not match the fourth color for the other "Warrior," "Worker," or "Wise" types that each have four corresponding colors.  This appears to have been an issue when the original files were created - `horrorworm_warrior_d_body_03` is a duplicate of `horrorworm_warrior_c_body_03` rather than having its own color.

In game terms, the fourth color of Phenotype 9 is the same as the third color.

## Changelog

* 1.0.0 Initial version
* 1.0.1 Require Apocalypse for prescripted empire, extra names for randomisation, allow portraits as secondary species and to be randomized

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/horrorworm_portraits_revisited).

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae and Oskar Potocki for creating and sharing these great animated portraits with the community.