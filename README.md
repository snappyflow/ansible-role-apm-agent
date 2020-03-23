# Ansible Role: SnappyFlow APM agent 

Installs SnappyFlow APM agent for RedHat/CentOS and Debian/Ubuntu linux servers.

## Role Variables

Available variables are listed below, along with default values:

    agent:
      Name: petclinic_aio
      appName: petclinic
      projectName: demo_app
      es_host: 127.0.0.1
      metrics_index: demo_app-naetr9c5jb-metric_write
      heartbeat_index: demo_app-naetr9c5jb-heartbeat_write
      logger_index: demo_app-naetr9c5jb-logger_write

Some other options available in role's 'defaults' folder.

## Dependencies

None.

## Example Playbook 

    - hosts: server
      roles:
        - role: ansible-role-sf-agent
          agent:
            Name: petclinic_aio
            appName: petclinic
            projectName: demo_app
            es_host: 127.0.0.1
            metrics_index: demo_app-naetr9c5jb-metric_write
            heartbeat_index: demo_app-naetr9c5jb-heartbeat_write
            logger_index: demo_app-naetr9c5jb-logger_write

## License

Copyright 2019-20, MapleLabs, All Rights Reserved.

## Author Information

https://www.snappyflow.io/
