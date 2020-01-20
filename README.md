# AnsibleRoleForNewUser
An Ansible Role for creating a new user on Linux distributions
## Overview
This is an Ansible role for automating the process of creating a Linux User on any Linux distributions (like Ubuntu, Fedora, openSUSE etc.)
## Requirements
 - You need to have a user on the remote server configured with passwordless sudo.
- The remote server should also have ssh configured based on Ansible's requirements
## How to Use
-   Begin by first cloning the repository with the command:  `git clone https://github.com/vishalbala-nps/AnsibleRoleForNewUser`
-   Change the IP Address of the remote server in the inventory file and change the remote server username in the test.yml file
- You can change more properties related to the user like the User's real name, Home Directory and Default Shell in `add_user/vars/main.yml`
-   Run the role by typing the command  `ansible-playbook -i inventory test.yml`
-   When running the role, it will ask you to enter the Username and Password for the user which is going to be created
