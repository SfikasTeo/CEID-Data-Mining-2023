## Short Guide: Python create a [Venv ](https://docs.python.org/3/library/venv.html)
* Prerequisites : [Python](https://archlinux.org/packages/core/x86_64/python/) and [Python-pip](https://archlinux.org/packages/extra/any/python-pip/)
* Enter the working directory and create a virtual environment : `python -m venv ./venv`
* Depending on the shell in use : `source ./venv/bin/activate.<shell>`
* After activating the venv we can assure that everything worked correctly using : `which python`
  * In case the python interpeter inside the venv is not automatically used, you can use the interpeter by `./venv/bin/pyhtonX`
* Use pip to install packages as : `pip install Django`
  * Using globally installed packages inside the venv:  
  Create it using --system-site-packages option, *or*  
  Edit `pyenv.cfg` and set `include-system-site-packages = true`  
  **Reactivate** the venv, verify via `pip list` 
* In order to deactivate the venv use : `deactivate` 

#### Using the virtual environment with Jupyter Notebook
* Activate the venv and install the ipykernel : `pip install ipykernel`
* Add the venv to the Jupyter Notebook : `python -m ipykernel install --user --name=venv`


