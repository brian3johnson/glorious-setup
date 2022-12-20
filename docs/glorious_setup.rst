==================
The Glorious Setup
==================

------------------------------
How to set up a python project
------------------------------

Setup a GitHub repository
=========================

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
     ~/dev/source/brian3johnson                                                                        took  1m 15s  schlockchain
   ❯ cd glorious-setup
   ❯ la
   total 16K
   drwxr-xr-x 8 brian brian 4.0K Dec 19 17:14 .git
   -rw-r--r-- 1 brian brian 1.8K Dec 19 17:14 .gitignore
   -rw-r--r-- 1 brian brian 1.1K Dec 19 17:14 LICENSE
   -rw-r--r-- 1 brian brian   48 Dec 19 17:14 README.md
   ❯ 

Setup a virtual environment
===========================

.. code-block:: sh

   ❯ python -m venv venv
   ❯ source venv/bin/activate
   ❯ python -m pip install pip -U
   Requirement already satisfied: pip in ./venv/lib/python3.10/site-packages (21.2.3)
   Collecting pip
   Using cached pip-22.3.1-py3-none-any.whl (2.1 MB)
   Installing collected packages: pip
   Attempting uninstall: pip
      Found existing installation: pip 21.2.3
      Uninstalling pip-21.2.3:
         Successfully uninstalled pip-21.2.3
   Successfully installed pip-22.3.1
     ~/dev/source/brian3johnson/glorious-setup on   main !1                                                       glorious-setup
   ❯

Install sphinx
==============

.. code-block:: sh

   ❯ pip install sphinx
   Collecting sphinx
   Using cached sphinx-5.3.0-py3-none-any.whl (3.2 MB)
   Collecting babel>=2.9
   Using cached Babel-2.11.0-py3-none-any.whl (9.5 MB)
   Collecting sphinxcontrib-jsmath
   Using cached sphinxcontrib_jsmath-1.0.1-py2.py3-none-any.whl (5.1 kB)
   Collecting docutils<0.20,>=0.14
   Using cached docutils-0.19-py3-none-any.whl (570 kB)
   Collecting Pygments>=2.12
   Using cached Pygments-2.13.0-py3-none-any.whl (1.1 MB)
   Collecting snowballstemmer>=2.0
   Using cached snowballstemmer-2.2.0-py2.py3-none-any.whl (93 kB)
   Collecting sphinxcontrib-qthelp
   Using cached sphinxcontrib_qthelp-1.0.3-py2.py3-none-any.whl (90 kB)
   Collecting alabaster<0.8,>=0.7
   Using cached alabaster-0.7.12-py2.py3-none-any.whl (14 kB)
   Collecting imagesize>=1.3
   Using cached imagesize-1.4.1-py2.py3-none-any.whl (8.8 kB)
   Collecting Jinja2>=3.0
   Using cached Jinja2-3.1.2-py3-none-any.whl (133 kB)
   Collecting sphinxcontrib-applehelp
   Using cached sphinxcontrib_applehelp-1.0.2-py2.py3-none-any.whl (121 kB)
   Collecting packaging>=21.0
   Using cached packaging-22.0-py3-none-any.whl (42 kB)
   Collecting sphinxcontrib-devhelp
   Using cached sphinxcontrib_devhelp-1.0.2-py2.py3-none-any.whl (84 kB)
   Collecting requests>=2.5.0
   Using cached requests-2.28.1-py3-none-any.whl (62 kB)
   Collecting sphinxcontrib-htmlhelp>=2.0.0
   Using cached sphinxcontrib_htmlhelp-2.0.0-py2.py3-none-any.whl (100 kB)
   Collecting sphinxcontrib-serializinghtml>=1.1.5
   Using cached sphinxcontrib_serializinghtml-1.1.5-py2.py3-none-any.whl (94 kB)
   Collecting pytz>=2015.7
   Using cached pytz-2022.7-py2.py3-none-any.whl (499 kB)
   Collecting MarkupSafe>=2.0
   Using cached MarkupSafe-2.1.1-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (25 kB)
   Collecting charset-normalizer<3,>=2
   Using cached charset_normalizer-2.1.1-py3-none-any.whl (39 kB)
   Collecting certifi>=2017.4.17
   Using cached certifi-2022.12.7-py3-none-any.whl (155 kB)
   Collecting idna<4,>=2.5
   Using cached idna-3.4-py3-none-any.whl (61 kB)
   Collecting urllib3<1.27,>=1.21.1
   Using cached urllib3-1.26.13-py2.py3-none-any.whl (140 kB)
   Installing collected packages: snowballstemmer, pytz, alabaster, urllib3, sphinxcontrib-serializinghtml, sphinxcontrib-qthelp, sphinxcontrib-jsmath, sphinxcontrib-htmlhelp, sphinxcontrib-devhelp, sphinxcontrib-applehelp, Pygments, packaging, MarkupSafe, imagesize, idna, docutils, charset-normalizer, certifi, babel, requests, Jinja2, sphinx
   Successfully installed Jinja2-3.1.2 MarkupSafe-2.1.1 Pygments-2.13.0 alabaster-0.7.12 babel-2.11.0 certifi-2022.12.7 charset-normalizer-2.1.1 docutils-0.19 idna-3.4 imagesize-1.4.1 packaging-22.0 pytz-2022.7 requests-2.28.1 snowballstemmer-2.2.0 sphinx-5.3.0 sphinxcontrib-applehelp-1.0.2 sphinxcontrib-devhelp-1.0.2 sphinxcontrib-htmlhelp-2.0.0 sphinxcontrib-jsmath-1.0.1 sphinxcontrib-qthelp-1.0.3 sphinxcontrib-serializinghtml-1.1.5 urllib3-1.26.13
     ~/dev/source/brian3johnson/glorious-setup on   main !1                                            took  6s  glorious-setup
   ❯

