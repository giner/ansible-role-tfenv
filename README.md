# Ansible Role: tfenv

Installs tfenv and Terraform into a user's home or a custom directory

## Requirements

* Ubuntu

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

User to install tfenv.

    tfenv_user: "{{ ansible_user_id }}"

Directory to install tfenv.

    tfenv_dir: "{{ tfenv_user }}/.tfenv"

Directory to create links to tfenv and terraform binaries.

    tfenv_dir: "{{ tfenv_user }}/bin"

## Dependencies

None.

## Example Playbook

    - hosts: terraform
      roles:
      - giner.tfenv

## Development

Running all tests (requires ansible, docker, molecule and molecule-docker to be installed).

    molecule test --all

## License

Apache 2.0

## Authors

This role was created in 2021 by [Stanislav German-Evtushenko](https://github.com/giner)
