# Ansible Role: SnappyFlow APM agent 

Installs SnappyFlow APM agent for RedHat/CentOS and Debian/Ubuntu linux servers.

## Role Variables

Generate key from snappyflow APM and add in /opt/sfagent/config.yml.

## Dependencies

None.

## Example Playbook 

    - hosts: server
      roles:
        - role: ansible-role-apm-agent

## License

Copyright 2019-20, MapleLabs, All Rights Reserved.

## Author Information

https://www.snappyflow.io/
