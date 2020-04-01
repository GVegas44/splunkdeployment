Playbook to setup connectivity between Ansible host or Master laptop and nodes

Edit Inventory file to reflect your environment

Prerequisites 
Run as root
1.	ssh-keygen
2.	/root/.ssh/ansible.id_rsa
3.	Enter
4.	Enter

Running the playbook
1.	ansible-playbook site.yml --extra-vars 'ansible_user=root' -k
2.	ssh password

Splunk Playbook Working:
TODO
Install License
Add Apps
Add Dashboards
Enable Receiving
Create Index
SSL Encryption
SSL Forwarder Encrytion

Splunk Removal Playbook Working
