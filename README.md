# IPv6

Enable or disable IPv6 in the GRUB boot loader. This will disable IPv6 system wide but changes require a reboot to be effective.

## Role Variables

### ipv6_enabled

Enable or disable IPv6.

default: `true`

### grub_change_reboot

Reboot the target machine immediately when grub is updated.  If set to `false`  IPv6 will remain unchanged until the next reboot.

default: `true`

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
