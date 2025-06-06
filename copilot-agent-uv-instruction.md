---
applyTo: "**"
---
# Project Setup Instructions (using uv)

## Project Initialization
When asked to initialize a new  project using `uv`, follow these steps:
1. Use `uv init` to initialize a new Python project with `uv`
    - This sets up a virtual environment, `pyproject.toml`, and source layout
    - Example:
    ```bash
    uv init
    ```
2. After Initialization RUN `uv run main.py`.
    - Now you should have the following structure:
    .
    ├── .python-version
    ├── README.md
    ├── main.py
    ├── pyproject.toml
    └── venv


## When asked to install Dependencies
When asked to install dependencies, you can use `uv add` to add them to your project.
1. Use `uv add` to install dependencies.
    - Example:
    ```bash
    uv add [packages_name]
    ```
    - When installing multiple dependencies, you can use:
    ```bash
    uv add [package1] [package2] ...
    ```

## When asked to run a file using `uv`
When asked to run a file using `uv`, you can use the `uv run` command.
1. Use `uv run` to run a specific file.
    - Example:
    ```bash
    uv run main.py
    ```
