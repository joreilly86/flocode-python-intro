# Virtual Environments Cheat Sheet

Virtual Environments with uv: A Beginner's Guide

> Brand new to virtual environments? Start here. This page explains what they are, why they matter for engineering work, and how to use [Astral's uv](https://docs.astral.sh/uv/) to set up fast, reliable project environments without getting into Git or advanced packaging topics.

---

### What is a virtual environment?

A virtual environment is a private workspace for a single project’s Python and packages. Instead of installing libraries system‑wide, you install them into this project’s environment. That keeps each project’s dependencies separate so they don’t conflict with each other.

### Why engineers should always isolate projects

- **Consistency across machines**
    
    Your code runs with the same Python and library versions on any laptop, desktop, or server.
    
- **Reproducibility**
    
    Teammates can recreate the exact environment and get the same results.
    
- **Safety while iterating**
    
    Updating one project’s packages won’t break another project.
    
- **Clean upgrades**
    
    You can test new versions in isolation, then roll forward confidently.
    

---

### Why use [uv](https://docs.astral.sh/uv/)?

uv is an extremely fast, all‑in‑one tool for Python projects. It can:

- Create and manage virtual environments for each project
- Install and lock dependencies quickly
- Manage which Python version a project uses
- Run commands inside the project’s environment

In short: one tool, predictable results, and great speed. Perfect for beginners and production work alike.

---

### Quick start: set up a new project with uv

[https://youtu.be/kUAJ1WoGsFk](https://youtu.be/kUAJ1WoGsFk)

Follow these steps the first time you create a project.

1) Install uv

- Windows (PowerShell):
    
    ```powershell
    powershell -ExecutionPolicy ByPass -c "irm [https://astral.sh/uv/install.ps1](https://astral.sh/uv/install.ps1) | iex"
    ```
    
- macOS/Linux (Terminal):

    ```bash
    curl -LsSf https://astral.sh/uv/install.sh | sh
    ```
    

2) Make a project folder

```bash
mkdir my_project
cd my_project
```

3) Initialize the project (creates pyproject.toml and lockfile)

```bash
uv init
```

4) Pick a Python version for this project (installs it if missing)

```bash
uv python 3.12
```

5) Add your first dependencies (examples)

```bash
uv add numpy pandas ipykernel
```

- Tip for notebooks: install `ipykernel` so Jupyter/VS Code can select this environment’s kernel.

6) Activate the environment

```bash
uv activate
```

You’ll see the environment name in your terminal. Commands you run now use this project’s Python and packages.

7) Sync on any machine (to recreate the env from the lockfile)

```bash
uv sync
```

This installs the exact versions recorded for the project—great for teammates or rebuilding on a new computer.

---

### Using uv day‑to‑day

- Run a Python script inside the env

    ```bash
    uv run python main.py
    ```
    
- Add or upgrade a package later
    
    ```bash
    uv add requests
    ```
    
- Remove a package
    
    ```bash
    uv remove requests
    ```
    
- List installed packages
    
    ```bash
    uv pip list
    ```
    
- Deactivate the environment
    
    ```bash
    exit
    ```
    

---

### Choosing and managing Python versions

Each project can declare its own Python version, and uv will install and use it for you.

- Set or change the version for this project
    
    ```bash
    uv python 3.13
    ```
    
- Install a version globally so it’s available
    
    ```bash
    uv python install 3.13
    ```
    

This avoids “works on my machine” problems and ensures compatibility on different operating systems and CPUs.

---

### Working in VS Code (optional, recommended)

- Open your project folder in VS Code.
- Press Ctrl+Shift+P and choose "Python: Select Interpreter".
- Pick the interpreter that matches your project's uv environment.
- For notebooks, select the kernel that matches your project (created by installing `ipykernel`).

---

### Troubleshooting tips

- “Command not found: uv”
    
    Re‑run the installer above and then restart your terminal so PATH updates apply.
    
- "VS Code doesn't see my environment"

    Close and reopen the terminal in VS Code, then use Python: Select Interpreter. Ensure you ran `uv activate` at least once in the project.

- "Package version conflicts"

    Run `uv sync` to apply the lockfile. If you changed dependencies, run `uv add ...` again and re‑sync.
    

---

### Minimal reference: common commands

```bash
# New project
uv init

# Set project Python
uv python 3.12

# Add / remove deps
uv add fastapi uvicorn
uv remove uvicorn

# Recreate env from lockfile
uv sync

# Run commands inside env
uv run python -V
uv run pytest

# Activate interactive shell
uv activate
```

---

### Learn more (official docs)

- uv overview and docs: [https://docs.astral.sh/uv/](https://docs.astral.sh/uv/)
- Install uv: [https://docs.astral.sh/uv/getting-started/installation/](https://docs.astral.sh/uv/getting-started/installation/)

Note: The uv documentation structure may change over time. Visit the main docs site for the latest guides on Python version management, dependency locking, and package building.