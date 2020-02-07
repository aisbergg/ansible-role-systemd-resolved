# Ansible Role: `aisbergg.systemd-resolved`

Configures [systemd-resolved](https://www.freedesktop.org/software/systemd/man/systemd-resolved.service.html#) as a network name resolution manager on Linux systems.

## Requirements

Systemd needs to be installed on the system.

## Role Variables

| Variable | Default | Comments |
|----------|---------|----------|
| `systemd_resolved_service_enabled` | `yes` | Enables the `resolved` service. |
| `systemd_resolved_service_state` | `started` | The state of the serice to be in. |
| `systemd_resolved_config` | `{}` | The configuration for `resolved`. The full documentation of the parameters can be found [here](https://www.freedesktop.org/software/systemd/man/resolved.conf.html). |
| `systemd_resolved_config.dns` | `[]` | List of  IPv4 and IPv6 addresses to use as system DNS servers. |
| `systemd_resolved_config.fallback_dns` | `[]` | List of IPv4 and IPv6 addresses to use as the fallback DNS servers. |
| `systemd_resolved_config.domains` | `[]` | List of domains to use as search suffixes when resolving single-label host names. |
| `systemd_resolved_config.llmnr` | `yes` | Controls Link-Local Multicast Name Resolution support on the local host. |
| `systemd_resolved_config.multicast_dns` | `no` | Controls Multicast DNS support on the local host. |
| `systemd_resolved_config.dnssec` | `no` | Enables DNSSEC-validation for DNS lookups. |
| `systemd_resolved_config.dns_over_tls` | `no` | Enables encryption for DNS lookups. |
| `systemd_resolved_config.cache` | `yes` | Use cache for DNS lookups. |
| `systemd_resolved_config.dns_stub_listener` | `yes` | Enable DNS stub resolver to listen on 127.0.0.53 port 53. |
| `systemd_resolved_config.read_etc_hosts` | `yes` | Read /etc/hosts and to resolve hosts. |

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  vars: 
    systemd_resolved_config:
      dns: []
      domains:
        - example.org
  roles:
    - role: aisbergg.systemd-resolved
```

## License

MIT

## Author Information

Andre Lehmann (aisberg@posteo.de)
