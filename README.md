# Ansible role: user
+ **Generate** random password for regular user
+ Store password in **hostvars**
+ Create **regular** user and set password
+ Add **ssh** pubkeys for login to regular user

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `user_name` (default: `{{ ansible_user }}`): username of regular user
+ `pw_dir` (default: `{{ inventory_dir }}/host_vars`):
  plaintext passwords will be stored in subdirectories under this path,
  `{{ inventory_hostname }}/pw.yml`, in a key named `user_pw`
+ `user_ssh_pubkeys` (default: empty): newline-delimited string of keys
   to place in user's authorized_keys

## Playbooks
+ `main.yml`: apply role

## Dependencies
None

## License
MIT

## Author Information
Sean Ho, https://github.com/ho-ansible/
