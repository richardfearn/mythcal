# Changelog

## [Unreleased]

### Changed

- Replace `print` statements with proper logging
- Migrate away from OAuth out-of-band flow

## [31.0] - 2020-05-25

### Added

- Include current/future recordings in "MythTV updated" event description
- Include date of next recording in "MythTV updated" event description

### Changed

- Convert to Python 3
- Update version numbering scheme to match MythTV (remove `0.` prefix)
- Time zone setting (`timezone` in `[mythtv]` section) is no longer required (it hasn't been used since 2014)
- Update `README`, and convert it to Markdown
- Convert this changelog to the [Keep a Changelog] format
- Refactor and reformat `mythcal`; fix issues reported by pylint and flake8

### Removed

- Remove unused code
- Remove `timezones` script

## [0.27.1] - 2015-03-14

### Fixed

- Don't add live programmes to the calendar. ([Issue 16](https://github.com/richardfearn/mythcal/issues/16))


## [0.27.0] - 2014-12-23

### Changed

- Update to use Calendar v3 API.

- Changes to settings in `mythcal.conf`:

   - The `[google]` section is no longer required. Credentials are stored in a new file, `mythcal.credentials`, which is set up using `mythcal --auth`. See the `README` for more information.

   - In the `[calendar]` section, `name` and `max_batch_size` are no longer required and can be removed.

- Simplify time zone handling.

[Unreleased]: https://github.com/richardfearn/mythcal/compare/31.0...HEAD
[31.0]: https://github.com/richardfearn/mythcal/compare/0.27.1...31.0
[0.27.1]: https://github.com/richardfearn/mythcal/compare/0.27.0...0.27.1
[0.27.0]: https://github.com/richardfearn/mythcal/tree/0.27.0

[Keep a Changelog]: https://keepachangelog.com/en/1.0.0/
