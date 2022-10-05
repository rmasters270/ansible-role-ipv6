# IPv6

Enable or disable IPv6 in the GRUB boot loader. This will disable IPv6 system wide but changes require a reboot to be effective.

[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-ipv6-blue.svg)](https://galaxy.ansible.com/rmasters270/ipv6)

## Role Variables

| Variable                | Required | Default | Choices      | Comments                                                |
|-------------------------|----------|---------|--------------|---------------------------------------------------------|
| ipv6_enabled            | yes      | true    | true, false  | Enable or disable IPv6.                                 |
| grub_change_reboot      | yes      | true    | true, false  | Reboot immediately when grub is updated. If set to `false` IPv6 will remain unchanged until the next reboot. |

## Example Playbook

Disable IPv6 on all servers.

```yaml
- hosts: servers
  become: true

  vars:
    ipv6_enabled: false

  roles:
    - rmasters270.ipv6
```

## License

MIT

## Author Information

Ryan Masters
