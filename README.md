# Ansible role for openssh-server

[![Build Status](https://travis-ci.org/shapeshed/openssh-server.svg?branch=master)](https://travis-ci.org/shapeshed/openssh-server)

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
|`ssh_x11_forwarding` | false | [Documentation][6] |

## Development

To develop the role an `ansible.cfg` should be added.

    { echo '[defaults]'; echo 'roles_path = ../'; } >> ansible.cfg


A [Vagrant][7] file is provided to support development of this role. To bring up a Virtual Machine and provision it with the role run

    vagrant up

If you want to poke about inside the Virtual Machine to run 

    vagrant ssh

If you make changes and want to run the provisioner again run

    vagrant provision

To start again run

    vagrant destroy && vagrant up

[1]: http://docs.ansible.com/ansible/playbooks_variables.html
[2]: https://man.openbsd.org/sshd_config#Port
[3]: https://man.openbsd.org/sshd_config#PasswordAuthentication
[4]: https://man.openbsd.org/sshd_config#PermitRootLogin
[5]: https://man.openbsd.org/sshd_config#AllowUsers
[6]: https://man.openbsd.org/sshd_config#X11Forwarding
