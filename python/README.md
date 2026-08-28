# python-playground

## Virtual Environment Setup

Initialize and activate an isolated Python virtual environment before installing project dependencies.

### Commands

```bash
python3 -m venv venv
source venv/bin/activate
pip install -U pip
```

### Explanation

#### 1. `python3 -m venv venv`

- `python3` — invokes the Python 3 interpreter
- `-m venv` — runs the built-in `venv` module (no extra install needed)
- `venv` (last one) — the name of the folder to create

**Result:** Creates a `./venv/` folder containing a self-contained Python installation (its own interpreter and a separate `pip`), isolated from your system Python.

---

#### 2. `source venv/bin/activate`

- `source` — executes the script in the current shell (so env changes persist)
- `venv/bin/activate` — the activation script shipped with the venv

**Result:** Modifies the shell's `$PATH` so `python`/`pip` point to the venv copies, and changes the prompt to show `(venv)`. Packages installed afterward only affect this venv.

> On **Windows**, use `venv\Scripts\activate` instead.

---

#### 3. `pip install -U pip`

- `-U` / `--upgrade` — upgrade the package if already installed
- `pip` — upgrades pip itself inside the venv

**Result:** Brings the venv's pip to the latest version, avoiding potential issues with outdated install logic when installing packages later.

---

### Quick Recap

```
create → activate → upgrade pip → (ready to install packages)
```

To exit the venv later:

```bash
deactivate
```