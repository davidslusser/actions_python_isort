# actions_python_isort
A Github action for sorting imports with isort.


<br/>

## How to use
In your .github/workflows directory, create a yaml file (such as main.yaml). Add a job for each desired workflow with the `uses` keyword. Use the `with` keyword to pass any desired variables.


Examples:

```
on: [push]

jobs:
  safety:
    runs-on: ubuntu-latest
    name: "isort"
    steps:
      - uses: davidslusser/actions_python_isort@v1.0.0
```
<br/>

```
on: [push]

jobs:
  safety:
    runs-on: ubuntu-latest
    name: "isort"
    steps:
      - uses: davidslusser/actions_python_isorty@v1.0.0
        with:
          options: "--check --diff"
          pip_install_command: "pip install -e .[dev]"
          python_version: "3.9"
```


<br/>

## Inputs
  - **options:** optional flags/parameters used in isort command (defaults to "`--check`")
  - **pip_install_command:** pip install command (defaults to "`pip install isort`")
  - **python_version:** version of python to run workflow with (defaults to "`3.x`")


<br/>

## References
 - https://pycqa.github.io/isort/
