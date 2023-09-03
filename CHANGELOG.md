# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

<!-- As much as possible use subsections: Added, Removed, Changed, BugFix -->

## [0.0.4] - 2023-09-03

### Added

- Usage example in `README.md`

### Changed

- Hash in file replacement : if file contains an incorrect hash in file name and `--overwrite` is set, the original hash is kept next to the correct/new hash. This is done to keep history of overridden hashes and deal with file name elements incorrectly interpreted as hash. _WARNING: this may lead to file names that exceed file system length limits (in which case renaming would fail)_
  > `[<original_hash>]` => `[!<original_hash>][<new_hash>]`
- Frozen directory hash file: its content is sorted to remove a point of variability

## [0.0.3] - 2023-08-27

### Added

- Concept of `frozen directories`: see `README.md`
  > New related fields: ``--skip_frozen_dirs``, ``--frozen_dirs``, ``--frozen_dir_file_ext``

### Changed

- `--min_size`: added support for human-readable numbers with SI suffix like `-4.4k` and `87G`
- `--write_report`: Now an option enabled via CLI argument
- `--debug`: now hidden from `--help`
- To reduce the number of messages printed, messages related to skipping files are now only enabled with `--debug`

## [0.0.2] - 2023-08-26

### Added

- `--skip_verify`: Skip verification; only process files with no hash in filename
- `--debug`: Debug mode (undocumented on purpose)

### BugFix

- fixed infinite recursion loop

## [0.0.1] - 2023-08-26

__INITIAL RELEASE__