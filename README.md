# LogDNA Agent Ansible Role

This role installs and configures the LogDNA collector agent on RHEL/CentOS and Fedora platforms.

## Requirements

* Ansible 2.7+

## Role Variables

``` yaml
logdna_key: ""
```

## Dependencies

None.

## Example Playbook

``` yaml
- hosts: localhost
  tasks:
    - name: Install LogDNA Collector
      import_role:
        name: rchouinard.logdna_agent
      vars:
        logdna_key: "00112233445566778899AABBCCDDEEFF"
```

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
