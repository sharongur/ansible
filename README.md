<img src="https://assets.morpheusdata.com/SpudMedia/1275/attachment/Ansible_original.svg" width="200">

- The Ansible (CM Tool) can be executed in many ways, the one we use is remote management host architecture, in which one main management host is responsible for the configuration of all other hosts, by remotely applying the ansible roles on the appropriate hosts.

---
### Create New Role
When creating a new role, few guidelines should be followed:

- You may copy the structure of the newly created role from an existing one or use [ansible-galaxy] init command (optional).
- Export to your role defaults/main.yml file as many parameters as possible.
- Most important - your role has to be idempotent, which means that a second run cannot create new changes and/or repeat tasks execution if it is not needed.

[ansible-galaxy]:http://docs.ansible.com/ansible/galaxy.html
