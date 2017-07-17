# Ansible role for openssh-server

An Ansible role for `openssh-server`. Includes sensible defaults that can be overridden.

## Default variables

Default variables are defined in `defaults/main.yml`. To override them set the variables as you [normally would][1] in your Ansible scripts.

|variable|default|
|---|---|
|`ssh_port` | 22 |
|`ssh_password_authentication` | false |
|`ssh_protocol` | true |
|`ssh_use_pam` | false |
|`ssh_permit_root_login` | false |
|`ssh_allow_users` | false |

[1]: http://docs.ansible.com/ansible/playbooks_variables.html
