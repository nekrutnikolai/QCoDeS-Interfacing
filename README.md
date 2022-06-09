<h1 align="center">
  QCoDeS-Interfacing
</h1>

<p align="center">
  Interfacing various equipment through Ethernet and GPIB with QCoDeS through the development of drivers and accompanying programs in python, initially in jupyter lab.
</p>

To Do:
- [x] Install Ubuntu on lab desktop
- [x] Install *jupyter lab* on Ubuntu
  - [x] Install miniconda
- [ ] Install QCoDeS
- [ ] Go through the QCoDeS tutorial again
- [ ] Interface with the Yokogawa GS200 over Ethernet

# Progress thus far

## Step 1: Configuring the lab computer

### Ubuntu

The SSD was wiped and the latest version of Ubuntu, 22.04 LTS, was installed on it. I used [balenaEtcher](https://www.balena.io/etcher/) to create the installation media.

### Miniconda

First, miniconda was installed by downloading the latest release:
```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

The file has a *.sh* ending meaning that it is a shell script. So to install it, navigate to the directory of the file in the terminal and then make the script executable:
```
chmod +x Miniconda3-latest-Linux-x86_64.sh
```

Then, execute it:
```
./Miniconda3-latest-Linux-x86_64.sh
```

### QCoDeS & jupyter lab installation

To actually install QCoDeS, first a conda environment was created following this [installation guide](https://qcodes.github.io/Qcodes/start/index.html) using python version 3.9, the latest supported by QCoDeS:
```
conda create -n qcodes python=3.9
```

Then, the environment was activated:
```
conda activate qcodes
```

Next, the latest version of QCoDeS was installed with pip:

```
pip install qcodes
```

Jupyter lab was installed with pip also:
```
pip install jupyterlab
```
