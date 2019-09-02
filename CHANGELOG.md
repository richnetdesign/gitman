# 2.0 (unreleased)

- TBD

# 1.7 (2019-08-07)

- **BREAKING**: Renamed `-f` alias to `-F` (`-f` now implies `--force-interactive`).
- Added `--force-interactive` option to interactively overwrite changed dependencies on install or update command. (@daniel-brosche)
- Added basic group support. (@daniel-brosche)
- Improved validity check of git repo. (@mttjohnson)
- Added rebuilding missing repo on `install --force`. (@mttjohnson)
- Added support for symlinks on Windows. (@sergey-shuyskiy)

# 1.6 (2019-01-26)

- **BREAKING**: Dropped support for Python 3.5.
- Added `git svn` support. (@daniel-brosche)
- Added `$GITMAN_CACHE_DISABLE` to disable repository mirrors. (@daniel-brosche)
- Added `--skip-changes` option to skip changed dependencies on install or update command. (@daniel-brosche)

# 1.5 (2018-09-08)

- **BREAKING**: Removed confusing `--lock` option on `update` command in favor of just using the `lock` command.
- **BREAKING**: Renamed `--no-lock` to `--skip-lock` on `update` command.
- **BREAKING**: Renamed `--no-dirty` to `--fail-if-dirty` on `list` command.
- Added `--keep-location` option on `uninstall`. (@DavidWatkins)
- Added feature to enable sparse checkouts. See the docs for further information. (@xenji)

# 1.4 (2017-03-21)

- Allow config files to exist in subdirectories of the main project.
- Added `$GITMAN_CACHE` to customize the repository cache location.

# 1.3 (2017-02-03)

- Added `init` command to generate sample config files.
- Added support for post-install scripts on dependencies.
- Updated config format to support `null` for links.

# 1.2 (2017-01-08)

- Added preliminary Windows support. (@StudioEtrange)

# 1.1 (2017-01-06)

- Added coloring to the command-line output.
- Fixed issue where `<dirty>` could be saved as a locked revision.

# 1.0.2 (2016-07-28)

- Moved documentation to http://gitman.readthedocs.io/.

# 1.0.1 (2016-05-31)

- Replaced calls to `git remote add origin` with `git remote set-url origin`.

# 1.0 (2016-05-22)

- Initial stable release.

# 0.11 (2016-05-10)

- Removed dependency on `sh` to support Cygwin/MinGW/etc. on Windows.
- Dropped Python 3.4 support for `subprocess` and `*args` improvements.
- **BREAKING**: Renamed config file key `dir` to `name`.

# 0.10 (2016-04-14)

- Added `show` command to display dependency and internal paths.

# 0.9 (2016-03-31)

- Added `edit` command to launch the config file.
- Depth now defaults to 5 to prevent infinite recursion.
- Fixed handling of source lists containing different dependencies.

# 0.8.3 (2016-03-14)

- Renamed to GitMan.

# 0.8.2 (2016-02-24)

- Updated to YORM v0.6.

# 0.8.1 (2016-01-21)

- Added an error message when attempting to lock invalid repositories.

# 0.8 (2016-01-13)

- Switched to using repository mirrors to speed up cloning.
- Disabled automatic fetching on install.
- Added `--fetch` option on `install` to always fetch.
- Now displaying `git status` output when there are changes.

# 0.7 (2015-12-22)

- Fixed `git remote rm` command. (@hdnivara)
- Now applying the `update` dependency filter to locking as well.
- Now only locking previous locked dependencies.
- Added `lock` command to manually save all dependency versions.
- Now requiring `--lock` option on `update` to explicitly lock dependencies.

# 0.6 (2015-11-13)

- Added the ability to filter the dependency list on `install` and `update`.
- Added `--depth` option to limit dependency traversal on `install`, `update`, and `list`.

# 0.5 (2015-10-20)

- Added Git plugin support via: `git deps`.
- Removed `--no-clean` option (now the default) on `install` and `update`.
- Added `--clean` option to delete ignored files on `install` and `update`.
- Switched to `install` rather than `update` of nested dependencies.
- Added `--all` option on `update` to update all nested dependencies.
- Disabled warnings when running `install` without locked sources.
- Added `--no-lock` option to disable version recording.

# 0.4.2 (2015-10-18)

- Fixed crash when running with some sources missing.

# 0.4.1 (2015-09-24)

- Switched to cloning for initial working tree creation.

# 0.4 (2015-09-18)

- Replaced `install` command with `update`.
- Updated `install` command to use locked dependency versions.
- Now sorting sources after a successful `update`.
- Now requiring `--force` to `uninstall` with uncommitted changes.
- Updated `list` command to show full shell commands.

# 0.3.1 (2015-09-09)

- Ensures files are not needlessly reloaded with newer versions of YORM.

# 0.3 (2015-06-26)

- Added `--no-clean` option to disable removing untracked files.
- Added support for `rev-parse` dates as the dependency `rev`.

# 0.2.5 (2015-06-15)

- Added `--quiet` option to hide warnings.

# 0.2.4 (2015-05-19)

- Now hiding YORM logging bellow warnings.

# 0.2.3 (2015-05-17)

- Upgraded to YORM v0.4.

# 0.2.2 (2015-05-04)

- Specified YORM < v0.4.

# 0.2.1 (2015-03-12)

- Added automatic remote branch tracking in dependencies.
- Now requiring `--force` when there are untracked files.

# 0.2 (2015-03-10)

- Added `list` command to display current URLs/SHAs.

# 0.1.4 (2014-02-27)

- Fixed an outdated index when checking for changes.

# 0.1.3 (2014-02-27)

- Fixed extra whitespace when logging shell output.

# 0.1.2 (2014-02-27)

- Added `--force` argument to:
    - overwrite uncommitted changes
    - create symbolic links in place of directories
- Added live shell command output with `-vv` argument.

# 0.1 (2014-02-24)

- Initial release.