Configure sphinx
================

Option 1 | Use the interactive wizard
-------------------------------------

.. code-block:: sh

   ❯ sphinx-quickstart docs
   Welcome to the Sphinx 5.3.0 quickstart utility.

   Please enter values for the following settings (just press Enter to
   accept a default value, if one is given in brackets).

   Selected root path: docs

   You have two options for placing the build directory for Sphinx output.
   Either, you use a directory "_build" within the root path, or you separate
   "source" and "build" directories within the root path.
   > Separate source and build directories (y/n) [n]:

   The project name will occur in several places in the built documentation.
   > Project name: glorious-setup
   > Author name(s): Brian E Johnson <brian@brian3johnson.me>
   > Project release []:

   If the documents are to be written in a language other than English,
   you can select a language here by its language code. Sphinx will then
   translate text that it generates into that language.

   For a list of supported codes, see
   https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-language.
   > Project language [en]:

   Creating file /home/brian/dev/source/brian3johnson/glorious-setup/docs/conf.py.
   Creating file /home/brian/dev/source/brian3johnson/glorious-setup/docs/index.rst.
   Creating file /home/brian/dev/source/brian3johnson/glorious-setup/docs/Makefile.
   Creating file /home/brian/dev/source/brian3johnson/glorious-setup/docs/make.bat.

   Finished: An initial directory structure has been created.

   You should now populate your master file /home/brian/dev/source/brian3johnson/glorious-setup/docs/index.rst and create other documentation
   source files. Use the Makefile to build the docs, like so:
      make builder
   where "builder" is one of the supported builders, e.g. html, latex or linkcheck.

   ❯ la
   total 24K
   drwxr-xr-x 8 brian brian 4.0K Dec 19 17:14 .git
   -rw-r--r-- 1 brian brian 1.8K Dec 19 17:14 .gitignore
   -rw-r--r-- 1 brian brian 1.1K Dec 19 17:14 LICENSE
   -rw-r--r-- 1 brian brian 2.0K Dec 19 17:18 README.md
   drwxr-xr-x 5 brian brian 4.0K Dec 19 17:25 docs
   drwxr-xr-x 5 brian brian 4.0K Dec 19 17:17 venv
   ❯ la docs
   total 28K
   -rw-r--r-- 1 brian brian  634 Dec 19 17:25 Makefile
   drwxr-xr-x 2 brian brian 4.0K Dec 19 17:25 _build
   drwxr-xr-x 2 brian brian 4.0K Dec 19 17:25 _static
   drwxr-xr-x 2 brian brian 4.0K Dec 19 17:25 _templates
   -rw-r--r-- 1 brian brian 1006 Dec 19 17:25 conf.py
   -rw-r--r-- 1 brian brian  458 Dec 19 17:25 index.rst
   -rw-r--r-- 1 brian brian  800 Dec 19 17:25 make.bat
     ~/dev/source/brian3johnson/glorious-setup on   main !1 ?1                                                    glorious-setup
   ❯

