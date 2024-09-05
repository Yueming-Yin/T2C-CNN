# T2C-CNN
Codes and data for the paper named "Discriminating Single-Molecule Binding Event from Diffraction-Limited Fluorescence".

- This work is accorded NTU Technique Disclosure application number 2024-299. All rights reserved by Yin Yueming (yueming.yin@ntu.edu.sg), Lipo Wang (elpwang@ntu.edu.sg), Thorsten Wohland (twohland@nus.edu.sg), Nithin Pathoor (nithin@nus.edu.sg) and Shao Ren Sim (shaoren.sim@u.nus.edu).

# Environments
- Anaconda
- Pytorch
- Jupyter
- GPU with CUDA

# Get Started With A New Conda Virtual Environment
## Anaconda Installation
For installing anaconda on your OS, please refer to [Anaconda Installation](https://docs.anaconda.com/free/anaconda/install/).

Once the anaconda is properly installed, one can create a new virtual environment by entering the following command in terminal:
```bash
cd path/to/your/T2C_CNN-main/folder
conda create --name T2C_CNN --file ./requirements.txt
conda activate T2C_CNN
```

## Jupyter Configuration
For configuring jupyter (has been installed from requirements.txt), please refer to [Jupyter Configuration](https://jupyter-server.readthedocs.io/en/latest/users/configuration.html).

Here, we provide our commands of configuring jupyter with conda:
```bash
jupyter notebook --generate-config
ipython
>>> from notebook.auth import passwd
>>> passwd()
(enter your passwords)
(conform your passwords)
Output: [your password key]
```

Then, open your generated jupyter_notebook_config.py file (usually in the '/home/.jupyter' directory) to add the following commands:
```python
c.NotebookApp.ip = '*'
c.NotebookApp.port = [port id, e.g., 8888]
c.NotebookApp.open_browser = False
c.NotebookApp.allow_remote_access = True
c.NotebookApp.password = [your password key]
c.NotebookApp.notebook_dir = [your default workdir (should include the T2C-CNN-main folder)]
```

To start jupyter notebook, please enter this commond in the terminal:
```bash
jupyter notebook
```
Then, one can access jupyter notebook at [your server's ip]:[your port id] in the same domain with the server.

# Data Preparation and Processing