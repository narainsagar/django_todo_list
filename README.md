

```bash

## Check if python is installed?
$ python --version

Python 3.10.7

# Step 1: Set Up Your Virtual Environment and Django

## Create project directory
$ mkdir projects/todo_list
$ cd projects/todo_list


### Create and activate virutal environment

$ python -m venv venv
$ source venv/bin/activate

### Install django

(venv) $ python -m pip install django


### Check if django installed correctly
$ python # this will open python terminal, execute following code inside python terminal.

>>> import django
>>> django.get_version()
'4.2.1'
>>> exit()

### Freeze the project dev dependencies.

(venv) $ python -m pip freeze > requirements.txt

# Step 2: Create Your Django To-Do App


## Scaffold the Parent Project

(venv) $ django-admin startproject todo_project .


## this is how your project directory structure will look like:

todo_list/
│
├── todo_project/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
├── venv/
│
├── manage.py
└── requirements.txt


## Get Started on Django To-Do List App

(venv) $ django-admin startapp todo_app


todo_list/
│
├── todo_app/
│
├── todo_project/
│
└── venv/

todo_app/
│
├── migrations/
│   └── __init__.py
│
├── __init__.py
├── admin.py
├── apps.py
├── models.py
├── tests.py
└── views.py

## Create and Apply migrations

(venv) $ python manage.py makemigrations todo_app
(venv) $ python manage.py migrate

## Run the app.

(venv) $ python manage.py runserver 3030

Navigate to http://localhost:3030/ in your browser




## Add sample Todo Data via Django-admin


(venv) $ python manage.py createsuperuser

sample: admin / admin
```

