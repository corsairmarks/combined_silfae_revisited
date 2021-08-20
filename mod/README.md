# Overview

Summary

# Changes

Notes

* Update the namelist to account for all built-in army types, remove obsolete entries
* Add custom trait to Eldar that makes their leaders begin at an older age, but live longer
* Update prescripted empire for 3.0
    * Now has Origin: Remnants (requires Ancient Relics)
    * You can use the portraits for your own empire without any DLC requirements
    * Can randomly spawn
    * Prescripted empire gains Psionic Theory for free
    * Names are a somewhat more lore-friendly
* Rebuilt challenge-start custom solar system initializer for 3.0:
    * Setup to work correctly for all origins/civics in unmodded Stellaris that do not restrict the starting system initializers (i.e. Origin Shattered Ring or Origin: Void Dwellers)
    * Add modified starting deposits for use with Origin: Remnants

## Compatibility

Notes

## Changelog

* 1.0.0 Initial version

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/eldar_portraits_revisited)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.