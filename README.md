# Using this template

This template is a starting point for creating a new repository for Ansible roles.  You must complete the following steps:

- [ ] Click on button `Use this template` to create a new repository.
- [ ] Clone it to your computer and follow [CONTRIBUTING.md](CONTRIBUTING.md) instructions to setup the developing enviroment.
- [ ] Update the `README.md` file to describe the role.
- [ ] Update the `meta/main.yml` with proper metadata about the role.
- [ ] Update the `defaults/main.yml` file to set the default values for the role.
- [ ] Update the `tasks/main.yml` file to implement the role.
- [ ] Update the `vars/main.yml` file to set the variables for the role.
- [ ] Add template files to the `templates` directory
- [ ] Add needed files to the `files` directory
- [ ] If needed, define handlers in the `handlers/main.yml` file
- [ ] Delete all unused files

## Contents

This template contains the following items:

- An Ansible role skeleton generated by `ansible-galaxy init`.
- Pre-filled `CONTRIBUTING.md` with instructions to set-up the development environment.
- Pre-commit configuration to check the code before commiting.
- `requirements.txt` file to include test dependencies.
- Github actions to check the role with `ansible-lint` and `yamllint`.
- Dependabot configuration to keep the dependencies up-to-date.
- A [LICENSE](LICENSE) file.

---

Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```bash
ansible-playbook tests/test.yml -i tests/inventory --extra-vars '{"var":"value"}'
```

License
-------

GPLv3

Author Information
------------------

[Coopdevs](https://coopdevs.org)