SomOffice role
=========

A role to deploy [SomOffice](https://git.coopdevs.org/coopdevs/comunitats-energetiques/somoffice/).

This role will:
- Ensure you have all the dependencies installed in your machine.
- Download the repository to a temp local directory.
- Install the app's dependencies.
- Render the `.env` file.
- Build the app.
- Ensure you have all the dependencies installed in the development environment.
- Deploy the app to the development environment.
- Backup any existing deployments.
- Create a symbolic link from `$base_path/current` to uploaded version.
- Delete local temporary files.

Requirements
------------
Hard dependencies are declared in `somoffice_role_hard_deps` var (see `vars/main.yml`).
They are checked by main task prior to role execution.

Role Variables
--------------
```yaml
somoffice_role_backoffice_version: "main"
somoffice_role_backoffice_repo:  "https://git.coopdevs.org/coopdevs/comunitats-energetiques/somoffice/back-office"
somoffice_role_local_path: "./build/backoffice"
somoffice_remote_base_path: "/opt/somoffice"

# .env file variables
somoffice_role_env_host: "https://example.coop"
somoffice_role_env_keycloak: "https://example.coop/auth"
somoffice_role_env_kc_realm: "somoffice"
somoffice_role_env_kc_client: "client id"
```
Example Playbook
----------------

You can test this role creating a local development environment with `devenv` command. This will call [`devenv`](https://github.com/coopdevs/devenv) with the [`.devenv`](.devenv) file as configuration. `devenv` will create a LXC virtual environment.

```bash
devenv
```

Then, you can run the playbook & inventory residing in the `tests` directory:

```bash
ansible-playbook tests/test.yml --extra-vars="@defaults/main.yml"  --extra-vars="@vars/main.yml" -i tests/inventory
```

License
-------

GPLv3

Author Information
------------------

[Coopdevs](https://coopdevs.org)
