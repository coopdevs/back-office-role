# Development setup

### Configure python environment

In order to assure that the files contained here are linted the same way, we are using [`pyenv`](https://github.com/pyenv/pyenv).

Follow [Installing and using pyenv](https://github.com/coopdevs/handbook/wiki/Installing-and-using-pyenv), or, in short:

```sh
pyenv install 3.8.12
pyenv virtualenv 3.8.12 back_office_role
pyenv activate back_office_role
pip install -r requirements.txt
```

### Configure development environment
You can edit the `.devenv` file if you want to override the default configuration.
```ini
URL=somoffice-role.local
USR=root
DIST=focal
```
The root user in devenv will have your ssh public key.

### Install pre-commit hooks

We use [pre-commit framework](https://pre-commit.com/) to assure quality code.

```sh
pre-commit install
```
