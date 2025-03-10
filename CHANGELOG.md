# CHANGELOG

## 0.15.5

* Use absolute path to package project directory, when it's different from repo root

## 0.15.4

* Don't execute shell as a program explicitly (#10)

## 0.15.3

* Show output from hooks (#8)

## 0.15.0

* Add universal os support via `python` hooks [#4](https://github.com/TobiasTimm/husky-hg/pull/4)

## 0.14.4

* Fix missing hooks for `hg` [#3](https://github.com/TobiasTimm/husky-hg/issues/3)

## 0.14.3

* Fix handle space in `PATH` [#150](https://github.com/typicode/husky/pull/114)

## 0.14.2

* Fix handle space in `HOME`

## 0.14.1

* Fix Git hooks install on Windows
* Fix hook script when `nvm` was installed with Brew

## 0.14.0

* Fix `npm@5` `Error: Cannot find module` warning when uninstalling
* Drop `Node 0.12` support
* Don't reload `nvm` if it's already in `PATH`
* Add Git worktree support [#114](https://github.com/typicode/husky/pull/114)
* Hide irrelevant `--no-verify` message for `prepare-commit-msg` [#137](https://github.com/typicode/husky/issues/137)

## 0.13.4

* Add Node version to husky output

## 0.13.3

* Revert `Fixes issue with OS X + brew where nvm was loaded even when npm was already present` that was introduced in `v0.13.0` as it was preventing Husky to load `nvm` in some cases [#106](https://github.com/typicode/husky/issues/106)

## 0.13.2

* Fixes issue [#103](https://github.com/typicode/husky/issues/103)

## 0.13.1

* Makes it easier for projects to transition from [ghooks](https://github.com/gtramontina/ghooks) by detecting ghooks installed scripts and automatically migrating them

## 0.13.0

* Makes `husky` a little less verbose by default
* Fixes issue with `OS X + brew` where `nvm` was loaded even when `npm` was already present
* Fixes issue with Git `v1.9` on Windows
* Prevents Git hooks being installed when husky is in a sub `node_modules` directory (i.e. `./node_modules/A/node_modules/husky`)

## 0.12.0

* Adds Git submodule support
* Adds Cygwin support
* Improves edge cases support (`.git` not found and `git` not in `PATH`)
* If `npm` is already present in path, doesn't load `nvm` default or `.nvmrc` version, which makes things faster in terminal. In GUI apps, the behavior is unchanged.
