# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.4.0] - 2020-10-01
### Changed
- Handlers will be forcefully flushed to apply config changes right away

## [1.3.2] - 2020-06-22
### Fixed
- Run installation task only, if any packages need to be installed
- Galaxy tags

## [1.3.1] - 2020-06-04
### Fixed
- Remove restart on-failure option, defaults to always anyway

## [1.3.0] - 2020-06-02
### Added
- Configure nsswitch

### Changed
- Use systemd-resolved plugin in Network Manager

## [1.2.0] - 2020-06-01
### Added
- Option to disable other resolvers (`systemd_resolved_disable_other_resolvers`)
- Tags to all tasks (`systemd-resolved`, `resolved`, `dns`)
- Role will disable DNS in Network Manager if it is present

### Changed
- Correct required Ansible version

## [1.1.0] - 2020-02-08
### Changed
- Change name of config variables to match the names documented in resolved.conf(5)

## [1.0.0] - 2020-02-07
### Added
- First version of the role
