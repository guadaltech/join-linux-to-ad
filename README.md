# join-linux-to-ad
Join machine with Linux OS to Active Directory of Microsoft

For to deploy of recipe from ansible, we have that changes the environment for that are defined in the configuration in the moment of deploy, this enviroment have is defined in the next directories:

- ./inventory/group_vars/all/all.yaml
- ./roles/all/vars/main.yaml

When already we have defined all the parameters, we have to execute the next command that it will change of network configuration for the correct join of node linux with the domain of Active Directory:
ansible-playbook -i inventory/inventory.ini --become --become-user=root site.yaml -vvv --limit all 

By last, We deploy the next command for start the process of join of operative system linux with the node of Active Directory:
ansible-playbook -i inventory/inventory.ini --become --become-user=root ansible.yaml -vvv --limit all 
