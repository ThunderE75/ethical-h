# UV for Python 

Docs: https://docs.astral.sh/uv/getting-started/installation/

```sh
curl -LsSf https://astral.sh/uv/install.sh | sh
```

## Python versions

Installing and managing Python itself.

- `uv python install`: Install Python versions.
- `uv python list`: View available Python versions.
- `uv python find`: Find an installed Python version.
- `uv python pin`: Pin the current project to use a specific Python version.
- `uv python uninstall`: Uninstall a Python version.


- `uv run`: Run a script.

- uv pip install: Install packages into the current environment.
- uv pip uninstall: Uninstall packages.


## venv 

docs: https://docs.astral.sh/uv/pip/environments/

```sh
uv venv # uv venv <env-name>
source .venv/bin/activate
uv pip install -r requirements.txt
```