# Overview

Have you experienced the sleek, tentacled allure of Silfae's "Animated Octee-lan Portraits" mod?  Do you wish that the gameplay elements were up-to-date so that you can play the Kuri-octa-Xibi and rebel against the Beep-Boops?  Then this mod is for you!

There are other mods which contain the same portraits, so why should you choose this one?  This mod fixes the old code so that the special starting system (containing your former machine overlords) is playable and ensures all the assets are usable by players.  Please enjoy my adaptation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.2 "Herbert," the latest version when this was written.  Updates include:

* Remove duplication in room selector
* Remove alternate (blank) city graphics - mostly they were to try and get a static diplomacy backdrop but only worked for colonies with city size 4; set the `graphical_culture` to not define a cityset
* Add a static room that looks identical to the original room plus backdrop image - this room is used by the predefined empire by default
* Original room (with see-through viewport) also remains available for use with custom empires
* Update the namelist to account for all built-in army types, remove obsolete entries
* Fix definitions for Octee-lan custom greeting sound
* Robot species (Beep-Boop) now uses the default robot sounds instead of (non-robotic) mammalian sounds
* Code now sets any leader using the Octee-lan portrait to have `gender = female`
    * This is now implemented through the feature introduced in Stellaris 3.2 to specify a mono-gender species during empire creation
* Add gestalt version of the Alien Zoo (both a building and technology) which is available to non-genocidal gestalt empires
* Override Isolated Valley (`d_alien_pets_deposit`) to support new zoo building
* Update prescripted empire (Kuri-octa-Xibi):
    * Octee-lan species:
        * Remove Communal to bring trait point total back to up 0 - this is because Charismatic is now 2 points now
        * Remove Wasteful and add Unruly in order to add Aquatic (requires the Aquatic Species Pack)
    * Uses Origin: Syncretic Evolution (the Quoi-chi are the secondary species; requires Utopia)
    * Uses Aquatic cities and ships (requires the Aquatic Species Pack)
    * Can randomly spawn
* Update custom starting initializer (Tsukimi Pool):
    * Now supports a variety of civics and origin starts (all the built-in ones)
    * Muubul species: add Aquatic because they had an extra point
    * Yuibitt species: add Aquatic because they had an extra point
    * Xueench species: remove Solitary because this species had a point remaining but couldn't spend it
    * Your former overlords, the Beep Boops, will spawn if the Synthetic Dawn DLC is active
    * Beep-Boop species: removed High Maintenance, add Efficient Processors so that all points are spent
    * Beep-Boop empire: now a regular empire, with a special exception allowing them to have a colony in the same system (in order to fight you)
    * You cannot close your borders to the Beep-Boops, nor can they close theirs to you
    * Beep-Boops will hate you for rejecting them
* You can use the Octee-lan portraits for your own empires without any DLC requirements
* You can use the Beep-Boop portrait (there is only one) for your own machine empires if you have Synthetic Dawn

## Compatibility

In order to make the Alien Zoo available to gestalts (needed for the Beep-Boops), it is necessary to override `d_alien_pets_deposit`.  That means this mod is incompatible with other mods that modify that planetary deposit - although I doubt many do.

New for Stellaris 3.2, this mod now overrides two diplomatic actions (Close Borders and Declare Rivalry) in order to prevent players beginning in Tsukimi Pool from closing their borders to the Beep-Boop (which would otherwise their fleets stuck permanently MIA).  Thus this mod is now not compatible with others that make changes to the same diplomatic actions (does not conflict with mods that add extra diplomatic message text).  Otherwise compatible with any other mod that does not add the same portraits, species class, or art assets.

The Launcher will tell you that some mods are outdated - that is because the dependency is out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mod.

Built for Stellaris version 3.2.* "Herbert."  Not compatible with achievements.

### Event Preemption

In order to allow the Beep-Boops to have a planet in the same system as the player, this mod replaces the event `action.85` that is responsible for (on a monthly basis) transferring control of any colonies not owned by the system's starbase's owner to the starbase owner. The Beep-Boops have a special exception, otherwise this event continues to function as normal.

### Dependencies

In order for this mod to function, you **must** install the following mod and load it before this one:

[Animated Octee-lan Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=929140455) by Silfae

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits.

## Known Issues

This mod preempts one event and overrides a deposit and two diplomatic actions, which generates four lines in the error log like this:

```
[02:34:24][game_singleobjectdatabase.h:147]: Object with key: action_make_rival already exists
[02:34:24][game_singleobjectdatabase.h:147]: Object with key: action_close_borders already exists
[02:34:24][eventmanager.cpp:355]: an event with id [action.85] already exists!  file: events/on_action_events.txt line: 8811
[02:34:24][game_singleobjectdatabase.h:147]: Object with key: d_alien_pets_deposit already exists
```

## Changelog

* 1.0.0 Initial version
* 1.0.1 Tsukimi Pool special bonus species available for any empire using the initializer
* 1.0.2 Random names for Beep-Boops
* 1.0.3 Ensure correct `graphical_culture`
* 1.1.0 Adjust Beep-Boops to work like regular empire
    * Start with a special starbase that orbits their homeworld but is functionally equivalent to a regular starbase (plus three defense platforms)
    * Can build ships with their starbase - they don't like you, so be very wary of their naval buildup
    * Initializer description calls out that it is challenging
* 1.1.1 Fix critical bug so all outposts are not `starbase_faux_outpost`
* 2.0.0 Update for compatibility with Stellaris version 3.1 "Lem"
    * Add new localisation keys introduced in 3.1
    * Set Octee-lans as female-only using new features (start a new game or run `event octeelan_evt.3` to update an existing game)
    * Integrate base game changes (field name changes, icons)
* 3.0.0 Update for compatibility with Stellaris version 3.2 "Herbert"
    * Use new "mono-gender" species choice to set the prescripted empire to `gender = female`
    * Remove event to force the Octee-lan portraits to be female (the game can do this now)
    * Octee-lans, Muubul, and Yuibitts are now Aquatic
    * Improve spawn code for bonus Tsukimi Pool system species
* 3.1.0 Implement special mechanic so you and the Beep-Boops can **fight** (total war) and no closing of borders
    * New Containment _casus belli_ that can be used by only the Beep-Boops and the player empire that started in their system
    * Wargoals for each side of the special Containment
    * Diplomacy action block you from closing borders or declaring a rivalry with the Beep-Boops and vice versa

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/octeelan_portraits_revisited)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.