# Ansible Role: SnappyFlow APM agent 

Install/Upgrade SnappyFlow APM agent for RedHat/CentOS and Debian/Ubuntu linux servers.

## Dependencies

None.

## Example Playbook 

    - hosts: server
      roles:
        - role: ansible-role-apm-agent

Execution:

        Install:

                ansible-playbook <Playbook> --tags "install" --key-file=<path to ssh key file>  -b -v

        Example
                ansible-playbook ansible-sfagent.yml --tags "install" --key-file=/home/centos/user-qa-aws-ssh.pem -b -v

        Upgrade:

                ansible-playbook <Playbook> --tags "upgrade" --key-file=<path to ssh key file>  -b -v

        Example
                ansible-playbook ansible-sfagent.yml --tags "upgrade" --key-file=/home/centos/user-qa-aws-ssh.pem -b -v

## License

Copyright 2019-20, MapleLabs, All Rights Reserved.

## Author Information

https://www.snappyflow.io/
