# Overview

This mod is a compilation of my adaptations of Silfae's portrait mods.  Please see the description of each individual mod for what the effects are.

Individual mods update first, then changes are merged here.

# Bundled Mods

This is a bundle of mods to make it a little easier to sub and ensure cross-compatibility with each-other.  Please check each individual mod for the effects and any known issues.  The large hex strings are the commit hashes - that is mostly for my own record-keeping to know what revision of the other source code is contained here.

* [Animated Aquilese Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2576769521) ([Source](https://github.com/corsairmarks/romaneagles_portraits_revisited) bb39ea81cdec49c85ba6e095f4c639873263fd9e)
* [Animated Asari Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2581752619) ([Source](https://github.com/corsairmarks/asari_portraits_revisited) 704c7f23ad90d9b523fa29d9db3c32eda72f2e05)
* [Animated Eldar Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2581388205) ([Source](https://github.com/corsairmarks/eldar_portraits_revisited) f1dd150f80ff47b99fee42d934eb061476d4fd9e)
* [Animated Hidden Eye Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2585946800) ([Source](https://github.com/corsairmarks/slreptilian_portraits_revisited) b9701925aa6c83d0e9a852b573e35125b70904cc)
* [Animated Hollow Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2578037235) ([Source](https://github.com/corsairmarks/horrorworm_portraits_revisited) 4e179313ffd7e96b797938219ec948db1bef74ee)
* [Animated Holosphere Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2592592503) ([Source](https://github.com/corsairmarks/holosphere_rising_revisited) ebdbc692a09fa8e5f5f8ca82b56d4da6c4f85c2f)
* [Animated Hyena Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2576290763) ([Source](https://github.com/corsairmarks/hyenafolk_portraits_revisited) 5e0c29ee2642a522e95b553655c79e415aa0ca01)
* [Animated Octee-lan Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2584680339) ([Source](https://github.com/corsairmarks/octeelan_portraits_revisited) 15efdcfdb7769ad8a1b5c3fbd6ec5e3e2a543f17)
* [Animated Quarian Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2583358569) ([Source](https://github.com/corsairmarks/quarian_portraits_revisited) 7cab66b6687ece28f76d0020c7a7363522660053)
* [Animated Raptor Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2577216891) ([Source](https://github.com/corsairmarks/saurischian_portraits_revisited) 829f3f82ea0634a35a83a1af92efcb4f014b51fd)
* [Animated Serpentoid Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2577093634) ([Source](https://github.com/corsairmarks/serpentoid_portraits_revisited) 4fc3b2a09d37cfa9526eba9f84337659061f288d)
* [Animated Shark Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2585030748) ([Source](https://github.com/corsairmarks/sharkanian_portraits_revisited) 8fa3453b461b378d71aef76d0503c44da2565b47)
* [Animated Silicoid Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2579736379) ([Source](https://github.com/corsairmarks/silicoid_portraits_revisited) 9ed56e37bf7b3ae41d5ab37df8489381a9cb63e8)
* [Animated Xirmian Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2577789863) ([Source](https://github.com/corsairmarks/xirmian_portraits_revisited) 4e47adddcdf71c0658e9c4e6515869483fb3b780)

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

Requires Stellaris 3.2.2 "Herbert" and disables achievements.

Check each of the contained mods for an explicit list of incompatibility notes.  Notably almost all Pop jobs and all Pop strata are overwritten (primarily for the Holosphere but also Silicoids), making this mod incompatible with other mods that make changes to Pop jobs or strata.

## Dependencies

In order for this mod to function, you **must** install these mods (and load them _before_ this one):

* [Animated Aquilese Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=910576007) by Silfae
* [Animated Asari Portraits - Mass Effect](https://steamcommunity.com/sharedfiles/filedetails/?id=707779361) by Silfae
* [Animated Eldar Portraits - Warhammer 40K](https://steamcommunity.com/sharedfiles/filedetails/?id=707415339) by Silfae
* [Animated Portraits - The Hidden Eye](https://steamcommunity.com/sharedfiles/filedetails/?id=1168459329) by Silfae
* [Animated Hollow Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=902526212) by Silfae
* [Holosphere Rising](https://steamcommunity.com/sharedfiles/filedetails/?id=868965217) by Silfae
* [Animated Hyena Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=1126014321) by Silfae
* [Animated Octee-lan Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=929140455) by Silfae
* [Animated Quarian Portraits - Mass Effect](https://steamcommunity.com/sharedfiles/filedetails/?id=708669421) by Silfae
* [Animated Raptor Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=872596925) by Silfae
* [Animated Serpentoid Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=861800679) by Silfae
* [Animated Shark Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=2585030748) by Silfae
* [Animated Silicoid Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=1160316076) by Silfae
* [Animated Xirmian Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=881118424) by Silfae
* [Silfae's city sets updated](https://steamcommunity.com/sharedfiles/filedetails/?id=2247427791) by Nozeminer (devastated cities and ecumenopolis-level cities)
* [Full Military Service for Battle Thralls](https://steamcommunity.com/sharedfiles/filedetails/?id=2496357447) by me (for Holosphere's enslaved leaders)

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