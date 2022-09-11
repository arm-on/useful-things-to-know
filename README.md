# Table of Contents

# How to make a Python package to use with pip

1. Download the initial project files ([python-package-initial.zip]()), and unzip the folder
2. Install "twine": Run `python3 -m pip install --upgrade twine`
3. Change the terminal's current directory to where the `pyproject.toml` exists
4. Build the package: `python3 -m build` (a `dist` folder containing two files will be created after this).
5. Run `python3 -m twine upload --repository testpypi dist/*` to upload the package to the `testpypi` directory.
6. Install the package from the `testpypi`: `python3 -m pip install --index-url https://test.pypi.org/simple/ --no-deps example-package-armon` (you can change `armon` to whatever you want. But make sure you change it inside the `pyproject.toml` before doing this. Also, `src/example_package_armon` should be changed). 



