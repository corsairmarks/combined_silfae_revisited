**_Important Update for Stellaris 3.6 "Orion":_** This mod is now even, even more compatible, thanks to improved trigger usage for Pop upkeep.  This mod no longer overrides any Pop strata.  Thanks Paradox!

# Overview

Have you seen the azure, chitinous portraits from Silfae's "Holosphere Rising" mod?  Do you want to manage techno-arthropoid hives with up-to-date gameplay elements and play the Holosphere as originally designed?  Then this mod is for you!

There are other mods which contain these portraits, so why should you choose this one?  None of the others update special holofrixit caste-based gameplay, but this one does!  Please enjoy my adaptation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.6 "Orion," the latest version when this was written.  Updates include:

* Update Holofrixit shipset (reuse of Unbidden) to work with current Stellaris - starbases, titans, juggernauts, and colossi fall back to molluscoid (the fallback for the Unbidden)
* Enhance Holofrixit portrait usage:
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
    * Only Xechiros may be rulers or Governors, only Ganglions may be Scientists, and Holowarriors or Xechiros may be Admirals and Generals - Holofrixigrams can be leaders with `tech_synthetic_leaders`, Drones can never be leaders, and other non-holofrixit species may produce leaders normally
* Remove unnecessary old army overrides
* Adjust Holowarrior and Hologenotype armies
* Update Polarizing Nexus energy storage building
* Pop portraits influenced by job stratum
* You can use Silfae's Holofrixit portraits for your own empires without any DLC requirements
    * Using the main Holofrixit species class will consume energy instead of food
    * Added a second species class (Holofrixit Alt.) that is a `BIOLOGICAL` archetype, so you can choose to play without the requirement for energy upkeep
* Disable the "Holocrisis" - a duplicate of original AI rebellion - at least until I can spend more time updating it to work with the current game version **postponed indefinitely**
* Support being able to choose a single-gender species (new in Stellaris 3.2)

## Compatibility

The Launcher will tell you that some mods are outdated - that is because the dependencies are both out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mods.

Built for Stellaris version 3.6 "Orion."  Not compatible with achievements.

### Partial Overrides

This mod also alters the requirements for ruler-stratum jobs and some "complicated" specialist/complex drone-stratum jobs.  Only Xechiros can work the majority of ruler jobs (Ganglions can be Head Researchers), and Drones cannot work any jobs that require "thinking" (similar to syncretic proles or zombies).  Jobs have also been re-weighted so the Holowarriors prefer military jobs.  These overrides _also_ mean that this mod will need to be explicitly updated any time Paradox makes changes to the overridden jobs.

Job overrides:

* Ruler: `head_researcher`
* Specialist: `enforcer`
* Worker:`soldier`
* Gestalt: `coordinator`, `evaluator`, `synapse_drone`, `brain_drone`, `calculator`, `patrol_drone`, `warrior_drone`, `chronicle_drone`
* Event-related: `dimensional_portal_researcher_gestalt`, `space_time_anomaly_researcher_gestalt`

Job-related triggers overridden:

* `complex_specialist_job_check_trigger` Holodrones and Holowarriors can't do complicated work but they are smart enough for non-complicated specialist/drone jobs
* `is_organic_species` most Holofrixits qualify as organic
* `is_robotic_species` Holofrixigrams are entirely mechanical

Furthermore, this mod alters some core game rules in `common/game_rules/00_rules.txt` to implement some of the Pop reproduction/assembly requirements and special rules for Holofrixit leaders.  In particular, these rules:

* `can_generate_leader_from_pop`
* `can_generate_military_leader_from_pop`
* `can_species_procreate`
* `can_species_be_assembled`
* `can_fill_ruler_job`

### Dependencies

In order for this mod to function, you **must** install these three mods and load them before this one:

