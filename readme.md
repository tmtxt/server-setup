# Personal setup for VPS server

## Preparation

- Create the VPS
- Create the user (with password and SSH key)
- Create SSH key (no passphrase) and add it to the services like Github

## Configuration

- add hosts in **hosts** file
- config remote user for the host in **host_vars/hostname**

## Deploy

```
ansible-playbook -i hosts main.yml -K
```

# Personal setup for Ubuntu PC

## Preparation

- Create SSH key for the current account, add to Github
- Install git and ansible

```
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
$ sudo apt-get install git-core
```

- Clone the project

Run the corresponding playbook for localhost

```
$ ansible-playbook xubuntu.yml -K
```

Or specify a user instead of tmtxt

```
$ ansible-playbook xubuntu.yml -K --extra-vars "remote_user=some_user"
```
