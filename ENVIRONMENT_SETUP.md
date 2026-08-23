# Environment setup

Complete the one-time Git steps in [README.md](README.md) before using this
guide.

This repository uses [uv](https://docs.astral.sh/uv/) to manage Python and
packages. Python **3.13** and all shared packages are pinned in
`pyproject.toml` / `uv.lock`, so every student ends up with the same
environment.

## 1. Install uv (one-time)

**Windows PowerShell**

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

For other methods, see the [official uv installation
guide](https://docs.astral.sh/uv/getting-started/installation/).

**macOS / Linux / Git Bash**

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Restart your terminal afterwards so `uv` is on your `PATH`.

## 2. Set up the project (one-time per clone)

From the repository root:

```bash
uv sync
```

This downloads Python 3.13 if needed, creates `.venv`, and installs the
exact package versions from `uv.lock`. There is nothing to activate and
nothing to install manually.

## 3. Open the project in VS Code (recommended)

Open the repository folder in VS Code. It will prompt you to install the
recommended extensions (Python and Jupyter) — accept that prompt, or install
them manually from the Extensions panel.

The workspace is configured to use the `.venv` created by `uv sync`. Open an
`.ipynb` file and run a cell. VS Code should select that environment
automatically, so cells run in place with no browser tab required.

VS Code may show a label such as `vit1106_student (3.13.x)`, `.venv`, or
`Python 3` in the notebook toolbar and saved notebook metadata. This display
label can vary between computers and does not change which project environment
is used. The important parts are that the selected interpreter is inside this
repository's `.venv` folder and the notebook kernel identifier is `python3`.

If VS Code previously remembered a different environment for this workspace,
click the kernel name in the top-right corner once, choose **Select Another
Kernel**, then **Python Environments**, and select this repository's `.venv`.
VS Code will remember that choice for later sessions.

## Alternative: launch JupyterLab in the browser

```bash
uv run jupyter lab
```
