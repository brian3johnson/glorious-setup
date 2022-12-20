================
The Optimal Flow
================

-----------------
The straight dope
-----------------

Setup a GitHub repository
=========================

.. todo::

   Fetch the command line arguments version of this.

.. code-block:: sh

   ❯ gh repo create
   ? What would you like to do? Create a new repository on GitHub from scratch
   ? Repository name glorious-setup
   ? Description How to set up a python project
   ? Visibility Public
   ? Would you like to add a README file? Yes
   ? Would you like to add a .gitignore? Yes
   ? Choose a .gitignore template Python
   ? Would you like to add a license? Yes
   ? Choose a license MIT License
   ? This will create "glorious-setup" as a public repository on GitHub. Continue? Yes
   ✓ Created repository brian3johnson/glorious-setup on GitHub
   ? Clone the new repository locally? Yes
   Cloning into 'glorious-setup'...
   Enter passphrase for key '/home/brian/.ssh/id_rsa':
   remote: Enumerating objects: 5, done.
   remote: Counting objects: 100% (5/5), done.
   remote: Compressing objects: 100% (4/4), done.
   remote: Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
   Receiving objects: 100% (5/5), done.

**Result**::

   project_root
   +- .git/
   +- .gitignore
   +- LICENSE
   +- README.md

Setup a virtual environment
===========================

.. code-block:: sh

   ❯ cd glorious-setup
   ❯ python -m venv venv
   ❯ source venv/bin/activate
   ❯ python -m pip install pip -U

**Result**::

   project_root
   +- .git/
   +- venv/
   +- .gitignore
   +- LICENSE
   +- README.md

Install sphinx
==============

.. code-block:: sh

   ❯ pip install sphinx

Configure sphinx
================

.. code-block:: sh

   sphinx-quickstart \
      -q \
      --no-sep \
      -p glorious-setup \
      -a "Brian E Johnson <brian@brian3johnson.me>" \
      -v 0.0.1 \
      -l en \
      --ext-autodoc \
      --ext-todo \
      docs

**Result**::

>  project_root
>  +- .git/
>  +- docs/
>     +- _build/
>     +- _static/
>     +- _templates/
>     +- conf.py
>     +- index.rst
>     +- make.bat
>     +- Makefile
>  +- venv/
>  +- .gitignore
>  +- LICENSE
>  +- README.md