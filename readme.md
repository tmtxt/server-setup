# Personal setup for VPS server

# Preparation

- Create the VPS
- Create the user (with password and SSH key)
- Create SSH key (no passphrase) and add it to the services like Github

# Configuration

- add hosts in **hosts** file
- config remote user for the host in **host_vars/hostname**

# Deploy

```
ansible-playbook -i hosts main.yml -K
```
