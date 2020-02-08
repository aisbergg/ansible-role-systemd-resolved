# Ansible Role: `aisbergg.systemd-resolved`

Configures [systemd-resolved](https://www.freedesktop.org/software/systemd/man/systemd-resolved.service.html#) as a network name resolution manager on Linux systems.

## Requirements

Systemd needs to be installed on the system.

## Role Variables

| Variable | Default | Comments |
|----------|---------|----------|
| `systemd_resolved_service_enabled` | `yes` | Enables the `resolved` service. |
| `systemd_resolved_service_state` | `started` | The state of the serice to be in. |
| `systemd_resolved_config` | `{}` | The configuration for `resolved`. Full documentation of all parameters can be found in [resolved.conf(5)](https://www.freedesktop.org/software/systemd/man/resolved.conf.html). |
| `systemd_resolved_config.DNS` | `[]` | List of  IPv4 and IPv6 addresses to use as system DNS servers. |
| `systemd_resolved_config.FallbackDNS` | `[]` | List of IPv4 and IPv6 addresses to use as the fallback DNS servers. |
| `systemd_resolved_config.Domains` | `[]` | List of domains to use as search suffixes when resolving single-label host names. |
| `systemd_resolved_config.LLMNR` | `yes` | Controls Link-Local Multicast Name Resolution support on the local host. |
| `systemd_resolved_config.MulticastDNS` | `no` | Controls Multicast DNS support on the local host. |
| `systemd_resolved_config.DNSSEC` | `no` | Enables DNSSEC-validation for DNS lookups. |
| `systemd_resolved_config.DNSOverTLS` | `no` | Enables encryption for DNS lookups. |
| `systemd_resolved_config.Cache` | `yes` | Use cache for DNS lookups. |
| `systemd_resolved_config.DNSStubListener` | `yes` | Enable DNS stub resolver to listen on 127.0.0.53 port 53. |
| `systemd_resolved_config.ReadEtcHosts` | `yes` | Read /etc/hosts and to resolve hosts. |

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  vars: 
    systemd_resolved_config:
      DNS: []
      Domains:
        - example.org
  roles:
    - role: aisbergg.systemd-resolved
```

## License

MIT

## Author Information

Andre Lehmann (aisberg@posteo.de)
