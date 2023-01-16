# Python and PIP installation guide
# Python
## Windows:
  1. Installation: Download python installation package for windows from [here](https://www.python.org/downloads/windows/) and install, make sure check for Add PAT
  2. Uninstall: Control Panel > Python.exe > select and double click to uninstall
  3. Version check: Run CMD and type `python` press enter to check the version
  
## Linux: 
 1. Installation: 
    1. to install python `sudo apt-get install python3` 
    2. to install python2 `sudo apt-get install python`
    3. Specific version: `sudo apt-get install python3.8`
 2. Check Version:
     ```python3 --version
        python --version
     ```
 3. Uninstall: 
    1. `sudo apt-get remove python3` This command will remove the Python 3 package and its dependencies, but it will not delete any configuration files or user-installed packages.
    2. `sudo apt-get purge python3` if you want to remove all the dependencies, configuration files and user-installed packages as well, you can use the following command
   
   
# PIP 
pip is a package management system for Python, used to install and manage software packages written in Python. It is the standard package manager for Python and is typically included with Python distributions. With pip, you can install packages from the Python Package Index (PyPI) and other indexes. It allows users to install packages easily, and also allows for the management of multiple versions of the same package.

