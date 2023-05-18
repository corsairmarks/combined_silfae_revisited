# Overview

Have you experienced the sleek, tentacled allure of Silfae's "Animated Octee-lan Portraits" mod?  Do you wish that the gameplay elements were up-to-date so that you can play the Kuri-octa-Xibi and rebel against the Beep-Boops?  Then this mod is for you!

There are other mods which contain the same portraits, so why should you choose this one?  This mod fixes the old code so that the special starting system (containing your former machine overlords) is playable and ensures all the assets are usable by players.  Please enjoy my adaptation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.8 "Gemini," the latest version when this was written.  Updates include:

* Remove duplication in room selector
* Remove alternate (blank) city graphics - mostly they were to try and get a static diplomacy backdrop but only worked for colonies with city size 4; set the `graphical_culture` to not define a cityset
* Add a static room that looks identical to the original room plus backdrop image - this room is used by the predefined empire by default
* Original room (with see-through viewport) also remains available for use with custom empires
* Update the namelist to account for all built-in army types, remove obsolete entries
* Fix definitions for Octee-lan custom greeting sound
* Machine species (Beep-Boop) now uses the default robot sounds instead of (non-robotic) mammalian sounds
* Add gestalt version of the Alien Zoo (building, technology, and job) which is available to non-genocidal gestalt empires
* Update pre-scripted empire (Kuri-octa-Xibi):
    * Octee-lan species:
    * Female mono-gender species (since Stellaris 3.2)
        * Swap Rapid Breeders to Aquatic (requires the Aquatic Species Pack) to fit the role-play better
        * Remove Communal because Charismatic is now 2 trait points now
    * Uses Origin: Syncretic Evolution (the Quoi-chi are the secondary species; requires Utopia)
    * Uses Aquatic cities and ships (requires the Aquatic Species Pack)
    * Can randomly spawn
* Update custom starting initializer (Tsukimi Pool):
    * Now supports a variety of civics and origin starts (all the built-in ones)
    * Muubul species: add Natural Engineers because they had an extra trait point
    * Yuibitt species: add Aquatic and Slow Learners to use all available trait points
    * Xueench species: add Quick Learners because they had an extra trait point
    * Your former overlords, the Beep Boops, will spawn if the Synthetic Dawn DLC is active
    * Beep-Boop species: removed High Maintenance, add Efficient Processors so that all points are spent
    * Beep-Boop empire: now a regular empire, with a special exception allowing them to have a colony in the same system (in order to fight you)
    * The Beep-Boops begin with a starbase above their planet, or an orbital ring if the Overlord DLC is active
    * You cannot close your borders to the Beep-Boops, nor can they close theirs to you
    * Beep-Boops will hate you for rejecting them
* The Octee-lan are part of the Aquatic species class (with the Aquatics Species Pack) or Molluscoid species class (without) (since Stellaris 3.8)
* The Beep-Boop portrait (there is only one) is part of the Machine and Robot species classes, meaning you can use it for your own amchine empire or as alternate robot portraits (since Stellaris 3.8)
* You can use the Octee-lan portraits for your own empires without any DLC requirements as well as the robotic Beep-Boops (the machine version requires Synthetic Dawn)

## Compatibility

This mod overrides two diplomatic actions (Close Borders and Declare Rivalry) in order to prevent players beginning in Tsukimi Pool from closing their borders to the Beep-Boops (which would otherwise cause their fleets to be stuck permanently MIA).  That means this mod is not compatible with others that make changes to the same diplomatic actions (but does not conflict with mods that add extra diplomatic message text).  Otherwise compatible with any other mod that does not add the same portraits, species class, or art assets.

The Launcher will tell you that some mods are outdated - that is because the dependency is out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mod.

Built for Stellaris version 3.8 "Gemini."  Not compatible with achievements.

### Event Preemption

In order to allow the Beep-Boops to have a planet in the same system as the player, this mod replaces the event `action.85` that is responsible for (on a monthly basis) transferring control of any colonies not owned by the system's starbase's owner to the starbase owner. The Beep-Boops have a special exception, otherwise this event continues to function as normal.

### Dependencies

In order for this mod to function, you **must** install the following mod and load it before this one:

[Animated Octee-lan Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=929140455) by Silfae

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits.

## Known Issues

This mod preempts one event and overrides two diplomatic actions, which generates three lines in the error log like this:

```
[00:23:32][game_singleobjectdatabase.h:153]: Object with key: action_make_rival already exists, using the one at  file: common/diplomatic_actions/10_octeelan_revisited_diplomatic_action_overrides.txt line: 2
[00:23:32][game_singleobjectdatabase.h:153]: Object with key: action_close_borders already exists, using the one at  file: common/diplomatic_actions/10_octeelan_revisited_diplomatic_action_overrides.txt line: 117
[00:23:36][eventmanager.cpp:369]: an event with id [action.85] already exists!  file: events/on_action_events_1.txt line: 6590
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
    * Use new "mono-gender" species choice to set the pre-scripted empire to `gender = female`
    * Remove event to force the Octee-lan portraits to be female (the game can do this now)
    * Octee-lans, Muubul, and Yuibitts are now Aquatic
    * Improve spawn code for bonus Tsukimi Pool system species
* 3.1.0 Implement special mechanic so you and the Beep-Boops can **fight** (total war) and no closing of borders
    * New Containment _casus belli_ that can be used by only the Beep-Boops and the player empire that started in their system
    * Wargoals for each side of the special Containment
    * Diplomacy action block you from closing borders or declaring a rivalry with the Beep-Boops and vice versa
* 3.1.1 Don't break the base game diplomacy rooms - fix is to name the new file to load _before_ the built-in file
* 3.1.2 No longer ignore portrait duplication for the pre-scripted empire
* 4.0.0 Update for compatibility with Stellaris version 3.3 "Libra"
* 5.0.0 Update for Stellaris version 3.4 "Cepheus"
    * Use memory optimization feature for effects and a trigger
    * Move deprecated `localisation_synced` into regular localisation
    * Update Beep-Boop special extra defensive army
    * Remove starbase code duplication - the Beep-Boops can just have a regular starbase now
    * All static text moved to localisation (name lists, species random names, prescripted empire, custom starting system)
    * Update overridden diplomatic actions to account for new Overlord systems
* 6.0.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax")
    * Minor namelist updates
    * Update `hair` to `attachment`
    * You are more likely to draw the gestalt Xenology technology if you have the Javorian Pox Sample (same as the original version)
    * Rebalance special starting system bonus species
* 7.0.0 Update for Stellaris version 3.7 "Canis Minor"
    * Update Interstellar Pursuers personality with new features
    * Remove no-longer-necessary override of the Isolated Valley deposit
    * Update Xeno Zoo (gestalt) building based on changes to the base Xeno Zoo
    * Add new jobs for the Xeno Zoo (gestalt) based on the new Zookeeper and Protected Fauna/Conserved Fauna jobs
    * Remove global flag
    * Add compatibility trigger `has_octeelan_portraits_revisited_active`
* 8.0.0 Update for Stellaris version 3.8 "Gemini"
    * Octee-lan are now part of the Aquatic (with Aquatic Species Pack) or Molluscoid (without) species class (thanks to changes by Paradox, this is no longer mod-unfriendly)
    * Beep-Boops are now part of the machine and robot species classes
    * Beep-Boops begin with an orbital ring (T1) instead of a starbase when the Overlord DLC is active
    * Update prescripted empire to use the new prescripted ruler class and trait system
    * Update shared triggers

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/octeelan_portraits_revisited)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.