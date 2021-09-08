# Overview

This mod is a compilation of my adaptations of Silfae's portrait mods.  Please see the description of each individual mod for what the effects are.

Individual mods update first, then changes are merged here.

# Bundled Mods

This is a bundle of mods to make it a little easier to sub and ensure cross-compatibility with each-other.  Please check each individual mod for the effects and any known issues.  The large hex strings are the commit hashes - that is mostly for my own record-keeping to know what revision of the other source code is contained here.

* [Animated Asari Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2581752619) ([Source](https://github.com/corsairmarks/asari_portraits_revisited) ede7e83760c484f791a62ffdecd97a41c578624d)
* [Animated Aquilese Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2576769521) ([Source](https://github.com/corsairmarks/romaneagles_portraits_revisited) 0f53196e0c167612451d03bac957a663fbf954bb)
* [Animated Eldar Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2581388205) ([Source](https://github.com/corsairmarks/eldar_portraits_revisited) 171c79ee115a6214f9e86f20239ef3c5992ac797)
* [Animated Hidden Eye Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2585946800) ([Source](https://github.com/corsairmarks/slreptilian_portraits_revisited) XXX)
* [Animated Hollow Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2578037235) ([Source](https://github.com/corsairmarks/horrorworm_portraits_revisited) eb81b8b47c4e0f5c2fdecf4526fc646c148ccfee)
* [Animated Holosphere Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2592592503) ([Source](https://github.com/corsairmarks/holosphere_rising_revisited) bbe45fd482e793c80c7dbca146f42f1f95ed3793)
* [Animated Hyena Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2576290763) ([Source](https://github.com/corsairmarks/hyenafolk_portraits_revisited) a4bcbdea5b7f2919cf2e3c69a2965df1e837b6f5)
* [Animated Octee-lan Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2584680339) ([Source](https://github.com/corsairmarks/octeelan_portraits_revisited) XXX)
* [Animated Quarian Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2583358569) ([Source](https://github.com/corsairmarks/quarian_portraits_revisited) c0af7d1eccfd8243c5911be9718cc5b634431c79)
* [Animated Raptor Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2577216891) ([Source](https://github.com/corsairmarks/saurischian_portraits_revisited) cc25708b88e17e2ea1a4c15322bc4579702ec0aa)
* [Animated Serpentoid Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2577093634) ([Source](https://github.com/corsairmarks/serpentoid_portraits_revisited) f68157f050ceb17e82686e00a82097d89de713f3)
* [Animated Shark Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2585030748) ([Source](https://github.com/corsairmarks/sharkanian_portraits_revisited) XXX)
* [Animated Silicoid Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2579736379) ([Source](https://github.com/corsairmarks/silicoid_portraits_revisited) XXX)
* [Animated Xirmian Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2577789863) ([Source](https://github.com/corsairmarks/xirmian_portraits_revisited) XXX)

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

Requires Stellaris 3.0.* and disables achievements.

Check each of the contained mods for an explicit list of incompatibility notes.

## Dependencies

In order for this mod to function, you **must** install these mods (and load them _before_ this one):

* [Animated Asari Portraits - Mass Effect](https://steamcommunity.com/sharedfiles/filedetails/?id=707779361) by Silfae
* [Animated Aquilese Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=910576007) by Silfae
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