# Hivecoin-developer

Developer guide for Hivecoin project.

## Install 

Content are writen in reStructuredText (RST) and rendered with Sphinx.

Much of the content displayed on the is converted from Markdown to
[reStructuredText (RST)](http://docutils.sourceforge.net/rst.html) and rendered
with [Sphinx](http://www.sphinx-doc.org).

### Render the documentation locally

To render the documentation locally you first need to install Sphinx and the
required theme modules, e.g. by running

    pip install -r requirements.txt

This should be done from the root of this repo. Then you can execute Sphinx by calling

    make html

This will generate HTML from the RST sources in the directory `_build/html`.
It's all static HTML so you can just open the index.html file in your browser
locally to view the rendered documentation.

