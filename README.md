# Ansible Amazon AWS EC2 Provision:
Tutorial to integrate Ansible provisioning with Amazon EC2 platform.

# Install:
- Clone the repository inside /etc/ansible. Warning: it will replace your 
ansible files;
- Create the ssh key (~/.ssh/) and import it to EC2. Note the ssh key name;
- Change the file /etc/ansible/ec2_creation/vars/all.yml with the information 
about your EC2 environment;
- Inside /etc/ansible/ec2_creation Run the command: ansible-playbook -i 
hosts playbook.yml --private-key=ssh key file name - ~/.ssh/id_ansible -vvvv

# More information:
Look this video for more information.


