# Ansible Role: ansible-apps_alerta

## Description


[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_alerta.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_alerta)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_alerta-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_alerta)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_alerta?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_alerta)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_alerta.svg)](https://github.com/lotusnoir/ansible-apps_alerta/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_alerta&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_alerta)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_alerta&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_alerta)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_alerta&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_alerta)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_alerta&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_alerta)

Deploy [alerta](https://docs.alerta.io/en/latest/) a monitoring web interface.

## Requierements

This role doest not install the following requierements:
  - nginx
  - pip
  - git

## Role variables

| Name                           | Default Value | Description                        |
| -------------------------      | ------------- | -----------------------------------|
| `alerta_install_dir`           | /opt/alerta | directory to install binary |
| `alerta_force_install`         | false       | force install variable |
| `alerta_auth_required`         | true        |  |
| `alerta_secretkey`             |  |  |
| `alerta_admin_users`           |  |  |
| `alerta_allowed_email_domains` |  |  |
| `alerta_allowed_environments`  |  |  |
| `alerta_plugins_list`          |  |  |
| `alerta_enabled_plugins`       |  |  |
| `alerta_severity_options`      | |  |
| `alerta_color_options`         | |  |
| `alerta_extra_conf_options`    | |  |
| `alerta_ldap_enable`           | |  |
| `alerta_ldap_options`          | |  |
| `alerta_keycloak_enable`       | |  |
| `alerta_keycloak_options`      | |  |

## Examples

	---
	- hosts: apps_alerta
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_alerta
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
