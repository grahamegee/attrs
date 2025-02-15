Changelog
=========

Versions are year-based with a strict backwards compatibility policy.
The third digit is only for regressions.


16.0.0 (UNRELEASED)
-------------------

Backward-incompatible changes:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Python 3.3 and 2.6 aren't supported anymore.
  They may work by chance but any effort to keep them working has ceased.

  The last Python 2.6 release was on October 29, 2013 and isn't supported by the CPython core team anymore.
  Major Python packages like Django and Twisted dropped Python 2.6 a while ago already.

  Python 3.3 never had a significant user base and wasn't part of any distribution's LTS release.

Changes:
^^^^^^^^

- Allow the case of initializing attributes that are set to ``init=False``.
  This allows for clean initializer parameter lists while being able to initialize attributes to default values.
  `[32] <https://github.com/hynek/attrs/issues/32>`_


----


15.2.0 (2015-12-08)
-------------------

Changes:
^^^^^^^^

- Add a ``convert`` argument to ``attr.ib``, which allows specifying a function to run on arguments.
  This allows for simple type conversions, e.g. with ``attr.ib(convert=int)``.
  `[26] <https://github.com/hynek/attrs/issues/26>`_
- Speed up object creation when attribute validators are used.
  `[28] <https://github.com/hynek/attrs/issues/28>`_


----


15.1.0 (2015-08-20)
-------------------

Changes:
^^^^^^^^

- Add ``attr.validators.optional`` that wraps other validators allowing attributes to be ``None``.
  `[16] <https://github.com/hynek/attrs/issues/16>`_
- Fix multi-level inheritance.
  `[24] <https://github.com/hynek/attrs/issues/24>`_
- Fix ``__repr__`` to work for non-redecorated subclasses.
  `[20] <https://github.com/hynek/attrs/issues/20>`_


----


15.0.0 (2015-04-15)
-------------------

Changes:
^^^^^^^^

Initial release.
