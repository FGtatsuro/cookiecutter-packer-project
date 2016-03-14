{{ cookiecutter.project_name }}
==================================================

|Build Status|

{{ cookiecutter.project_description }}

Supported platforms are here.

- Docker
  - Debian
  - Alpine Linux

Requirements
------------

The dependencies on other softwares/librarys for this project.

Supported build environments are here.

- Ubuntu(>= 14.04)
    - Python (2.7.x)
- OSX(>= 10.9.5)
    - Python (2.7.x)
    - Homebrew (>= 0.9.5)

How to
------

1. Setup Packer build environment.

.. code:: bash

    $ pip install -r requirements.txt
    $ ansible-galaxy install -r role_requirements.yml
    $ ansible-playbook playbooks/buildenv.yml -i inventory/default -l buildenv

2. Build base image.

.. code:: bash

    $ packer build platforms/docker/debian.json

3. If you want to upload the image, you need to use the way for each image type.

.. code:: bash

    # Docker
    $ docker login -e="$DOCKER_EMAIL" -u="$DOCKER_USERNAME" -p="$DOCKER_PASSWORD"
    $ docker push <repository>:<tag>

.. |Build Status| image:: https://travis-ci.org/FGtatsuro/{{ cookiecutter.project_name }}.svg?branch=master
   :target: https://travis-ci.org/FGtatsuro/{{ cookiecutter.project_name }}
