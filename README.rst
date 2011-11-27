SymPy webpages
==============

These are SymPy webpages served at:

http://sympy.org/

using github. To modify them, edit the templates in the ``templates`` dir and::

    ./generate

You need to install jinja2 (http://jinja.pocoo.org/) and Babel
(http://pypi.python.org/pypi/Babel).

How to translate
----------------

First extract all translatable texts into a .pot file using::

    ./extract_i18n_text

Then translate it by creating a .po file with the translation in the i18n
directory. Compile it using::

    ./compile_i18n