**NOTE**: Another approach is to first create the `docs` directory:

.. code-block:: sh

   mkdir docs
   cd docs
   sphinx-quickstart docs


Then follow the prompts.

Option 2 | Use command line options
-----------------------------------

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

Option 3 | Use minimal command line options
-------------------------------------------

This version uses `-q` to suppress the interactive wizard.

.. code-block:: sh

   sphinx-quickstart \
      -q \
      -p glorious-setup \
      -a "Brian E Johnson <brian@brian3johnson.me>" \
      -v 0.0.1 \
      --ext-autodoc \
      --ext-todo \
      docs

Adding ``-r 0.0.1`` adds ``release = '0.0.1'`` to :file:`conf.py`.
Adding ``-v 0.0.1`` adds ``version = '0.0.1'`` and ``release = '0.0.1'`` to :file:`conf.py`.
The ``language`` key and value are not added to :file:`conf.py`.

Setting options to empty strings for ``-p "" -a "" -v ""`` or ``-p "" -a "" -r ""``
adds following to :file:`conf.py`:

.. code-block:: sh

   project = ''
   copyright = '2022, '
   author = ''

``version`` and ``release`` keys and values are not created.

Option 4 | Use command line options with a custom template
----------------------------------------------------------

:program:`sphinx-quickstart` uses the template files in :file:`{project_root}/venv/lib/python3.{XX}/site-packages/sphinx/templates/quickstart`
to generate the :file:`Makefile`, :file:`conf.py`, :file:`make.bat`, and :file:`root_doc.rst` files in your project.

You can customize these template files and use them instead of the templates shipped with :program:`sphinx`.

Copy the files to a new directory. I will use :file:`~/.config/sphinx/templates/quickstart_brian/`

.. code-block:: sh

   mkdir -p ~/.config/sphinx/templates/brian/
   cp -r venv/lib/python3.10/site-packages/sphinx/templates/quickstart \
      ~/.config/sphinx/templates/quickstart_brian/


Then add the template option `-t` with the location of your custom template.

.. code-block:: sh

   sphinx-quickstart \
      -q \
      -p glorious-setup \
      -a "Brian E Johnson <brian@brian3johnson.me>" \
      -v 0.0.1 \
      --ext-autodoc \
      --ext-todo \
      -t ~/.config/sphinx/templates/quickstart_brian \
      docs

What do all the other templates in :file:`venv/lib/python3.{XX}/site-packages/sphinx/templates/` do?
How does the ``-d NAME=VALUE`` option work in those templates?

These templates are used for various builders. They are not templates used for themes. Theme files are stored at: :file:`la venv/lib/python3.{XX}/site-packages/sphinx/themes/`

.. code-block:: sh

   sphinx-quickstart \
      -q \
      -p glorious-setup \
      -a "Brian E Johnson <brian@brian3johnson.me>" \
      -v 0.0.1 \
      --ext-autodoc \
      --ext-todo \
      -t ~/.config/sphinx/templates/quickstart_brian \
      -d dogsay=woof \
      docs

.. note::
   
   The following code in :file:`conf.py_t` does not render since there is no
   command line flag for ``append_syspath``. Additionally,
   the ``module_path`` returns ``Undefined`` in the output.

   These two are addressed in the :program:`apidoc` cli tool.

   Lastly, does the jinja documentation talk about the ``repr`` filter using double-quotes 
   instead of single quotes? Not that I have found. I also have not found the ``repr`` filter
   in the jinja2 documentation.