# Computer Vision Assignment 02

\---



## Environment Setup

This project uses a Python **virtual environment (venv)** to manage dependencies cleanly and avoid conflicts with your system Python.

### Prerequisites

* Python 3.8 or higher installed on your system
* `pip` available
* Terminal / Command Prompt access

\---

### Step 1 — Clone the repository

```bash
git clone https://github.com/BudhvinThinomal/cv-assignment-02.git
cd cv-assignment-02
```

Or if you already have the folder locally:

```bash
cd cv-assignment-02
```

\---

### Step 2 — Create the virtual environment

```bash
# Mac / Linux
python3 -m venv venv

# Windows
python -m venv venv
```

\---

### Step 3 — Activate the virtual environment

```bash
# Mac / Linux
source venv/bin/activate

# Windows (Command Prompt)
venv\\Scripts\\activate.bat

# Windows (PowerShell)
venv\\Scripts\\Activate.ps1
```

You will see `(venv)` appear at the start of your terminal prompt — this confirms the environment is active.

> \*\*Important:\*\* You must activate the venv every time you open a new terminal before working on this project.

\---

### Step 4 — Install all dependencies

```bash
pip install -r requirements.txt
```

This installs all required packages including OpenCV, NumPy, Matplotlib, SciPy, and Jupyter.

\---

### Step 5 — Register the venv as a Jupyter kernel

This is the most commonly missed step. Without it, Jupyter uses the system Python and cannot find `cv2`.

```bash
python -m ipykernel install --user --name=cv\_assignment --display-name "CV Assignment 02 (venv)"
```

\---

### Step 6 — Launch Jupyter Lab

```bash
jupyter lab
```

\---

### Step 7 — Select the correct kernel in Jupyter

When you open any notebook:

1. Look at the **top right corner** of the notebook
2. Click the kernel name
3. Select **"CV Assignment 02 (venv)"** from the list

\---

### Verify your setup

Run this as the first cell in any notebook to confirm everything is working:

```python
import sys
print("Python:", sys.executable)  # Should show a path inside your venv/ folder

import cv2, numpy, matplotlib, scipy
print("cv2        :", cv2.\_\_version\_\_)
print("numpy      :", numpy.\_\_version\_\_)
print("matplotlib :", matplotlib.\_\_version\_\_)
print("scipy      :", scipy.\_\_version\_\_)
```

\---

### Deactivate the virtual environment

When you are done working:

```bash
deactivate
```

\---

### Updating requirements.txt

If you install any new packages during the project, update the requirements file:

```bash
pip freeze > requirements.txt
git add requirements.txt
git commit -m "Update requirements.txt"
```

\---

## Dependencies

|Package|Purpose|
|-|-|
|opencv-python|Image I/O, filtering, morphology, transforms|
|numpy|Array operations, kernel computation|
|matplotlib|Plotting images, histograms, 3D surfaces|
|nbformat|Notebook creation utilities|
|ipykernel|Register venv as Jupyter kernel|
|jupyterlab|Notebook IDE|