* [Holosphere Rising](https://steamcommunity.com/sharedfiles/filedetails/?id=868965217) by Silfae
* [Silfae's city sets updated](https://steamcommunity.com/sharedfiles/filedetails/?id=2247427791) by Nozeminer
* [Special Leadership Privileges for Battle Thralls and Bio-Trophies](https://steamcommunity.com/sharedfiles/filedetails/?id=2496357447) by me

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits or city graphics.

## Known Issues

This mod overwrites the corresponding species class added by "Silfae's city sets updated."  Instead, the original species class from Silfae (with localisation) is used.  It also overwrites a total of 4 triggers and 13 jobs from the base game; expect to see 18 lines in error.log similar to these:

```
[04:11:29][game_singleobjectdatabase.h:165]: Object with key: Silfae-Holofrixit already exists, using the one at  file: common/species_classes/zz_silfae_cities_holofrixit_exclude.txt line: 2
[04:11:31][game_singleobjectdatabase.h:165]: Object with key: has_energy_upkeep already exists, using the one at  file: common/scripted_triggers/01_holofrixit_revisited_scripted_trigger_overrides.txt line: 1
[04:11:31][game_singleobjectdatabase.h:165]: Object with key: complex_specialist_job_check_trigger already exists, using the one at  file: common/scripted_triggers/02_holofrixit_revisited_scripted_triggers_jobs_overrides.txt line: 1
[04:11:31][game_singleobjectdatabase.h:165]: Object with key: is_organic_species already exists, using the one at  file: common/scripted_triggers/02_holofrixit_revisited_scripted_triggers_jobs_overrides.txt line: 20
[04:11:31][game_singleobjectdatabase.h:165]: Object with key: is_robotic_species already exists, using the one at  file: common/scripted_triggers/02_holofrixit_revisited_scripted_triggers_jobs_overrides.txt line: 38
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: head_researcher already exists, using the one at  file: common/pop_jobs/11_holofrixit_revisited_ruler_job_overrides.txt line: 6
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: enforcer already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 7
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: soldier already exists, using the one at  file: common/pop_jobs/13_holofrixit_revisited_worker_job_overrides.txt line: 6
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: coordinator already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 6
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: evaluator already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 56
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: synapse_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 107
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: brain_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 171
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: calculator already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 213
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: patrol_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 256
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: warrior_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 348
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: chronicle_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 470
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: dimensional_portal_researcher_gestalt already exists, using the one at  file: common/pop_jobs/16_holofrixit_revisited_event_job_overrides.txt line: 6
[04:11:32][game_singleobjectdatabase.h:165]: Object with key: space_time_anomaly_researcher_gestalt already exists, using the one at  file: common/pop_jobs/16_holofrixit_revisited_event_job_overrides.txt line: 237
```

## Changelog

* 1.0.0 Initial version
* 1.0.1 Bugfixes
    * Ensure that species are properly upgraded into Advance Holofrixigrams/Hyperfrixigrams/Hologenotypes when the relevant technologies are discovered
    * Fix incorrect scoping for initial leader checks (scientists will be Ganglions)
    * Fix accidental food usage (side-effect of identifying the species as organic)
    * Add namelist for `HLFXT` and `HLFXTALT` (duplicates of `ART1`)
    * Re-weight Ganglion and Drone jobs - *frixigrams should always prefer technician jobs and weight lower than Ganglions for science
* 1.0.2 More bugfixes
    * Fix incorrect random name reference
    * Allow Xechiros to procreate
    * Ensure correct `graphical_culture`
* 2.0.0 Update for compatibility with Stellaris version 3.1.1 "Lem"
    * Add new localisation keys introduced in 3.1
    * Update Pop strata (categories) with updates from the base game - adding Budding, Phototropic/Radiotropic, etc.
    * Update Pop jobs with updates from from the base game - Catalytic Processing jobs, new event jobs, Scrap Miners, etc.
    * Update with code improvements from the base game
* 2.0.1 Update Pop jobs with deficit changes for Catalytic Tech/Drone in Stellaris 3.1.2
* 2.0.2 Pop Job fixes:
    * Fix slave technician job weight (same as [Enslaved Technician Job Priority Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=2484702578))
    * Fix gestalt gas extractors (from Feral Overload) improperly allowing enslaved species
    * Fix gestalt cave miners (from Feral Overload) improperly allowing enslaved species
* 3.0.0 Update for compatibility with Stellaris version 3.2.2 "Herbert"
    * Apply new mono-gender portrait rules
    * Ganglions are alway male, as their description indicates
    * Holofrixigrams are genderless (role-play wise they are mini-gestalts)
    * More Pop clothing selector refinements
    * Apply base game rule changes (precalc for jobs)
    * Convert from a trigger to a game rule override for the special rule to allow enslaved Ganglions as Head Researchers
    * Apply base game job changes (performance gains!)
    * Apply base game pop strata changes
* 3.0.1 Update `mortal_initiate` and `robot_caretaker` job triggers
* 3.0.2 Update for full compatibility with a dependency (Special Leadership Privileges for Battle Thralls and Bio-Trophies)
* 3.0.3 Update portrait selectors and job rules
    * Portrait selectors based on job category, not pop category - my goal is for the Pop portraits to be based on the job, not the Pop's stratum
    * No longer ignore portrait duplication for the pre-scripted empire
    * Biological Holofrixit alternate species class is not randomized
    * Don't restrict the ability to work the Angler job to Anglers empires (allows other empires to employ Anglers should they somehow get access to the job)
* 4.0.0 Update for compatibility with Stellaris version 3.3 "Libra"
    * Integrate base game script changes
    * Jobs are no longer full-file overwrites!
    * Only the relevant jobs are overridden (which adjust weights based on Holofrixit castes)
    * Significant simplification of `pop_categories`
    * Holofrixit traits use the new properties that replaced `modification`
    * Remove the Hologenotype, Advanced Holofrixigram, and Hyperfrixigram traits - the base traits now dynamically scale their bonuses based on whether you satisfy the prerequisites; as a bonus, they also can detect Machine Empire-related technologies as alternate to the regular techs
    * Add Holowarrior and Hologenotype defensive armies
    * Adjust the Holowarrior trait to grant bonus defensive armies when it upgrades (it is not possible to apply army stat bonuses via a triggered modifier from a trait)
    * Holowarriors no longer want to be Necromancers (the job produces research) but instead attracts Hologanglions
    * Use a shared set of triggers for job-based portraits
* 4.0.1 Remove holowarrior occupation armies - the game does not allow for using alternative occupation armies
* 4.0.2 Updates for 3.3.3/3.3.4 job updates (Death Priest, Death Chronicler, Chronicle Drone)
* 5.0.0 Update for Stellaris version 3.4 "Cepheus"
    * Use memory optimization feature for effects and triggers
    * Remove now-unnecessary job overrides
    * Update remaining job overrides with underlying changes
    * Add `ai_weight` to custom assault armies, add "Resistance is Frugal" bonus unity to custom defensive armies
    * Polarizing Nexus buildings can store even more energy, and double in capacity when Global Production Strategy is researched (the base game updated Resource Silos this way)
    * Pop categories (social strata) updated with underlying trade multiplier changes
    * All static text moved to localisation
* 5.1.0 Further enhancements for Stellaris version 3.4 "Cepheus" - add slave cost adjustments for the custom traits
* 6.0.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax")
    * Minor namelist updates
    * Update `hair` to `attachment`
    * Use the updated file path for the origin icon
    * Update game rule overrides with changes from the base game (affects pop assembly)
    * Update Pop jobs with underlying game changes (only gestalt jobs required updating)
    * Remove Pop category (social strata) overrides - no longer necessary
* 6.0.1 Limit the game to spawning at most one empire with the Hive-Network origin
* 6.0.2 Update empire random names based on changes from Stellaris version 3.6 "Orion"
* 6.0.3 Use the original image from "Overtuned" because it was changed in Stellaris version 3.5 "Fornax" for Toxoids

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/holosphere_rising_revisited).

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.