# Ansible Role: Go

[![CI](https://github.com/mdelapenya/ansible-role-go/workflows/CI/badge.svg?event=push)](https://github.com/mdelapenya/ansible-role-go/actions?query=workflow%3ACI)

An Ansible Role that installs Go (the language) on Linux.

## Requirements

N/A

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    go_version: "1.17"
    go_platform: linux
    go_arch: amd64
    go_ext: tar.gz

Version, platform, architecture and file extension to use when downloading Go.

    go_tarball: go{{ go_version }}.{{ go_platform }}-{{ go_arch }}.{{ go_ext }}
    go_download_url: https://dl.google.com/go/{{ go_tarball }}

## Dependencies

None.

## Example Playbook

    - hosts: myserver
      roles:
        - { role: mdelapenya.go }

## License

MIT / BSD

## Author Information

This role was created in 2022 as inspiration of [Jeff Geerling's](https://github.com/geerlingguy/ansible-role-go).
