# Docker Without Cookiecutter
    In this repo we try to do practical on docker creating dockerfile only.

## PreRequsite :

    - Software which you have to install : 
             1. docker-desktop 	
             2. git 

    - If you are working on VSCode install extension : 
             1. docker

    - If you have seeing error in :
             1. Click on the given link : https://aka.ms/wsl2kernel and install this software.
             2. When page open just look for STEP 4: DOWNLOAD THE LINUX KERNEL UPDATE PACKAGE  where you get this link click on it and download 
             3. https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi 

    - Create your docker account on : https://www.docker.com/

## Install Requirements :
    pip install -r requirements.txt

## How to check docker is installed and ready for work or not:
    - In vs code terminal type : docker login (if you logged in then it’s working)
    - In cmd type : docker –verson (if you saw version you can now ready to work)
 
## Step To Setup Your Docker:
    Create your django projects as you in general create. Only add 3 files at project level
        1- Dockerfile 	
        2- command.txt	
        3- .dockerignore

## In dockerfile Mention : 
    FROM python:3.8-slim-buster
    WORKDIR /app
    COPY requirements.txt requirements.txt
    RUN pip3 install -r requirements.txt
    COPY . .
    CMD ["python","manage.py","runserver","0.0.0.0:8000"]

## Command to Run Docker:
    1. docker build --tag python-django .
    2. docker run --publish 8000:8000 python-django

### Refrence : 
[Blog](nahid-ibne-akhtar.medium.com/django-app-on-docker-or-dockerize-your-existing-django-app-on-windows-10-be4c28937dc)

<a href="https://www.youtube.com/watch?v=W5Ov0H7E_o4">Youtube Link</a>

<a href="https://docs.google.com/document/d/1yClbE24tpVuEaNYpljbb1L0Wwio7Mz5Aj4P8Uk7NrZ4/edit?usp=sharing">Google Doc </a>

# testing

Behold My Awesome Project!

[![Built with Cookiecutter Django](https://img.shields.io/badge/built%20with-Cookiecutter%20Django-ff69b4.svg?logo=cookiecutter)](https://github.com/cookiecutter/cookiecutter-django/)
[![Black code style](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)

License: MIT

## Settings

Moved to [settings](http://cookiecutter-django.readthedocs.io/en/latest/settings.html).

## Basic Commands

### Setting Up Your Users

-   To create a **normal user account**, just go to Sign Up and fill out the form. Once you submit it, you'll see a "Verify Your E-mail Address" page. Go to your console to see a simulated email verification message. Copy the link into your browser. Now the user's email should be verified and ready to go.

-   To create a **superuser account**, use this command:

        $ python manage.py createsuperuser

For convenience, you can keep your normal user logged in on Chrome and your superuser logged in on Firefox (or similar), so that you can see how the site behaves for both kinds of users.

### Type checks

Running type checks with mypy:

    $ mypy testing

### Test coverage

To run the tests, check your test coverage, and generate an HTML coverage report:

    $ coverage run -m pytest
    $ coverage html
    $ open htmlcov/index.html

#### Running tests with pytest

    $ pytest

### Live reloading and Sass CSS compilation

Moved to [Live reloading and SASS compilation](https://cookiecutter-django.readthedocs.io/en/latest/developing-locally.html#sass-compilation-live-reloading).

## Deployment

The following details how to deploy this application.

### Docker

See detailed [cookiecutter-django Docker documentation](http://cookiecutter-django.readthedocs.io/en/latest/deployment-with-docker.html).
