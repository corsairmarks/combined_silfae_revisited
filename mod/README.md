# Overview

Have you seen the azure, chitinous portraits from Silfae's "Holosphere Rising" mod?  Do you want to manage techno-arthropoid hives with up-to-date gameplay elements and play the Holosphere as originally designed?  Then this mod is for you!

There are other mods which contain these portraits, so why should you choose this one?  None of the others update special holofrixit caste-based gameplay, but this one does!  Please enjoy my adaptation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.3 "Libra," the latest version when this was written.  Updates include:

* Update Holofrixit shipset (reuse of Unbidden) to work with current Stellaris - starbases, titans, juggernauts, and colossi fall back to molluscoid (the fallback for the Unbidden)
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

This mod is much less compatible than the other Silfae's Revisited series mods.  This is because this mod makes significantly more gameplay changes.  It is explicitly incompatible with [Animated Silicoid Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2579736379) unless you use the [compatibility patch](https://steamcommunity.com/sharedfiles/filedetails/?id=2596642632).

The Launcher will tell you that some mods are outdated - that is because the dependencies are both out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mods.

Built for Stellaris version 3.3 "Libra."  Not compatible with achievements.

### File Overwrites

This mod overwrites all of the Pop strata to implement Holofrixit energy-based Pop upkeep (instead of food).  It's likely to break any time Stellaris makes changes to the underlying Pop stratum.  These files are completely overwritten:

* `common/pop_categories/00_social_classes.txt`
* `common/pop_categories/01_gestalt_drones.txt`
* `common/pop_categories/02_other_categories.txt`

### Partial Overrides

This mod also alters the requirements for ruler-stratum jobs and some "complex" specialist/complex drone-stratum jobs.  Only Xechiros can work the majority of ruler jobs (Ganglions can be Head Researchers), and Drones cannot work any "complex" jobs.  Jobs have also been re-weighted so the Holowarriors prefer military jobs and Holofrixigrams avoid mining and favor technician jobs.  These overrides _also_ mean that this mod will need to be explicitly updated any time Paradox makes changes to jobs.

Job overrides:

* Ruler: `head_researcher`, `politician`, `noble`
* Specialist: `researcher`, `priest`, `death_priest`, `enforcer`, `telepath`, `duelist`, `culture_worker`, `bureaucrat`, `manager`, `necromancer`, `death_chronicler`
* Worker: `technician`, `miner`, `soldier`, `scrap_miner`
* Gestalt: `coordinator`, `evaluator`, `synapse_drone`, `brain_drone`, `calculator`, `patrol_drone`, `mining_drone`, `technician_drone`, `warrior_drone`, `chronicle_drone`, `scrap_miner_drone`
* Event-related: `dimensional_portal_researcher`, `dimensional_portal_researcher_gestalt`, `space_time_anomaly_researcher`, `space_time_anomaly_researcher_gestalt`, `cave_cleaner`, `cave_cleaner_gestalt`, `robot_caretaker`, `turtle_miner`, `turtle_miner_gestalt`

Job-related triggers overridden:

* `complex_specialist_job_check_trigger` Holodrones can't do complex work
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

This mod overwrites the corresponding species class added by "Silfae's city sets updated." Instead, the original species class from Silfae (with localisation) is used.  It overwrites a total of 3 triggers, 1 species class, and 38 jobs from the base game; expect to see 42 lines in error.log similar to these:

