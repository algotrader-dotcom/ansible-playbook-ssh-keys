# ansible-playbook-ssh-keys
Ansible playbook create user &amp; ssh key to remote servers

# How it works
Ansible playbook help to create user ansible & add ssh key to remote servers

# Step by step

## Create SSH keypair
mkdir -p files

ssh-keygen -t rsa -f ./files/authorized_keys.ansible

## Run playbook on target servers
ansible-playbook -i hosts/web ssh-keys-playbook.yml -v
