# Overview

Have you seen the insidious, sleek portraits from Silfae's "Holosphere Rising" mod?  Do you long to steer the unwitting masses with up-to-date gameplay elements and play the Holosphere as originally designed?  Then this mod is for you!

There are other mods which contain these portraits, so why should you choose this one?  None of the others update special holofrixit caste-based gameplay, but this one does!  Please enjoy my adaptation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.0.*, the latest version when this was written.  Updates include:

* Enhance Holofrixit portrait usage:
    * Allow portraits to be randomly selected
    * Fix portrait selector and mesh errors (lead to error logs)
    * Set all the main Holofrixit portraits to have a version with and without the Unbidden sparkles
    * Adjust portrait grouping so that all Holofrixit portraits can be selected by the player when creating a custom empire
    * Add Pop-job-based selectors for empires that are not using the custom origin
* Attach special Holofrixit features to an origin, which allows players to opt out of it
* **Rebuild Holofrixit "caste"-based playstyle to work with the Pop job system and new way of assembling robot Pops**
    * Remove old-style "buildable Pops"
    * Reduce amount modifiers attached to the shared Holofrixit trait
    * Adjust special "caste" traits (Hologanglion, Holowarrior/Hologenotype, Holofrixigram/Advanced Holofrixigram/Hyperfrixigram) for up-to-date modifiers
    * Add Holodrone trait for basic drones
    * Add Xechiro trait for highest caste
    * Start with Pops from each of the five castes, but overall fewer than normal empires
    * Holofrixit government is now divided into the Xechiros Protocol government and Hive-network authority, available only with the Holofrixit origin
    * Add random names for the Holofrixit government
* Remove unnecessary old army overrides
* Adjust Holowarrior and Hologenotype armies
* Update Polarizing Nexus energy storage building
* You can use Silfae's Holofrixit portraits for your own empires without any DLC requirements
    * Using the main Holofrixit species class will consume energy instead of food
    * Added a second species class (Holofrixit Alt.) that is a `BIOLOGICAL` archetype, so you can choose to play without the requirement for energy upkeep
* Disable the "Holocrisis" - a duplicate of original AI rebellion - at least until I can spend more time updating it to work with the current game version **postponed until after 3.1 'Lem'**

## Compatibility

This mod is much less compatible than the other Silfae's Revisited series mods.  This is because this mod makes significantly more gameplay changes.  It is explicitly incompatible with [Animated Silicoid Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2579736379) without a compatibility patch.

This mod overwrites most of the Pop jobs definitions to account for the special Holofixit caste traits.  It also overwrites all the Pop strata to implement Holofrixit energy-based Pop upkeep (instead of food).  It's likely to break any time Stellaris makes changes to the underlying Pop strata, such as the anticipated changes for the upcoming 3.1 'Lem' minor release.  These files are completely overwritten:

* `common/pop_categories/00_social_classes.txt`
* `common/pop_categories/01_gestalt_drones.txt`
* `common/pop_categories/02_other_categories.txt`
* `common/pop_jobs/01_ruler_jobs.txt`
* `common/pop_jobs/02_specialist_jobs.txt`
* `common/pop_jobs/03_worker_jobs.txt`
* `common/pop_jobs/04_gestalt_jobs.txt`
* `common/pop_jobs/06_event_jobs.txt`

This mod also lightly alters the requirements for ruler-stratum jobs and some "complex" specialist/complex drone-strata jobs.  Only Xechiros can work the majority of ruler jobs (Ganglions can be Head Researchers), and Drones cannot work any "complex" jobs.  This _also_ means that this mod will need to be explicitly updated any time Paradox makes changes to jobs.

Furthermore, this mod alters some core game rules in `common/game_rules/00_rules.txt` to implement some of the Pop reproduction/assembly requirements and special rules for Holofrixit leaders.  In particular, these rules:

* `can_generate_leader_from_pop`
* `can_generate_military_leader_from_pop`
* `can_species_procreate`
* `can_species_be_assembled`

The Launcher will tell you that some mods are outdated - that is because the dependencies are both out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mods.

Not compatible with achievements.

### Dependencies

In order for this mod to function, you **must** install these three mods and load them before this one:

* [Holosphere Rising](https://steamcommunity.com/sharedfiles/filedetails/?id=868965217) by Silfae
* [Silfae's city sets updated](https://steamcommunity.com/sharedfiles/filedetails/?id=2247427791) by Nozeminer
* [Full Military Service for Battle Thralls](https://steamcommunity.com/sharedfiles/filedetails/?id=2496357447) by me

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits or city graphics.

## Known Issues

This mod overwrites the corresponding species class added by "Silfae's city sets updated" so that it will not be available for use.  Instead, the original species class from Silfae (with localisation) is used.  Also, it replces two triggers from the base game.  Expect to see three lines in error.log like this:

```
[14:11:39][game_singleobjectdatabase.h:147]: Object with key: Silfae-Holofrixit already exists
[14:11:44][game_singleobjectdatabase.h:147]: Object with key: ruler_job_check_trigger already exists
[14:11:44][game_singleobjectdatabase.h:147]: Object with key: complex_specialist_job_check_trigger already exists
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