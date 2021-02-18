!---
!header-includes:
!  - \hypersetup{colorlinks=true,
!            allbordercolors={0 0 0},
!            pdfborderstyle={/S/U/W 1}}
!---

Open source PyMOL 2.4 for Windows
=====

This repository provides a method to install PyMOL v2.4 by [Anaconda](https://www.anaconda.com) on Windows.


# Download & Instalação

Follow these steps to install PyMOL v2.4:

## 1. Install Anaconda

Download [Anaconda](https://www.anaconda.com/products/individual) and install it.

## 2. Create a environment on Anaconda

Open `Anaconda Prompt` (type it on Start menu), and run:

```bash
conda create -n pymol python=3.7
``` 

Then, activate the `pymol` environment:

```bash
conda activate pymol
```

## 3. Install required Python packages

Still on `Anaconda Prompt`, run:

- pip 3:
```bash
conda install -c anaconda pip
```

- Numpy:
```bash
pip install numpy
```

- PMW:
```bash
pip install pmw
```

- pyqt5:
```bash
pip install pyqt5
```

## 4. Download PyMOL whl files

Download pre-compiled Open-Source PyMOL wheel files, compatible with Python 3.7.x and Windows 64-bit, from the links below:

- [pymol-launcher](https://github.com/jvsguerra/pymol-2.4-win/releases/latest/download/pymol_launcher-2.1-cp37-cp37m-win_amd64.whl)

- [pymol](https://github.com/jvsguerra/pymol-2.4-win/releases/latest/download/pymol-2.4.0-cp37-cp37m-win_amd64.whl)

_Note:_ You can check Python version on anaconda by typing `python --version`.

If you are using a different Python version or Windows 32-bits, please there are other pre-compiled versions [here](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pymol). 

The filename structure is the following:

![](imgs/wheel_filename_structure.png)

## 5. Install wheel files

In the `pymol` environment, switch to download directory (`C:\Downloads`):

```bash
cd C:\Downloads
```

Then, install `pymol_launcher-2.1-cp37-cp37m-win_amd64.whl` by typing:

```bash
pip install --no-index --find-links="%CD% pymol_launcher-2.1-cp37-cp37m-win_amd64.whl
```

Finally, to install `pymol-2.4.0-cp37-cp37m-win_amd64.whl`, run:

```bash
pip install --upgrade --no-deps pymol-2.4.0-cp37-cp37m-win_amd64.whl
```

_Note_: If you downloaded different files in **Step 4**, replace `pymol_launcher-2.1-cp37-cp37m-win_amd64.whl` and `pymol-2.4.0-cp37-cp37m-win_amd64.whl` by the downloaded wheel files.

## 6. Launch PyMOL v2.4

In the activate `pymol` environment on `Anaconda Prompt`, run:

```bash
pymol
```

Then, PyMOL v2.4 will be launched and ready to go.
