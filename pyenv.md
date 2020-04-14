# PyEnv Notes
**check which versions are available**  
pyenv versions

**check the python version currently active**  
python -V

**see where python file lives (finds also site packages)**  
which python
pyenv which python

**switch between virtual environments (activate)**  
pyenv global 2.7.15

**install a specific versions of python**  
pyenv install 3.6.8

**creating new environment**  
pyenv virtualenv <python_version> <environment_name>

**activating your version**  
pyenv local myproject

**manually activating and deactivating (if '$(pyenv virtualenv-init -)' is not in shell)**  
pyenv activate <environment_name>  
pyenv deactivate 