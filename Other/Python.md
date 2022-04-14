# Python

## Virtual environment

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