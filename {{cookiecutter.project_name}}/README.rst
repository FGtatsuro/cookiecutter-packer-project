{{ cookiecutter.project_name }}
==================================================

|Build Status|

{{ cookiecutter.project_description }}

Requirements
------------

The dependencies on other softwares/librarys for this project.

- Debian
    - Python (2.7.x)
    - pip (>= 8.0.3)
- OSX
    - Python (2.7.x)
    - pip (>= 8.0.3)
    - Homebrew (>= 0.9.5)

How to
------

1. Setup Packer build environment.

.. code:: bash

    $ pip install -r requirements.txt
    $ ansible-galaxy install -r role_requirements.yml
    $ ansible-playbook playbooks/buildenv.yml -i inventory/default -l buildenv


.. |Build Status| image:: https://travis-ci.org/FGtatsuro/{{ cookiecutter.project_name }}.svg?branch=master
   :target: https://travis-ci.org/FGtatsuro/{{ cookiecutter.project_name }}
