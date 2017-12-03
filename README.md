<img src="https://assets.morpheusdata.com/SpudMedia/1275/attachment/Ansible_original.svg" width="200">

- The Ansible (CM Tool) is the second layer of environment deployment process.
- It can be executed in many ways, the one we use is ansible-pull architecture, in which every host is responsible for its own configuration, by cloning this repository and applying the appropriate playbook on itself.
- [Ansible pull command], is executed by the Terraform init scripts (aka user data), created by [Terraform deploy module]

---
### Create New Role
When creating a new role, few guidelines should be followed:

- You may copy the structure of the newly created role from an existing one or use [ansible-galaxy] init command (optional).
- Export to the external variable source file (terraform_vars.yml) as few parameters as possible
- Export to your role defaults/main.yml file as many parameters as possible.
- Most important - your role has to be idempotent, which means that a second run cannot create new changes and/or repeat tasks execution if it is not needed.

[Ansible pull command]:https://github.com/GefenOnline/terraform
[Terraform deploy module]:https://github.com/GefenOnline/terraform/blob/master/modules/deploy
[ansible-galaxy]:http://docs.ansible.com/ansible/galaxy.html

