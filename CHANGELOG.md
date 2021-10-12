# Changelog

All notable changes to this project will be documented in this file.

- [2.0.0 (2021-10-12)](#200-2021-10-12)
- [1.4.1 (2020-10-22)](#141-2020-10-22)
- [1.4.0 (2020-10-01)](#140-2020-10-01)
- [1.3.2 (2020-06-22)](#132-2020-06-22)
- [1.3.1 (2020-06-04)](#131-2020-06-04)
- [1.3.0 (2020-06-02)](#130-2020-06-02)
- [1.2.0 (2020-06-01)](#120-2020-06-01)
- [1.1.0 (2020-02-08)](#110-2020-02-08)

---

<a name="2.0.0"></a>
## [2.0.0](https://github.com/aisbergg/ansible-role-systemd-resolved/compare/v1.4.1...v2.0.0) (2021-10-12)

### CI Configuration

- add Github action for automatic releases

### Chores

- update changelog
- update development configs
- **.ansible-lint:** update linter config
- **.pre-commit-config.yaml:** bump pre-commit hook versions
- **CHANGELOG.tpl.md:** update changelog template
- **requirements.yml:** add role requirements

### Code Refactoring

- drop support for Ansible < 2.10

### Documentation

- **README.md:** update role name


<a name="1.4.1"></a>
## [1.4.1](https://github.com/aisbergg/ansible-role-systemd-resolved/compare/v1.4.0...v1.4.1) (2020-10-22)

### Chores

- **CHANGELOG.md:** update changelog

### Features

- add option `ReadEtcHosts` only for `systemd>=240`


<a name="1.4.0"></a>
## [1.4.0](https://github.com/aisbergg/ansible-role-systemd-resolved/compare/v1.3.2...v1.4.0) (2020-10-01)

### Bug Fixes

- forcefully flush handlers

### Chores

- **CHANGELOG.md:** update changelog


<a name="1.3.2"></a>
## [1.3.2](https://github.com/aisbergg/ansible-role-systemd-resolved/compare/v1.3.1...v1.3.2) (2020-06-22)

### Bug Fixes

- galaxy tags

### Chores

- **CHANGELOG.md:** update changelog

### Features

- add condition to installation


<a name="1.3.1"></a>
## [1.3.1](https://github.com/aisbergg/ansible-role-systemd-resolved/compare/v1.3.0...v1.3.1) (2020-06-04)

### Features

- remove restart on-failure option


<a name="1.3.0"></a>
## [1.3.0](https://github.com/aisbergg/ansible-role-systemd-resolved/compare/v1.2.0...v1.3.0) (2020-06-02)

### Chores

- **CHANGELOG.md:** update changelog

### Features

- configure nsswitch
- use systemd-resolved dns plugin in NM


<a name="1.2.0"></a>
## [1.2.0](https://github.com/aisbergg/ansible-role-systemd-resolved/compare/v1.1.0...v1.2.0) (2020-06-01)

### Bug Fixes

- correct Ansible version requirement

### Chores

- add bump2version config

### Features

- update role
- update variable names


<a name="1.1.0"></a>
## [1.1.0]() (2020-02-08)

Initial Release
