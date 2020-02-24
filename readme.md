Ansible User Role
=================

User creation role.

## Role Variables

- `user_name`: The name of the user
- `user_groups`: The groups of the user
- `user_authorized_keys`: The authorized keys of the user

## Example Playbook

    - hosts: all
      roles:
        - role: ansible-user
          vars:
            user_name: alex
            user_groups:
              - docker
            user_authorized_keys:
              - {{ lookup('file', 'path-to-key') }}
