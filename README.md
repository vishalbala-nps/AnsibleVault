# AnsibleVault
A small demo/use of Ansible Vault in User creation
## Overview
This is an Ansible role for automating the process of creating a Linux User on any Fedora Linux where the values of username, password, user's real name, default shell are encrypted using Ansible Vault
## Requirements
 - You need to have a user on the remote server configured with passwordless sudo.
 - The remote server should also have ssh configured based on Ansible's requirements
## How to Use
 -   Begin by first cloning the repository with the command:  `git clone https://github.com/vishalbala-nps/AnsibleVault`
 -   Change the IP Address of the remote server in the inventory file and change the remote server username in the test.yml file
 -   To Edit the Details of the user (which you plan to create). Run the command: `ansible-vault edit add_user/vars/main.yml`. It will ask the Vault's password (which is `test`). It will open the file in your default editor (If you want to change the editor set the environment variable EDITOR)
 -   Run the role by typing the command  `ansible-playbook -i inventory test.yml --ask-vault-pass`
 -   When running the role, it will ask you to enter the Vault's password which  is `test`.
## Uses of Ansible Vault
 - It can be used to encrypt sensitive data like a user's password and other details in this case
 - It can be used to encrypt SSH and GPG Public and private keys when copying them to another machine
 - It can be used to encrypt database username password and such sensitive data
