# Ansible Amazon AWS EC2 Provision:
Tutorial to integrate Ansible provisioning with Amazon EC2 platform, using an Ubuntu 14.04 LTS Desktop and creating an Ubuntu 14.04 LTS Server.

# Install:
- Install Ansible last version:
  sudo apt-get update
  sudo apt-get install software-properties-common
  sudo apt-add-repository ppa:ansible/ansible
  sudo apt-get update
  sudo apt-get install ansible

- Install boto (python lib):
  sudo apt-get install python-pip
	pip install -U boto

- Clone the repository inside /etc/ansible. Warning: it will replace your ansible files;

- Create the ssh key (~/.ssh/) and import it to EC2. Note the ssh key name (e.g. ssh-keygen -t rsa -f ~/.ssh/id_ansible, if you use a different name, change it inside /etc/ansible/hosts);

- Change the file /etc/ansible/ec2_creation/vars/all.yml with the information 
about your EC2 environment (there's a example in /etc/ansible/vars/example.txt);

- Export your Amazon credential to to environment variables;
  export AWS_ACCESS_KEY_ID=YOURKEYID
  export AWS_SECRET_ACCESS_KEY=YOUSECRETKEY

- Inside /etc/ansible/ec2_creation Run the command: ansible-playbook -i 
hosts playbook.yml --private-key=[your ssh key file] -vvvv

# More information:
Look this video for more information (PT-BR) or open an issue.


