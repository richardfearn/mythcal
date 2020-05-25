# Changelog

## [0.27.0] - 2014-12-23

### Changed

- Update to use Calendar v3 API.

- Changes to settings in `mythcal.conf`:

   - The `[google]` section is no longer required. Credentials are stored in a new file, `mythcal.credentials`, which is set up using `mythcal --auth`. See the `README` for more information.

   - In the `[calendar]` section, `name` and `max_batch_size` are no longer required and can be removed.

- Simplify time zone handling.

[0.27.0]: https://github.com/richardfearn/mythcal/tree/0.27.0
