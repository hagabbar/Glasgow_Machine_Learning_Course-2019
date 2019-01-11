# intro2ml
An assortment of scripts to help you get started in machine learning.

Some of scripts are based on the [examples](https://github.com/keras-team/keras/tree/master/examples) provided for keras. They have been transferred to Jupyter notebooks and a then edited and added to.

## Requirements 

These notebooks should be compatible with python 2.7 or 3.6 and require the following packages:
* NumPy
* SciPy
* Matplotlib
* Pandas
* Root_pandas
* Keras (with either TensorFlow or Theano backend)

The following packages are also requiered to use a virutalenv in Jupyter:
* iPyKernel

The recommended installation is with a python [virtual enviroment](https://virtualenv.pypa.io/en/stable/) or similar (conda environment).

## Installation with virtualenv

These instructions will assume you have a version of python installed with pip.

### Installing virtualenv

The simplest way to install virutalenv is:

```
$ sudo pip install virtualenv
```

If you don't have sudo privileges, it can be installed for just the user with:

```
$ pip install virtualenv --user
```
If installing with ``--user``, an alias must be added to your ``.bashrc``/``.cshrc`` or equivalent. Something along the lines of:

```
alias virtualenv "python ~/.local/lib/python2.7/site-packages/virtualenv.py"
```
Virtualenv can now be used to create separate python instances to better manage different dependencies.

### Making a new virtual environment with the packages

Virtualenvs can inherit packages from the system version of python. But to keep avoid a possible version differences, these instructions will outline how to make a virtual environment with no system packages.

To create the environment:

```
$ virtualenv <path/name>
```

There are lots of other [options](https://virtualenv.pypa.io/en/stable/reference/), such as passing all or specific packages. But they are not important for this use case.

For example to create an environment called 'ml' in my current directory ```$ virtualenv ml```

Now to activate the environment with:

```
$ source </path/name/bin/activate(.csh)>
```

Bash based systems use the default ``activate`` file, where as systems with other shells (csh) use ``activate.csh``

First to make sure ``pip`` is up-to-date

```
$ pip install --upgrade pip
```

Then you can install the necessary packages using the requirements file:

```
$ pip install -r requirements.txt
```

The packages can also been installed manually:

```
$ pip install <package-name>
```
Instead of a name you can use a space separate list of packages names ``$ pip install numpy scipy pandas``.

To then add the virtualenv to Jupyter:

```
$ ipython kernel install --user --name=<name>
```
Here ``<name>`` is the kernel name that will appear in Jupyter.

To then leave the virtualenv simply type:

```
$ deactivate
```

## Starting Jupyter

To open the Jupyter:

```
$ jupyter-notebook
```
Now when you make a new notebook you should be able to select the enviroment you created.
