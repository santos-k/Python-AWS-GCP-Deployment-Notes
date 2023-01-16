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

## PIP in Windows:
   1. Installation: `python -m pip install --upgrade pip`
   2. Version Check: `pip --version`
   3. Uninstall: `python -m pip uninstall pip`



## Linux: 
   1. Installation: `sudo apt-get install python3-pip`
   2. Version Check: `sudo apt-get install python3-pip`
   3. Uninstall: `python3 -m pip uninstall pip`


## Install/Unistall Python Package
1. Install/Unistall single package: 
   ```pip install <package name>
      pip install pandas
      
      pip uninstall <package name>
      pip uninstall pandas
   ```
2. To install/uninstall multiple packages:
    using pip, you can list them all out in a single command, separated by spaces. For example: 
   ```
      pip install package1 package2 package3
      pip install pandas numpy requests

      pip uninstall package1 package2 package3
      pip uninstall pandas numpy requests
   ```
3. Install/Uninstall using file: 
   A requirements file is a plain text file that lists all the packages and their versions that you want to install
   ```
      pip install -r filename
      pip install -r requirements,txt

      pip uninstall -r filename
      pip uninstall -r requirements,txt      
   ```

   ## Freeze
   The pip freeze command is used to generate a list of all the packages and their versions currently installed in a Python environment. The output of the command is written to a file in a format that can be used with the pip install command. This file is commonly called a "requirements file" and has the file extension .txt.
   The pip freeze command generates a list of all installed packages in the format of <package>==<version>.
      1. Genarate requirements.txt
         ```
            pip freeze > requirements.txt
         ```
      2. without specifying the file name, this will print the packages and their versions in the command prompt
         ```
            pip freeze
         ```



