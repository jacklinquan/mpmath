mpmath
======

|pypi version| |Build status| |Code coverage status| |Zenodo Badge|

.. |pypi version| image:: https://img.shields.io/pypi/v/mpmath.svg
   :target: https://pypi.python.org/pypi/mpmath
.. |Build status| image:: https://github.com/mpmath/mpmath/workflows/test/badge.svg
   :target: https://github.com/mpmath/mpmath/actions?workflow=test
.. |Code coverage status| image:: https://codecov.io/gh/mpmath/mpmath/branch/master/graph/badge.svg
   :target: https://codecov.io/gh/mpmath/mpmath
.. |Zenodo Badge| image:: https://zenodo.org/badge/2934512.svg
   :target: https://zenodo.org/badge/latestdoi/2934512

A Python library for arbitrary-precision floating-point arithmetic.

Website: https://mpmath.org/
Main author: Fredrik Johansson <fredrik.johansson@gmail.com>

Mpmath is free software released under the New BSD License (see the
LICENSE file for details).

0. History and credits
----------------------

The following people (among others) have contributed major patches
or new features to mpmath:

* Pearu Peterson <pearu.peterson@gmail.com>
* Mario Pernici <mario.pernici@mi.infn.it>
* Ondrej Certik <ondrej@certik.cz>
* Vinzent Steinberg <vinzent.steinberg@gmail.com>
* Nimish Telang <ntelang@gmail.com>
* Mike Taschuk <mtaschuk@ece.ualberta.ca>
* Case Van Horsen <casevh@gmail.com>
* Jorn Baayen <jorn.baayen@gmail.com>
* Chris Smith <smichr@gmail.com>
* Juan Arias de Reyna <arias@us.es>
* Ioannis Tziakos <itziakos@gmail.com>
* Aaron Meurer <asmeurer@gmail.com>
* Stefan Krastanov <krastanov.stefan@gmail.com>
* Ken Allen <ken.allen@sbcglobal.net>
* Timo Hartmann <thartmann15@gmail.com>
* Sergey B Kirpichev <skirpichev@gmail.com>
* Kris Kuhlman <kristopher.kuhlman@gmail.com>
* Paul Masson <paulmasson@analyticphysics.com>
* Michael Kagalenko <michael.kagalenko@gmail.com>
* Jonathan Warner <warnerjon12@gmail.com>
* Max Gaukler <max.gaukler@fau.de>
* Guillermo Navas-Palencia <g.navas.palencia@gmail.com>
* Nike Dattani <nike@hpqc.org>

Numerous other people have contributed by reporting bugs,
requesting new features, or suggesting improvements to the
documentation.

For a detailed changelog, including individual contributions,
see the CHANGES file.

Fredrik's work on mpmath during summer 2008 was sponsored by Google
as part of the Google Summer of Code program.

Fredrik's work on mpmath during summer 2009 was sponsored by the
American Institute of Mathematics under the support of the National Science
Foundation Grant No. 0757627 (FRG: L-functions and Modular Forms).

Any opinions, findings, and conclusions or recommendations expressed in this
material are those of the author(s) and do not necessarily reflect the
views of the sponsors.

Credit also goes to:

* The authors of the GMP library and the Python wrapper
  gmpy, enabling mpmath to become much faster at
  high precision
* The authors of MPFR, pari/gp, MPFUN, and other arbitrary-
  precision libraries, whose documentation has been helpful
  for implementing many of the algorithms in mpmath
* Wikipedia contributors; Abramowitz & Stegun; Gradshteyn & Ryzhik;
  Wolfram Research for MathWorld and the Wolfram Functions site.
  These are the main references used for special functions
  implementations.
* George Brandl for developing the Sphinx documentation tool
  used to build mpmath's documentation

Release history:

* Version 1.3.0 released on March 7, 2023
* Version 1.2.1 released on February 9, 2021
* Version 1.2.0 released on February 1, 2021
* Version 1.1.0 released on December 11, 2018
* Version 1.0.0 released on September 27, 2017
* Version 0.19 released on June 10, 2014
* Version 0.18 released on December 31, 2013
* Version 0.17 released on February 1, 2011
* Version 0.16 released on September 24, 2010
* Version 0.15 released on June 6, 2010
* Version 0.14 released on February 5, 2010
* Version 0.13 released on August 13, 2009
* Version 0.12 released on June 9, 2009
* Version 0.11 released on January 26, 2009
* Version 0.10 released on October 15, 2008
* Version 0.9 released on August 23, 2008
* Version 0.8 released on April 20, 2008
* Version 0.7 released on March 12, 2008
* Version 0.6 released on January 13, 2008
* Version 0.5 released on November 24, 2007
* Version 0.4 released on November 3, 2007
* Version 0.3 released on October 5, 2007
* Version 0.2 released on October 2, 2007
* Version 0.1 released on September 27, 2007

1. Download & installation
--------------------------

Mpmath requires Python 3.9 or later versions.  It has been tested with CPython
3.9 through 3.14 and for PyPy 3.10.

The latest release of mpmath can be downloaded from the mpmath
website and from https://github.com/mpmath/mpmath/releases

It should also be available in the Python Package Index at
https://pypi.python.org/pypi/mpmath

To install latest release of Mpmath with pip, simply run

``pip install mpmath``

or from the source tree

``pip install .``

The latest development code is available from
https://github.com/mpmath/mpmath

See the main documentation for more detailed instructions.

2. Documentation
----------------

Documentation in reStructuredText format is available in the
docs directory included with the source package. These files
are human-readable, but can be compiled to prettier HTML using
`Sphinx <https://www.sphinx-doc.org/>`_.

The most recent documentation is also available in HTML format:

https://mpmath.readthedocs.io/

3. Running tests
----------------

The unit tests in mpmath/tests/ can be run with `pytest
<https://pytest.org/>`_, see the main documentation.

You may also want to check out the demo scripts in the demo
directory.

The master branch is automatically tested on the Github Actions.

4. Known problems
-----------------

Mpmath is a work in progress. Major issues include:

* Some functions may return incorrect values when given extremely
  large arguments or arguments very close to singularities.

* Directed rounding works for arithmetic operations. It is implemented
  heuristically for other operations, and their results may be off by one
  or two units in the last place (even if otherwise accurate).

* Some IEEE 754 features are not available. Inifinities and NaN are
  partially supported, there is no signed zero; denormal rounding is
  not available at all.

* The interface for switching precision and rounding is not finalized.
  The current method is not threadsafe.

5. Help and bug reports
-----------------------

General questions and comments can be `sent <mailto:mpmath@googlegroups.com>`_
to the `mpmath mailinglist <https://groups.google.com/g/mpmath>`_.

You can also report bugs and send patches to the mpmath issue tracker,
https://github.com/mpmath/mpmath/issues
