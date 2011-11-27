SymPy webpages
==============

These are SymPy webpages served at:

http://sympy.org/

using github. To modify them, edit the templates in the ``templates`` dir and::

    ./generate

You need to install jinja2 (http://jinja.pocoo.org/) and Babel
(http://pypi.python.org/pypi/Babel).

More details
------------

The web pages for each language are generated into the "cs", "de", "en"
directories. In order to add a new language, first extract all translatable
texts into a .pot file using::

    ./extract_i18n_text

It will appear in the i18n directory. Then translate it by creating a .po file
with the translation in the i18n directory. Compile it using::

    ./compile_i18n

Then add the language in the generate script, generate the pages and commit the
generated files. Don't forget to add the new language in the base.html so that
one can switch into it.
