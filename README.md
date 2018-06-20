# ansible-role-sysctl

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-sysctl.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-sysctl)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-sysctl-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/sysctl)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - Configure kernel parameters at runtime

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    sysctl_conf: {}
    sysctl_d: []

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.sysctl
          sysctl_conf:
            kernel.dmesg_restrict: 1
          sysctl_d:
            - file: ansible
              order: 99
              settings:
                kernel.modules_disabled: 1

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
