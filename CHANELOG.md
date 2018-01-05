# Changelog


## [Unreleased]
### Added

### Changed

### Removed


## [0.14.0]
### Added
- Explicit & configurable `Settings` struct.
    - These are the configurable settings used by the `Config` type
      are were previously only configurable in a file
    - Migrant.toml config files can be replaced by `Settings` configured in source.
- `Config::with_settings` for initializing a `Config` from `Settings`

### Changed
- Config file renamed from `.migrant.toml` to `Migrant.toml`
    - In sqlite configs, `database_name` parameter is now `database_path`
      and can be either an absolute or relative (to the config file dir) path.
    - Config file must be renamed (and `database_name` changed to `database_path`)
      or re-initialized.
- `Config::load_file_only` renamed to `Config::from_settings_file`
- `search_for_config` renamed to `search_for_settings_file`
- Output from `Config::setup` is now only shown in debug logs (`debug!` macro)
- Move to separate repo (apart from `migrant` the cli tool)

### Removed
