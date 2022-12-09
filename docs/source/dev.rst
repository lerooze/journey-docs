Development
===========
We'd love you to contribute to *journey*!


.. contents::
   :local:
   :backlinks: none

Issues
------

Questions, feature requests and bug reports are all welcome as [discussions or issues](https://github.com/lerooze/journey-docs/issues/new/choose). 


Pull Requests
-------------

It should be extremely simple to get started and create a Pull Request.


You'll need to have a version between **python 3.8 and 3.10**, **pipenv**, **git**, and **make** installed.

.. code-block:: bash

    # 1. clone your fork and cd into the repo directory
    git clone git@github.com:<your username>/journey-docs.git
    cd journey-docs

    # 2. Set up a virtualenv
    pipenv install --dev

    # 3. Checkout a new branch and make your changes
    git checkout -b my-new-feature-branch
    # make your changes...

    # 4. Build documentation
    make html

    # ... commit, push, and create your pull request
