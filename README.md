# Table of Contents
- [How to make a Python package to use with pip](#how-to-make-a-python-package-to-use-with-pip)


# How to make a Python package to use with pip

0. Make an account at [TestPyPi](https://test.pypi.org/), and get an API Token [here](https://test.pypi.org/manage/account/token/)
1. Download the initial project files ([python-package-initial.zip](https://github.com/arm-on/useful-things-to-know/blob/main/pip-package-initial.zip)), and unzip the folder
2. Install "twine": Run `python3 -m pip install --upgrade twine`
3. Change the terminal's current directory to where the `pyproject.toml` exists
4. Build the package: `python3 -m build` (a `dist` folder containing two files will be created after this).
5. Run `python3 -m twine upload --repository testpypi dist/*` to upload the package to the `testpypi` directory. Now, the terminal asks you for a username and a password. Enter `__token__` as the username and `YOUR_API_TOKEN` as the password (note that it includes `pypi-` at the beginning).
6. Install the package from the `testpypi`: `python3 -m pip install --index-url https://test.pypi.org/simple/ --no-deps example-package-armon` (you can change `armon` to whatever you want. But make sure you change it inside the `pyproject.toml` before doing this. Also, `src/example_package_armon` should be changed). 



