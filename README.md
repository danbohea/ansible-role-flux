# Ansible role: f.lux

[![Build Status](https://travis-ci.org/danbohea/ansible-role-flux.svg?branch=master)](https://travis-ci.org/danbohea/ansible-role-flux)

Installs & configures f.lux on macOS.


## Requirements

- macOS 10.11 or 10.12


## Role Variables

All role default variables are listed below along with their respective default values.

```yaml
flux_locationTextField: "ta126bu"
```

Your postal code. f.lux will use this to determine your Latitude & longitude.

```yaml
flux_location: "50.976297,-2.838684"
```

Latitude & longitude. f.lux normally determines this for you but if you have the value from a previous installation enter it here.

```yaml
flux_lateColorTemp: 3500
```

Color temperature for "Sunset".

```yaml
flux_nightColorTemp: "{{ flux_lateColorTemp }}"
```

Color temperature for "Bedtime".


## Dependencies

- [danbohea.homebrew](https://galaxy.ansible.com/danbohea/homebrew)


## Example Playbook

```yaml
- hosts: macbook
  connection: local

  roles:
    - role: ansible-role-flux
```

## License

MIT


## Author Information

This role was created by [Dan Bohea](http://bohea.co.uk) primarily for use with [Macsible](https://github.com/macsible/macsible).
