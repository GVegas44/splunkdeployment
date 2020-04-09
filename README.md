Playbook to setup connectivity between Ansible host or Master laptop deploy splunk

Edit Inventory file to reflect your environment

Prerequisites 
Run as root
1.	ssh-keygen
2.	/root/.ssh/ansible.id_rsa
3.	Enter
4.	Enter

Modify the following Variables:

playbooks/user_provision.yml:
hosts: "reflect your inventory file'
ansible_user: "to your target box"
ansible_ssh_pass: {{ ansible.password }} 

group_vars/all.yml
host:
    work_dir: "to your working directory"
ansible:
    user: "make a user"
    usergroup: "make a usergroup"
    sudoer: "same as user"
    password: "This is used for ansible_ssh_pass in playbook/user_provision"
    
splunk:
    password: "your splunk admin password"
    secert:
    pass4SymmKey:
    license: "put your license in roles/license_master/files/"
    pkg: "change to match your splunk rpm package out file in roles/splunk_common/files/
    web_ssl_cert: "your .pem put it in roles/splunk_common/files/
    web_ssl_privKey: your .key put it in roles/splunk_common/files
    web_ssl_privKey_password: " password used to create certs"
    apps: desired apps for splunk put in /roles/standalone/files/

/roles/standalone/vars/main.yml
config_users:
  password: "default password for splunk users"
  users: "list of users to add to splunk webUI"
  
Splunk Playbook Working:
TODO

SSL Forwarder Encrytion
Create Bro Index

