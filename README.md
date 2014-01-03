# ansible-td-agent

This ansible role installs the td-agent, the distribution of [fluentd](http://fluentd.org/).

This role is written based on [the official installation page](http://docs.fluentd.org/categories/installation)

## Requirements

This role requires Ansible 1.4 higher and platforms listed in the metadata file.

## Role Variables

The variables that can be passed to this role **when the OS is Debian** and a brief description about them are as follows

```
# The version of td-agent (optional)
td_agent_version: 1.1.18-1

# Architecture of the machine (required, i386 or amd64)
td_agent_architecture: amd64
```

Detail for [the official intallation page](http://docs.fluentd.org/articles/install-by-deb)

## Examples

1) Ubuntu or EL
```
---
- hosts: all
  roles:
    - td-agent
```

2) Debian (define only architecture)
```
---
- hosts: all
  roles:
    - role: td-agent
      td_agent_architecture: i386
```

3) Debian (define architecture and td_agent_version)
```
---
- hosts: all
  roles:
    - role: td-agent
      td_agent_architecture: amd64
      td_agent_version: 1.1.17-1
```

## Dependencies

None

## Licence

BSD

## Contribution

Fork and make pull request!

[kawasakitoshiya / ansible-td-agen](https://github.com/kawasakitoshiya/ansible-td-agent)

## Author Information

Toshiya Kawasaki
