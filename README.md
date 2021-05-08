# LogDNA Agent Ansible Role

This role installs and configures the LogDNA collector agent on RHEL/CentOS and Fedora platforms.

## Requirements

* Ansible 2.7+

## Role Variables

``` yaml
# LogDNA ingestion key
logdna_key: ""

# List of log directories to scan (supports globs)
logdna_logdirs: [ "/var/log" ]

# List of log files to scan
logdna_logfiles: []

# List of log files to exclude
logdna_excludes: []

# List of regexes used to filter log lines
logdna_excludes_regex: []

# Alternative hostname to report
logdna_hostname: ""

# List of host tags
logdna_tags: []

# Start the service?
logdna_start_service: yes
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
