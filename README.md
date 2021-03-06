# Ansible Role: Vagrant

[![Build Status](https://travis-ci.org/pixelart/ansible-role-vagrant.svg?branch=master)](https://travis-ci.org/pixelart/ansible-role-vagrant)

Installs [Vagrant](https://www.vagrantup.com/) on Ubuntu or Debian.

## Requirements

  - `virtualbox` or any other vm provider should be installed and working.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    vagrant_version: '1.9.4'

The version of Vagrant which should be installed.

    vagrant_manage_sudoers: false

If the sudoers file should be managed for passwordless vagrant up/down if using NFS. If true, a `/etc/sudoers.d/vagrant-syncedfolders` will be created and the `#includedir /etc/sudoers.d` directive activated. This is managed only for Ubuntu now. On Ubuntu the user must be in the `sudo` group.

    vagrant_plugin_users: []
    
Add a list of user account names for which vagrant plugins should be installed.

    vagrant_plugins: []

Add a list of vagrant with a `name` and (optional) `version` constraint or specific version to be installed for the users above. For example:

```yaml
vagrant_plugins:
  # Install a higher version than supplied by the system
  - name: vagrant-share
    version: '>=1.1.8'
  # Install the latest stable release of a plugin.
  - name: vagrant-cachier
```

    vagrant_plugins_keep_updated: false
    
Set to true if you want to keep the vagrant plugins installed updated. If you set this to true, only plugins without version constraint above are updated. Install with specific version and update is mutually exclusive.

## Dependencies

None.

## Example Playbook

    - hosts: phpdevs
      vars_files:
        - vars/main.yml
      roles:
        - pixelart.vagrant
        
*Inside `vars/main.yml`*:

    vagrant_plugin_users: ['username']
    vagrant_plugins:
      - name: vagrant-bindfs
      - name: vagrant-cachier
      - name: vagrant-hostmanager
      - name: vagrant-vbguest

After the playbook runs, `vagrant` will be accessible via normal user accounts.

## Code of Conduct

Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

## License

MIT, see the [LICENSE](LICENSE) file.

## Author Information

This role was created in 2017 by [pixelart GmbH](https://www.pixelart.at/).
