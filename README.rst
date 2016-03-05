|Build Status|

cookiecutter-packer-project
==================================================

Cookiecutter template for Packer project.

Requirements
------------

Cookiecutter (>=1.3.0) (https://github.com/audreyr/cookiecutter)

How to
------

You can create new project of Cookiecutter template as follows.

.. code:: bash

    $ cookiecutter gh:FGtatsuro/cookiecutter-packer-project
    ...
    project_name [Name of generated project]: test-project
    project_description [Description of generated project]: Test Project
    year [2016]:
    author [FGtatsuro]:
    ...
    $ cd use-generated-template
    $ ls -1a
    .
    ..
    LICENSE
    README.rst

You can overwrite default value of the field prompt asks with `~/.cookiecutterrc`.
It's better to overwrite 'author' field with your Github username.

.. code:: bash

    $ cat ~/.cookiecutterrc
    default_context:
        author: "FGtatsuro"
    
    $ cookiecutter gh:FGtatsuro/cookiecutter-packer-project
    ...
    author [FGtatsuro]: 
    ...

.. |Build Status| image:: https://travis-ci.org/FGtatsuro/cookiecutter-packer-project.svg?branch=master
   :target: https://travis-ci.org/FGtatsuro/cookiecutter-packer-project

