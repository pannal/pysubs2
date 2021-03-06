pysubs2
=======

pysubs2 is a Python library for editing subtitle files. It’s based on *SubStation Alpha*, the native format of `Aegisub <http://www.aegisub.org/>`_; it also supports *SubRip* and *MicroDVD* formats. There is a small CLI tool for batch conversion and retiming.

::

    import pysubs2
    subs = pysubs2.load("my_subtitles.ass", encoding="utf-8")
    subs.shift(s=2.5)
    for line in subs:
        line.text = "{\\be1}" + line.text
    subs.save("my_subtitles_edited.ass")

pysubs2 works with Python 3 and 2.7. It’s available under the MIT license (see bottom of the page).

To install pysubs2, just use `pip <https://pypi.python.org/pypi/pip>`_: ``pip install pysubs2``. You can also clone `the GitHub repository <https://github.com/tkarabela/pysubs2/>`_ and install via ``python setup.py install``.

If you find a bug or have something to say, please let me know `via GitHub <https://github.com/tkarabela/pysubs2/issues>`_ or email (tkarabela at seznam dot cz). Your feedback is much appreciated. Thanks!

Documentation
-------------

.. toctree::
   :maxdepth: 2

   cli
   tutorial
   api-reference
   release-notes


License
-------

::

    Copyright (c) 2014-2015 Tomas Karabela

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in
    all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
    THE SOFTWARE.
