# Ansible role for openssh-server

An Ansible role for `openssh-server`. Includes sensible defaults that can be overridden.

## Default variables

Default variables are defined in `defaults/main.yml`. To override them set the variables as you [normally would][1] in your Ansible scripts.

|Variable|Default|Documentation|
|---|---|---|
|`ssh_port` | 22 | [Documentation][2] |
|`ssh_password_authentication` | false | [Documentation][3] |
|`ssh_protocol` | true |  |
|`ssh_use_pam` | false | |
|`ssh_permit_root_login` | false | [Documentation][4] |
|`ssh_allow_users` | false | [Documentation][5] |

[1]: http://docs.ansible.com/ansible/playbooks_variables.html
[2]: https://man.openbsd.org/sshd_config#Port
[3]: https://man.openbsd.org/sshd_config#PasswordAuthentication
[4]: https://man.openbsd.org/sshd_config#PermitRootLogin
[5]: https://man.openbsd.org/sshd_config#AllowUsers
