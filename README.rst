======================
cookiecutter-pypackage
======================

Cookiecutter template for a Python package.

* Free software: BSD license
* Vanilla testing setup with `unittest` and `python setup.py test`
* Travis-CI_: Ready for Travis Continuous Integration testing
* Tox_ testing: Setup to easily test for Python 2.6, 2.7, 3.3
* Sphinx_ docs: Documentation ready for generation with, for example, ReadTheDocs_

Usage
-----

Generate a Python package project::

    cookiecutter https://github.com/dariusbakunas/cookiecutter-pypackage.git

Then:

* Create a repo and put it there.
* Add the repo to your Travis CI account.
* Add the repo to your ReadTheDocs account + turn on the ReadTheDocs service hook.
* Release your package the standard Python way. Here's a release checklist: https://gist.github.com/audreyr/5990987

User Config
-----------

If you use Cookiecutter a lot, you'll find it useful to have a
`.cookiecutterrc` file in your home directory like this:

.. code-block:: yaml

    default_context:
        full_name: "Your FullName"
        email: "Your email"
        github_username: "Your github username"
    cookiecutters_dir: "$HOME/my-custom-cookiecutters-dir/"
    abbreviations:
        pp: https://github.com/username/cookiecutter-pypackage.git
        gh: https://github.com/{0}.git
        bb: https://bitbucket.org/{0}

Possible settings are:

* default_context: A list of key/value pairs that you want injected as context
  whenever you generate a project with Cookiecutter. These values are treated
  like the defaults in `cookiecutter.json`, upon generation of any project.
* cookiecutters_dir: Directory where your cookiecutters are cloned to when you
  use Cookiecutter with a repo argument.
* abbreviations: A list of abbreviations for cookiecutters. Abbreviations can
  be simple aliases for a repo name, or can be used as a prefix, in the form
  `abbr:suffix`. Any suffix will be inserted into the expansion in place of
  the text `{0}`, using standard Python string formatting.  With the above
  aliases, you could use the `cookiecutter-pypackage` template simply by saying
  `cookiecutter pp`, or `cookiecutter gh:username/cookiecutter-pypackage`.
  The `gh` (github) and `bb` (bitbucket) abbreviations shown above are actually
  built in, and can be used without defining them yourself.

Not Exactly What You Want?
--------------------------

Don't worry, you have options:

Similar Cookiecutter Templates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* `Nekroze/cookiecutter-pypackage`_: A fork of this with a PyTest test runner,
  strict flake8 checking with Travis/Tox, and some docs and `setup.py` differences.

* `tony/cookiecutter-pypackage`_: Fork with py2.7+3.3 optimizations. Flask/Werkzeug-style
  test runner, ``_compat`` module and module/doc conventions. See ``README.rst`` or
  the `github comparison view`_ for exhaustive list of additions and modifications.

* Also see the `network`_ and `family tree`_ for this repo. (If you find
  anything that should be listed here, please add it and send a pull request!)

Fork This / Create Your Own
~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you have differences in your preferred setup, I encourage you to fork this
to create your own version. Or create your own; it doesn't strictly have to
be a fork.

* Once you have your own version working, add it to the Similar Cookiecutter
  Templates list above with a brief description.

* It's up to you whether or not to rename your fork/own version. Do whatever
  you think sounds good.

.. _Travis-CI: http://travis-ci.org/
.. _Tox: http://testrun.org/tox/
.. _Sphinx: http://sphinx-doc.org/
.. _ReadTheDocs: https://readthedocs.org/
.. _`Nekroze/cookiecutter-pypackage`: https://github.com/Nekroze/cookiecutter-pypackage
.. _`tony/cookiecutter-pypackage`: https://github.com/tony/cookiecutter-pypackage
.. _github comparison view: https://github.com/tony/cookiecutter-pypackage/compare/audreyr:master...master
.. _`network`: https://github.com/audreyr/cookiecutter-pypackage/network
.. _`family tree`: https://github.com/audreyr/cookiecutter-pypackage/network/members
