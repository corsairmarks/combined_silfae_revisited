# Overview

This mod is a compilation of my adaptations of Silfae's portrait mods.  Please see the description of each individual mod for what the effects are.

Individual mods update first, then changes are merged here.

# Bundled Mods

This is a bundle of mods to make it a little easier to sub and ensure cross-compatibility with each-other.  Please check each individual mod for the effects and any known issues.  The numbers indicate which version of a particular mod is contained in this mod (which also corresponds to the version tag in its `git` repository).

* [Animated Aquilese Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2576769521) ([Source](https://github.com/corsairmarks/romaneagles_portraits_revisited) 6.0.0)
* [Animated Asari Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2581752619) ([Source](https://github.com/corsairmarks/asari_portraits_revisited) 7.0.0)
* [Animated Eldar Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2581388205) ([Source](https://github.com/corsairmarks/eldar_portraits_revisited) 6.0.1)
* [Animated Hidden Eye Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2585946800) ([Source](https://github.com/corsairmarks/slreptilian_portraits_revisited) 6.0.0)
* [Animated Hollow Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2578037235) ([Source](https://github.com/corsairmarks/horrorworm_portraits_revisited) 6.0.1)
* [Animated Holosphere Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2592592503) ([Source](https://github.com/corsairmarks/holosphere_rising_revisited) 6.0.3)
* [Animated Hyena Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2576290763) ([Source](https://github.com/corsairmarks/hyenafolk_portraits_revisited) 6.0.0)
* [Animated Octee-lan Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2584680339) ([Source](https://github.com/corsairmarks/octeelan_portraits_revisited) 6.0.0)
* [Animated Quarian Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2583358569) ([Source](https://github.com/corsairmarks/quarian_portraits_revisited) 7.0.1)
* [Animated Raptor Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2577216891) ([Source](https://github.com/corsairmarks/saurischian_portraits_revisited) 5.0.0)
* [Animated Serpentoid Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2577093634) ([Source](https://github.com/corsairmarks/serpentoid_portraits_revisited) 6.0.0)
* [Animated Shark Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2585030748) ([Source](https://github.com/corsairmarks/sharkanian_portraits_revisited) 5.0.0)
* [Animated Silicoid Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2579736379) ([Source](https://github.com/corsairmarks/silicoid_portraits_revisited) 7.0.0)
* [Animated Xirmian Portraits: Revisited](https://steamcommunity.com/workshop/filedetails/?id=2577789863) ([Source](https://github.com/corsairmarks/xirmian_portraits_revisited) 6.0.1)

## Source Code

Hosted on [Github](https://github.com/corsairmarks/combined_silfae_revisited)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

## Methodology

Each of the source repositories above is added as a remote to this repository on my local machine.  I fetch all the repositories, then merge them into the `master` branch of this repository.

1. `git remote add <friendly-remote-name> <repo-url>`
2. `git fetch --all -n` to get all the commits, but not the tags
3. `git checkout master` (stash if you need to beforehand)
4. `git merge --no-commit --allow-unrelated-histories -m "merge version 1.2.3 from another repo" <friendly-remote-name>/<branch or commit hash>` (`--allow-unrelated-histories` is only required the first time an unrelated tree, i.e. new remote repo, is added - the first merge commit establishes history between the trees)
5. Solve merge conflicts, if any
6. `git merge --continue`

# Compatibility

Requires Stellaris 3.7 "Canis Minor" and disables achievements.

Check each of the contained mods for an explicit list of incompatibility notes.  Notably some Pop jobs (13 for the Holofrixits) are overridden.  These job overrides help Pops with Holofrixit caste traits be attracted to jobs for which they are well-suited.  If overridden by another mod, the job(s) in question will no longer attract Holofrixits based on their caste role, which could lead to some Pops working jobs they are less-suited for (primarily military-related jobs for normal empires, or "complex" drone jobs for gestalts).

## Dependencies

In order for this mod to function, you **must** install these mods (and load them _before_ this one):

* [Animated Aquilese Portraits](https://steamcommunity.com/workshop/filedetails/?id=910576007) by Silfae
* [Animated Asari Portraits - Mass Effect](https://steamcommunity.com/workshop/filedetails/?id=707779361) by Silfae
* [Animated Eldar Portraits - Warhammer 40K](https://steamcommunity.com/workshop/filedetails/?id=707415339) by Silfae
* [Animated Portraits - The Hidden Eye](https://steamcommunity.com/workshop/filedetails/?id=1168459329) by Silfae
* [Animated Hollow Portraits](https://steamcommunity.com/workshop/filedetails/?id=902526212) by Silfae
* [Holosphere Rising](https://steamcommunity.com/workshop/filedetails/?id=868965217) by Silfae
* [Animated Hyena Portraits](https://steamcommunity.com/workshop/filedetails/?id=1126014321) by Silfae
* [Animated Octee-lan Portraits](https://steamcommunity.com/workshop/filedetails/?id=929140455) by Silfae
* [Animated Quarian Portraits - Mass Effect](https://steamcommunity.com/workshop/filedetails/?id=708669421) by Silfae
* [Animated Raptor Portraits](https://steamcommunity.com/workshop/filedetails/?id=872596925) by Silfae
* [Animated Serpentoid Portraits](https://steamcommunity.com/workshop/filedetails/?id=861800679) by Silfae
* [Animated Shark Portraits](url=https://steamcommunity.com/workshop/filedetails/?id=1098915405) by Silfae
* [Animated Silicoid Portraits](https://steamcommunity.com/workshop/filedetails/?id=1160316076) by Silfae
* [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424) by Silfae
* [Silfae's city sets updated](https://steamcommunity.com/workshop/filedetails/?id=2247427791) by Nozeminer (devastated cities and ecumenopolis-level cities)
* [Building: Aquaponics Farms](https://steamcommunity.com/workshop/filedetails/?id=2768297949) by me (for Anglers starting on the Eldar custom system)
* [Special Leadership Privileges for Battle Thralls and Bio-Trophies](https://steamcommunity.com/workshop/filedetails/?id=2496357447) by me (for Holosphere's enslaved leaders)

These mods are not included as part of this mod so that the original authors get credit via mod subscriptions.

## When to Install

You should only add this mod before starting a new game, or remove it before starting a new game.  It should **not** be added to or removed from an in-progress game.

## Changelog

* 1.0.0 Initial version
* 1.0.1 Update Octee-lan portraits - resolves critical bug where starbases were the wrong type
* 2.0.0 All merged mods updated for Stellaris version 3.1 "Lem"
* 2.0.1 Update merged mods for Stellaris version 3.1.2
    * Updated: Animated Holosphere Portraits: Revisited at 2.0.1
    * Updated: Animated Silicoid Portraits: Revisited at 2.0.2
* 2.0.2 Update merged mods:
    * Animated Holosphere Portraits: Revisited at 2.0.2
    * Animated Hollow Portraits: Revisited at 2.1.0
    * Animated Silicoid Portraits: Revisited at 2.1.0
* 3.0.0 Update all merged mods for Stellaris version 3.2.2 "Herbert"
* 3.0.1 Update merged mod Animated Holosphere Portraits: Revisited at 3.0.1
* 3.0.2 Update merged mods with added diplomacy rooms - the files need to load before the built-in file in order to not overwrite built-in diplomacy room selection
    * Animated Hidden Eye Portraits: Revisited at 2.0.2
    * Animated Hollow Portraits: Revisited at 3.0.1
    * Animated Octee-lan Portraits: Revisited at 3.1.1
    * Animated Quarian Portraits: Revisited at 3.0.1
    * Animated Shark Portraits: Revisited at 2.0.1
* 3.0.3 Update merged mod Animated Holosphere Portraits: Revisited at 3.0.2
* 3.0.4 Update all merged mods
* 3.0.5 Update merged mod Animated Hidden Eye Portraits: Revisited at 2.0.4
* 4.0.0 Update all merged mods for Stellaris version 3.3 "Libra"
* 4.0.1 Update merged mods for Stellaris version 3.3.1
    * Updated: Animated Holosphere Portraits: Revisited at 4.0.1
    * Updated: Animated Silicoid Portraits: Revisited at 4.0.1
* 4.0.2 Update merged mods for Stellaris version 3.3.4
    * Updated: Animated Holosphere Portraits: Revisited at 4.0.2
* 5.0.0 Update all merged mods for Stellaris version 3.4 "Cepheus"
* 5.1.0 Update merged mod Animated Hollow Portraits: Revisited at 5.1.0
* 6.0.0 Update all merged mods for Stellaris version 3.6 "Orion"
* 7.0.0 Update all merged mods for Stellaris version 3.7 "Canis Minor"