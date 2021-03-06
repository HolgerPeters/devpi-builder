=========
Changelog
=========

This lists the most important changes for each release.


Unreleased
==========

Changed
-------

* Changelog is now in the format suggested by Keep-a-CHANGELOG_.


Version 2.2.0 — 2016-05-23
==========================

Added
-----

* Capture build errors for better output in case of build failures. Thanks Travis Mehlinger.


Version 2.1.0 — 2016-04-22
==========================

Added
-----

* Support for client certificates. Thanks Hans Lawrenz.


Version 2.0.0 — 2016-01-20
==========================

Added
-----

* Compatibility with pip >= 8.0 by relying on pip's default download cache
  mechanism instead of explicitly requiring a download cache. This effectively
  disables caching for people still using pip < 6.0.
  Thanks Christian Stefanescu.
* Support for dry-running the wheel build without changing the devpi server state.
* Python 3.5 is now officially supported.

Removed
-------

* Python 3.2 is no longer supported.


Version 1.0.0 — 2015-05-22
==========================

Changed
-------

- Use devpi-plumber_ instead of a custom devpi wrapper.
- Check the blacklist first when deciding whether to build a package.

Version 0.4.0 — 2015-09-13
==========================

Changed
-------

* Only consider a package to exist if it is a wheel and it is compatible with
  the current system. Thanks Michael Still and David Szotten

Fixed
-----

* The source distribution now properly contains a README.md.
  Thanks Mikhail Lukyanchenko.


Version 0.3.0 — 2015-08-15
==========================

Added
-----

* Support for special-case handling of pure python wheels
* Optional support for reporting skipped packages in a JUnit-compatible XML
* Python 3 support


Version 0.2.1 — 2014-08-07
==========================

Fixed
-----

* Fixed crash if a built wheel could cannot be found
  (because pip<=1.5.2 skipped it).


Version 0.2.0 — 2014-08-01
==========================

Added
-----

* Support for package blacklisting to never build certain wheels.

Changed
-------

* build as many packages as possible. Do not stop if one fails.


Version 0.1.0 — 2014-08-01
==========================

Added
-----

- Build a list of packages and upload them to a Devpi index


.. _devpi-plumber: https://github.com/blue-yonder/devpi-plumber
.. _Keep-a-CHANGELOG: http://keepachangelog.com
