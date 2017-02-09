# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/) 
and this project adheres to [Semantic Versioning](http://semver.org/).

## [1.2.2] - 2017-02-09
### Fixed
- Fix managed sudoers file for change occurred in Vagrant 1.9.1

## [1.2.1] - 2017-02-02
### Fixed
- Add missing leading zero on the sudoers file permissions

## [1.2.0] - 2017-02-02
### Added
- Manage sudoers file for passwordless vagrant up/down with NFS

## [1.1.0] - 2017-02-01
### Added
- Add installation of vagrant plugins for given users

### Changed
- Ignore irrelevant files on galaxy installs

## [1.0.0] - 2017-01-31
### Added
- Created the role to provision Vagrant
- Add variable to define the Vagrant version to be installed
- Test the role on Ubuntu 16.04 and Debian 8

[Unreleased]: https://github.com/pixelart/ansible-role-vagrant/compare/1.2.2...HEAD
[1.2.2]: https://github.com/pixelart/ansible-role-vagrant/compare/1.2.1...1.2.2
[1.2.1]: https://github.com/pixelart/ansible-role-vagrant/compare/1.2.0...1.2.1
[1.2.0]: https://github.com/pixelart/ansible-role-vagrant/compare/1.1.0...1.2.0
[1.1.0]: https://github.com/pixelart/ansible-role-vagrant/compare/1.0.0...1.1.0
[1.0.0]: https://github.com/pixelart/ansible-role-vagrant/compare/bafa1aa...1.0.0
