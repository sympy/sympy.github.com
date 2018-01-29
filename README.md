# SymPy Website

This is the SymPy website served at:

http://sympy.org/

using GitHub Pages.

To modify it, edit the files in the `templates` directory. You can check the
output with

    ./generate

You need to install jinja2 (http://jinja.pocoo.org/) and Babel
(http://pypi.python.org/pypi/Babel).

The website is generated automatically on [Travis
CI](https://travis-ci.org/sympy/sympy.github.com) using. The pages are served
using GitHub pages from the
[`master`](https://github.com/sympy/sympy.github.com/tree/master) branch. All
modifications should be made to the
[`sources`](https://github.com/sympy/sympy.github.com/tree/sources) branch. The
`master` branch is generated automatically.

## Translations

The web pages for each language are generated into the `cs`, `de`, `en`
directories. In order to add a new language, first extract all translatable
texts into a `.pot` file using

    ./extract_i18n_text

It will appear in the i18n directory. Then translate it by creating a `.po` file
with the translation in the i18n directory. Compile it using

    ./compile_i18n

Then add the language in the generate script, generate the pages and commit the
generated files. Don't forget to add the new language in the `base.html` so that
one can switch into it.
