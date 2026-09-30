# Physics-Informed Neural Networks (PINN) for Boundary Value Problems in Continuum Mechanics

*From an axially loaded prismatic bar to a cantilever plate in plane stress*

Mikołaj Miecznikowski, MSc Eng. · 30 September 2026

> The slides and notebooks are in Polish.

## Contents

| File | Description |
|---|---|
| [lecture.pdf](lecture.pdf) | Slides |
| [notebooks/01. poisson_equation](notebooks/01.%20poisson_equation) | Axially loaded prismatic bar: PINN |
| [notebooks/02. cantilever_beam](notebooks/02.%20cantilever_beam) | Cantilever beam under uniform load |
| [notebooks/03. cantilever_beam_inverse](notebooks/03.%20cantilever_beam_inverse) | Cantilever beam: identifying Young's modulus from deflection measurements (inverse problem) |

## Running the notebooks

Requirements: Git and Python 3.12 (the tested version).

### 1. Clone the repository

```bash
git clone https://github.com/Mieczmik/lectures.git
cd lectures/2026-09-PINN
```

### 2. Create a virtual environment

Linux / macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Windows (PowerShell):

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

### 3. Install the dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

The notebooks run on a CPU. To use an NVIDIA GPU, install a CUDA build of PyTorch following the
instructions at [pytorch.org](https://pytorch.org/get-started/locally/), then run
`pip install -r requirements.txt` again.

### 4. Run

```bash
jupyter lab
```

Then open a notebook from the `notebooks/` directory.

**VS Code:** open this lecture folder (`2026-09-PINN`), not the repository root. VS Code
only detects a `.venv` located in the root of the opened folder:

```bash
code .
```

Then open a `.ipynb` file, click *Select Kernel* (top right) → *Python Environments* → `.venv`.

If you prefer to keep the whole repository open, choose *Select Kernel* → *Select Another Kernel…*
→ *Python Environments…* → *Create Python Environment*, where you can enter an existing interpreter
path, and point it to `2026-09-PINN/.venv/bin/python` (Windows: `2026-09-PINN\.venv\Scripts\python.exe`).
Menu labels may differ slightly between VS Code versions.

Each notebook sets the DeepXDE backend to PyTorch itself (`DDE_BACKEND=pytorch`).
