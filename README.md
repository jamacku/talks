# Talks

- [2023-12-11 - Custom GitHub Actions 101](custom-github-actions-101/main.md)

## Installation

```sh
sudo dnf install python3.6
python3.6 -m venv env
source env/bin/activate
pip install --upgrade pip
python -m pip install lookatme
```

## Usage

Activate virtual environment and run `lookatme` with path to markdown file.

```sh
source env/bin/activate
lookatme $PATH_TO_MARKDOWN_FILE
```

Navigate by `←` and `→`. Press `q` to quit. Deactivate virtual environment with `deactivate` command.
