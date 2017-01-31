# Ansible Role: Vagrant

[![Build Status](https://travis-ci.org/pixelart/ansible-role-vagrant.svg?branch=master)](https://travis-ci.org/pixelart/ansible-role-vagrant)

Installs [Vagrant](https://www.vagrantup.com/) on Ubuntu or Debian.

## Requirements

  - `virtualbox` or any other vm provider should be installed and working.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    vagrant_version: '1.9.1'

The version of Vagrant which should be installed.

## Dependencies

None.

## Example Playbook

    - hosts: phpdevs
      roles:
        - pixelart.vagrant

After the playbook runs, `vagrant` will be accessible via normal user accounts.

## License

MIT, see the [LICENSE](LICENSE) file.

## Author Information

This role was created in 2017 by [pixelart GmbH](https://www.pixelart.at/).
