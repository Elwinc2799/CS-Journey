## Default virtual environment

Check if virtualenv library is installed

```
which virtualenv
```

Install virtualenv in terminal

```
pip3 install virtualenv
```

Create a virtual environment in current directory

```
virtualenv env_name
```

Create a virtual environment with specific version

```
virtualenv -p /usr/bin/python2.7 env_name
```

Activate a virtual environment
```
source env_name/bin/activate
```

Install the required packages based on a requirements.txt file in a virtual environment
```
pip3 install -r requirements.txt
```

Deactivate a virtual environment
```
deactivate
```

Delete a virtual environment
```
rm -r env_name
```

## Conda Virtual Environment

Install miniconda in MacOS using Homebrew

```
brew install miniconda
```

Check miniconda version

```
conda --version
```

Create virtual environment
```
conda create --name env_name
```

Create virtual environment with a specific Python version

```
conda create --name env_name python=3.9
```

Check all created virtual environment

```
conda env list

or

conda info --envs
```

Install packages into an environment 

```
conda install --name env_name scipy

if no environment specified, packages will be installed to the current environment
```

To use pip in an environment, run

```
conda install --name env_name pip
```

Activate an environment

```
conda activate env_name
```

View a list of installed packages

```
conda list
```

To view a specific package installed in an environment, run

```
conda list -n env_name scipy
```

Deactivate an environment

```
conda deactivate
```

Remove an environment

```
conda remove --name env_name --all
```