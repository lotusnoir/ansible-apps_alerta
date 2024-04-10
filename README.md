# ansible-apps_alerta

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_alerta-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_alerta)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_alerta.svg)](https://github.com/lotusnoir/ansible-apps_alerta/releases/latest)
[![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_alerta?color=orange&style=flat)](https://galaxy.ansible.com/lotusnoir/apps_alerta)
[![downloads](https://img.shields.io/ansible/role/d/56088)](https://galaxy.ansible.com/lotusnoir/apps_alerta)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/56088)](https://galaxy.ansible.com/lotusnoir/apps_alerta)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Description](#description)
- [Requirements](#requirements)
- [Role variables](#role-variables)
- [Examples](#examples)
- [License](#license)
- [Author Information](#author-information)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Description

Deploy [alerta](https://docs.alerta.io/en/latest/) a monitoring web interface.
## Requirements

This role doest not install the following requierements:
  - nginx
  - pip
  - git


## Role variables

See [variables](/defaults/main.yml) for more details.

## Examples

        ---
        - hosts: apps_alerta
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_alerta


## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

## Author Information

- [Philippe LEAL](https://github.com/lotusnoir)
