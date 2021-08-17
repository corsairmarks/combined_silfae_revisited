# Overview

This mod is a compilation of my adaptations of Silfae's portrait mods.  Please see the description of each individual mod for what the effects are.

Individual mods update first, then changes are merged here.

# Bundled Mods

This is a bundle of mods to make it a little easier to sub.  Please check each individual mod for the effects and any known issues.  The large hex strings are the commit hashes - that is mostly for my own record-keeping to know what revision of the other source code is contained here.

* [Animated Aquilese Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2576769521) ([Source](https://github.com/corsairmarks/romaneagles_portraits_revisited) affa2af4656ca9c63d7d371e49b165ae1ee08106)
* [Animated Hyena Portraits: Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2576290763) ([Source](https://github.com/corsairmarks/hyenafolk_portraits_revisited) 2fa586d0e1d4086bf7be4c3491da1e0a0a62c2b1)

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

* [Animated Hyena Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=1126014321) by Silfae
* [Silfae's city sets updated](https://steamcommunity.com/sharedfiles/filedetails/?id=2247427791) by Nozeminer

These mods are not included as part of this mod so that the original authors get credit via mod subscriptions.

## When to Install

You should only add this mod before starting a new game, or remove it before starting a new game.  It should **not** be added to or removed from an in-progress game.

## Changelog

* 1.0.0 Initial version