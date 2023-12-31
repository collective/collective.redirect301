.. This README is meant for consumption by humans and pypi. Pypi can render rst files so please do not use Sphinx features.
   If you want to learn more about writing documentation, please check out: http://docs.plone.org/about/documentation_styleguide.html
   This text does not appear on pypi or github. It is a comment.

.. image:: https://github.com/collective/collective.redirect301/actions/workflows/plone-package.yml/badge.svg
    :target: https://github.com/collective/collective.redirect301/actions/workflows/plone-package.yml

.. image:: https://coveralls.io/repos/github/collective/collective.redirect301/badge.svg?branch=main
    :target: https://coveralls.io/github/collective/collective.redirect301?branch=main
    :alt: Coveralls

.. image:: https://codecov.io/gh/collective/collective.redirect301/branch/master/graph/badge.svg
    :target: https://codecov.io/gh/collective/collective.redirect301

.. image:: https://img.shields.io/pypi/v/collective.redirect301.svg
    :target: https://pypi.python.org/pypi/collective.redirect301/
    :alt: Latest Version

.. image:: https://img.shields.io/pypi/status/collective.redirect301.svg
    :target: https://pypi.python.org/pypi/collective.redirect301
    :alt: Egg Status

.. image:: https://img.shields.io/pypi/pyversions/collective.redirect301.svg?style=plastic   :alt: Supported - Python Versions

.. image:: https://img.shields.io/pypi/l/collective.redirect301.svg
    :target: https://pypi.python.org/pypi/collective.redirect301/
    :alt: License


======================
collective.redirect301
======================

Thanks to `plone.app.redirector`_ Plone saves all URL changes that happen in the content and redirects the user to the proper content url.

It also allows the content-editor to create custom URLs for the content.

When doing so Plone uses a `HTTP 302`_ status code to redirect the user to the new URL.

Sometimes you want those redirects to return a `HTTP 301`_ status code, signaling that the redirect is *Permanent*.

There was a philosophical discussion when the status code was decided and the decission was to return a *Temporary* redirect.

This addon product, when enabled, changes that behavior and allows returning a *Permanent* redirect in such cases.


Installation
------------

Install collective.redirect301 by adding it to your buildout::

    [buildout]

    ...

    eggs =
        collective.redirect301


and then running ``bin/buildout``


Finally you need to go to the Plone Addons Controlpanel and install the product there.


Authors
-------

- Lur Ibargutxi <libargutxi@codesyntax.com>


Contribute
----------

- Issue Tracker: https://github.com/collective/collective.redirect301/issues
- Source Code: https://github.com/collective/collective.redirect301


Support
-------

If you are having issues, please let us know.


License
-------

The project is licensed under the GPLv2.

.. _`HTTP 302`: https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/302
.. _`HTTP 301`: https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/301
.. _`plone.app.redirector`: https://pypi.org/project/plone.app.redirector/