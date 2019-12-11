.. -*- coding: utf-8 -*-

.. Note: this page is linked to from CONTRIBUTING.rst in all packages.  Keep it short!

=========================================
Guidelines for contributing to Plone Core
=========================================

You probably came here by clicking one of the 'guidelines for contributing' links on GitHub.
You probably have an issue to report or you want to create a pull request.
Thanks a lot!
Let's bring you up to speed with the minimum you need to know to start contributing.


Create an issue
===============

* If you know the issue is for a specific package, you can add an issue there.
  When in doubt, create one in the `CMFPlone issue tracker <https://github.com/plone/Products.CMFPlone/issues>`_.

* Please specify a few things:

  - What steps reproduce the problem?

  - What do you expect when you do that?

  - What happens instead?

  - Which Plone version are you using?

* If it is a visual issue, can you add a screen shot?

* If there is an error in the Site Setup error log, please include it.
  Especially a traceback is helpful.
  Click on the  'Display traceback as text' link if you see it in the error log.


Create a pull request
=====================

* Legally,
  you can NOT contribute code unless you have signed the :doc:`contributor agreement <agreement>`.
  This means that we can NOT accept pull requests from you unless this is done,
  so please don't put the code reviewers at risk and do it anyways.

* Add a changelog entry as a `towncrier <https://github.com/hawkowl/towncrier>`_ news entry in the ``news`` directory in the repository root.
  The entry should make clear what your change is about.
  When in doubt, don't worry about it.
  The file should follow this naming scheme: ``<issue or PR number>.<changelog type>``.
  Please reference the issue (on the same Github repository, no cross-references possible here).
  If there is no issue and it doesn't make sense to create one, you can just use the pull-request number.
  The changelog type should be one of our `configured issue types <https://github.com/plone/plone.releaser/blob/master/pyproject.toml>`_: ``feature``, ``bugfix`` or ``breaking``.
  If there is no ``news`` directory the repository probably doesn't use towncrier yet.
  In that case, add your changelog entry to ``CHANGES.rst``, ``CHANGES.txt`` or ``docs/HISTORY.txt`` - whatever is available.

* For new features, an addition to README.rst is probably needed.
  A package may include other documentation that needs updating.

* All text that can be shown in a browser must be translatable.
  Please mark all such strings as translatable.

* Be nice and use code quality checkers like flake8 and jshint.

* See if you can use git to squash multiple commits into one where this makes sense.
  If you are not comfortable with git, never mind.

* If after reading this you become hesitant: don't worry.
  You can always create a pull request, mark it as WIP (work in progress),
  and improve the above points later.