```
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: head_researcher already exists, using the one at  file: common/pop_jobs/11_holofrixit_revisited_ruler_job_overrides.txt line: 4
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: politician already exists, using the one at  file: common/pop_jobs/11_holofrixit_revisited_ruler_job_overrides.txt line: 176
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: noble already exists, using the one at  file: common/pop_jobs/11_holofrixit_revisited_ruler_job_overrides.txt line: 304
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: researcher already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 4
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: priest already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 150
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: death_priest already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 330
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: enforcer already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 508
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: telepath already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 686
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: duelist already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 853
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: culture_worker already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 1007
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: bureaucrat already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 1149
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: manager already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 1244
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: necromancer already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 1414
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: death_chronicler already exists, using the one at  file: common/pop_jobs/12_holofrixit_revisited_specialist_job_overrides.txt line: 1577
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: technician already exists, using the one at  file: common/pop_jobs/13_holofrixit_revisited_worker_job_overrides.txt line: 5
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: miner already exists, using the one at  file: common/pop_jobs/13_holofrixit_revisited_worker_job_overrides.txt line: 198
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: soldier already exists, using the one at  file: common/pop_jobs/13_holofrixit_revisited_worker_job_overrides.txt line: 350
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: scrap_miner already exists, using the one at  file: common/pop_jobs/13_holofrixit_revisited_worker_job_overrides.txt line: 521
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: coordinator already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 4
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: evaluator already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 67
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: synapse_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 112
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: brain_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 188
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: calculator already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 282
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: patrol_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 368
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: mining_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 460
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: technician_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 526
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: warrior_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 601
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: chronicle_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 720
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: scrap_miner_drone already exists, using the one at  file: common/pop_jobs/14_holofrixit_revisited_gestalt_job_overrides.txt line: 789
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: dimensional_portal_researcher already exists, using the one at  file: common/pop_jobs/16_holofrixit_revisited_event_job_overrides.txt line: 5
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: dimensional_portal_researcher_gestalt already exists, using the one at  file: common/pop_jobs/16_holofrixit_revisited_event_job_overrides.txt line: 195
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: space_time_anomaly_researcher already exists, using the one at  file: common/pop_jobs/16_holofrixit_revisited_event_job_overrides.txt line: 437
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: space_time_anomaly_researcher_gestalt already exists, using the one at  file: common/pop_jobs/16_holofrixit_revisited_event_job_overrides.txt line: 542
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: cave_cleaner already exists, using the one at  file: common/pop_jobs/16_holofrixit_revisited_event_job_overrides.txt line: 639
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: cave_cleaner_gestalt already exists, using the one at  file: common/pop_jobs/16_holofrixit_revisited_event_job_overrides.txt line: 692
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: robot_caretaker already exists, using the one at  file: common/pop_jobs/16_holofrixit_revisited_event_job_overrides.txt line: 744
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: turtle_miner already exists, using the one at  file: common/pop_jobs/16_holofrixit_revisited_event_job_overrides.txt line: 828
[23:26:54][game_singleobjectdatabase.h:147]: Object with key: turtle_miner_gestalt already exists, using the one at  file: common/pop_jobs/16_holofrixit_revisited_event_job_overrides.txt line: 972
[23:27:00][game_singleobjectdatabase.h:147]: Object with key: Silfae-Holofrixit already exists, using the one at  file: common/species_classes/zz_silfae_cities_holofrixit_exclude.txt line: 2
[23:27:08][game_singleobjectdatabase.h:147]: Object with key: complex_specialist_job_check_trigger already exists, using the one at  file: common/scripted_triggers/02_holofrixit_revisited_scripted_triggers_jobs_overrides.txt line: 1
[23:27:08][game_singleobjectdatabase.h:147]: Object with key: is_organic_species already exists, using the one at  file: common/scripted_triggers/02_holofrixit_revisited_scripted_triggers_jobs_overrides.txt line: 19
[23:27:08][game_singleobjectdatabase.h:147]: Object with key: is_robotic_species already exists, using the one at  file: common/scripted_triggers/02_holofrixit_revisited_scripted_triggers_jobs_overrides.txt line: 36
```

## Changelog

* 1.0.0 Initial version
* 1.0.1 Bugfixes
    * Ensure that species are properly upgraded into Advance Holofrixigrams/Hyperfrixigrams/Hologenotypes when the relevant technologies are discovered
    * Fix incorrect scoping for initial leader checks (scientists will be Ganglions)
    * Fix accidental food usage (side-effect of identifying the species as organic)
    * Add namelist for `HLFXT` and `HLFXTALT` (duplicates of `ART1`)
    * Reweight Ganglion and Drone jobs - *frixigrams should always prefer technician jobs and weight lower than Ganglions for science
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
    * Holofrixigams are genderless (role-play wise they are mini-gestalts)
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

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/holosphere_rising_revisited).

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.