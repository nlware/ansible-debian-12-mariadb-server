## debian-12-mariadb-server

[![CI](https://github.com/nlware/ansible-debian-12-mariadb-server/workflows/CI/badge.svg)](https://github.com/nlware/ansible-debian-12-mariadb-server/actions?query=workflow%3ACI)

Ansible role to set up a MariaDB server on Debian 12.

#### Variables

* `debian_12_mariadb_server_root_password`: [required]: Root password

* `debian_12_mariadb_server_certificates_present`: [default: `{}`]: SSL certificates to create
* `debian_12_mariadb_server_certificates_absent`: [default: `[]`]: SSL certificates to remove

* `debian_12_mariadb_server_configuration_files_present`: [default: `{}`]: Configuration files to create
* `debian_12_mariadb_server_configuration_files_absent`: [default: `[]`]: Configuration files to remove

#### Examples

##### Minimal (set root password only)

```yaml
---
- hosts: all
  roles:
    - debian-12-mariadb-server
  vars:
    debian_12_mariadb_server_root_password: 'this-is-a-test-password'
```
