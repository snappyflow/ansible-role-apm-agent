##Ansible script to Install/Upgrade sfagent

ansible.cfg - Ansible configuration file.

hosts - Ansible Inventory File

env_variables - Main environment variable file where we have to specify based on our environment.

ansible-sfagent.yml - Ansible Playbook helps to Install/Upgrade sfagent.

playbooks - Its a directory holds all playbooks.

Requirement:

        1. install ansible

    2. copy node ssh key to local machine and change permission with chmod 400  <ssh key>

        3. Update nodes details to install/Upgrade sfagent in host file.

Execution:

	Install:

        	ansible-playbook ansible-sfagent.yml --tags "install" --key-file=<path to ssh key file>  -b -v

        Example
                ansible-playbook ansible-sfagent.yml --tags "install" --key-file=/home/centos/user-qa-aws-ssh.pem -b -v

	Upgrade:

        	ansible-playbook ansible-sfagent.yml --tags "upgrade" --key-file=<path to ssh key file>  -b -v

        Example
                ansible-playbook ansible-sfagent.yml --tags "upgrade" --key-file=/home/centos/user-qa-aws-ssh.pem -b -v

