# Ansible Role : setup_ssh_keys

[![Build Status](https://github.com/glillico/ansible-role-setup_ssh_keys/workflows/build/badge.svg)](https://github.com/glillico/ansible-role-setup_ssh_keys)

This role will add or remove a defined SSH authorized key for a user.

## Requirements

None

## Role Variables

### defaults/main.yml

|Variable|Description|
|---|:---|
|ssk_user|The username of the account, this is required.|
|ssk_state|Defines what do to with the account.|
|ssk_keyfile|Defines the ssh public keys file to use.|

#### Examples

##### Deploys the ssh public key testuser.pub to the users authorized_keys file.

```
  - ssk_user: testuser
    ssk_state: present
    ssk_keyfile: 'files/testuser.pub'
```

## Dependencies

None

## Example Playbook

    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
        - glillico.setup_ssh_keys

## License

MIT

## Author Information

This role was created in 2020 by Graham Lillico.
