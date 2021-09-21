##Ansible script to Install/Upgrade/Uninstall/Configure sfagent using ansible

ansible.cfg - Ansible configuration file.

hosts - Ansible Inventory File

config-params.yml - file to pass values to config.yaml 

ansible-sfagent.yml - Ansible Playbook helps to Install/Upgrade sfagent.

Requirement:

        1. install ansible.
    
        2. copy node ssh key to local machine, change permission with chmod 400 <ssh key>.
    
        3. copy the profile key from snappyflow and paste it in the config-params.yml file.
    
        4. Update nodes details in hosts file .


Execution:

	Install:
	    	ansible-playbook ansible-sfagent.yml --tags "install" 
	    
	Install with Environment variables:
	       	ansible-playbook ansible-sfagent.yml --tags "install" -e "env_vars=<something> include_paths=<something>"
	
	Upgrade:
	    	ansible-playbook ansible-sfagent.yml --tags "upgrade"
	
	Upgrade with Environment variables:
	        ansible-playbook ansible-sfagent.yml --tags "upgrade" -e "env_vars=<something> include_paths=<something>"
	
	Uninstall:
	        ansible-playbook ansible-sfagent.yml --tags "uninstall"
	
	Help:
		ansible-playbook ansible-sfagent.yml --tags "help"
	
	Update-config file:
	        ansible-playbook ansible-sfagent.yml --tags "update-config"
	
	Generate config file:
	        ansible-playbook ansible-sfagent.yml --tags "generate-config"
	
	NOTE:
	        1. -e or --extra-vars is optional and is required if you pass extra variables from the command-line.
	        2. --key-file can be optional as keyfile can be passed in hosts file.