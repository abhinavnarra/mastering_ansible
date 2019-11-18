## Mastering Ansible

# Installing ansible on ubuntu

 sudo apt-get install ansible
 ansible --version
 ansible-galaxy --version

# Check the list of hosts

 ansible --list-hosts all or ansible --list-hosts "*"
 ansible --list-hosts <host_name>:<host_name2> (you can use comma too)
 ansible --list-hosts \!<host_name> (except the specified host)
 sudo vi /etc/ansible/hosts

# Custom inventory host listing
 ansible --list-hosts -i <inventory_file_name> all

# Ping Hosts
    ansible -m ping all
    ansible -m command -a "hostname" all

# execute playbooks
    ansible-playbook <path_to_playbook/playbook_name.yml>

# lineinfile
 In order to keep everything of any configuration file as it is, but you want to change only one line then you can use linwinfile

 # waitfor
 waitfor is used to check whether a service is listening on a port or not

 # Roles
 ansible-galaxy init control(to create skeleton structure for the role)

 # Setup
 ansible -m setup <host-name>(it will give the detailed info about the hosts)

 #D efaults
 to setup default values in db configurations or any. these file will be within the role directory


