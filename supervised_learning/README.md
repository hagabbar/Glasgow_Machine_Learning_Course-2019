## Supervised Learning

This is the supervised learning portion of our machine learning course. This is the session for the first week.

We will create a Python virtual environment containing all the packages needed to do these exercises.

If using `Conda`, please enter the following commands after cloning the repository.

```
>>> conda env create -f environment.yml
>>> conda activate supervised-learning
>>> conda install pytorch torchvision -c pytorch
```

or if using your own Python install, please enter the following commands

```
>>> pip install virtualenv
>>> python -m venv supervised-learning
>>> source supervised-learning/bin/activate
>>> pip install -r requirements.txt
>>> pip install pytorch torchvision
```
