# Classic pip environment setup

Use this guide only if `uv` is not available on your computer. It creates the
same project environment with Python's built-in `venv` tool and installs the
required packages directly with `pip`. You do not need a requirements file.

Complete the one-time Git steps in [README.md](README.md) before using this
guide.

## 1. Check if Python 3.13 is installed (one-time)

Check that Python 3.13 is available:

**Windows PowerShell**

```powershell
py -3.13 --version
```

**macOS / Linux / Git Bash**

```bash
python3.13 --version
```

The command should display `Python 3.13` followed by a patch version.

## 2. Create the project environment (one-time per clone)

Open a terminal in the repository root.

**Windows PowerShell**

```powershell
py -3.13 -m venv .venv
.venv\Scripts\python.exe -m pip install --upgrade pip
.venv\Scripts\python.exe -m pip install html5lib jupyterlab lxml matplotlib numpy openpyxl pandas scikit-learn seaborn xlsxwriter
```

**macOS / Linux / Git Bash**

```bash
python3.13 -m venv .venv
.venv/bin/python -m pip install --upgrade pip
.venv/bin/python -m pip install html5lib jupyterlab lxml matplotlib numpy openpyxl pandas scikit-learn seaborn xlsxwriter
```

These commands create `.venv` inside the repository and install the packages
used in the unit. You do not need to activate the environment when you use the
full Python path shown above.

## 3. Open the project in VS Code

Open the repository folder in VS Code. Accept the prompt to install the
recommended Python and Jupyter extensions, or install them from the Extensions
panel.

Open an `.ipynb` file and check the kernel shown in the top-right corner. If
VS Code does not select this project's environment automatically, click the
kernel name, choose **Select Another Kernel**, then **Python Environments**, and
select the interpreter inside this repository's `.venv` folder.

VS Code may display the environment as `.venv`, `Python 3`, or a similar name.
The important part is that the interpreter path is inside this repository's
`.venv` folder.

## Alternative: launch JupyterLab in the browser

**Windows PowerShell**

```powershell
.venv\Scripts\python.exe -m jupyter lab
```

**macOS / Linux / Git Bash**

```bash
.venv/bin/python -m jupyter lab
```
